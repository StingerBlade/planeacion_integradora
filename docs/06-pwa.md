# 6. PWA de Little Bearstards

**Responsables:** Angel Arras (front) y G. González (backend/API), con apoyo de Jesús para conectar el juego.

**FECHA DE INICIO (backend real): 2 de noviembre de 2026.**
**FECHA DE FIN: 13 de noviembre de 2026.**

Repositorio: [StingerBlade/BEARSTARDS_PWA](https://github.com/StingerBlade/BEARSTARDS_PWA). Su `README.md` tiene la propuesta completa (arquitectura, consumo de API, estrategia PWA, UI/UX, guía de estilos, datos y CI/CD) con diagramas.

> El boceto del esquema de datos se hace antes, pero el backend empieza hasta el 2-nov: G. González está 100% enfocado en el Núcleo PvP del juego hasta el 1-nov.

## Estado al 10-oct-2026

- Repositorio creado (6-oct) con el proyecto base en `ui/`: React 19 + Vite + `vite-plugin-pwa`.
- CI en GitHub Actions (front y back) y blueprint de Render ya en `main`.
- **Definidos el 10-oct:** arquitectura, modelo de datos, manejo de sesiones (PWA y Unity), endpoints y guía de estilos. Ver [03-decisiones.md](03-decisiones.md#pwa-datos-y-sesiones-10-oct-2026).
- Propuesta de interfaz maquetada (Inicio, Ranking, Login, Registro y Panel) con datos de prueba; pendiente de subir al repositorio.
- Entrega académica *Diseño preproyecto PWA*: cierra el 11-oct a las 00:00 (URL del repo con `README.md` y diagramas).
- Todavía no existe el backend (`backend/`) ni el despliegue en Render.

Ya **no** es un extra post-entrega: se necesita lista, junto con el videojuego, para la presentación del 20-nov.

## Alcance (MVP)

- Página de **inicio** que presenta el juego.
- **Ranking** de jugadores por puntos totales (top 10, con podio).
- **Registro e inicio de sesión** con usuario y contraseña. La misma cuenta sirve para la PWA y para el juego.
- **Panel** del jugador: estadísticas, gráfica de sus últimas 10 partidas e historial.
- API para que el juego **reporte cada partida** al terminar.
- Funciona como PWA: instalable y con funcionamiento sin conexión.

Fuera del alcance: correo electrónico, rachas, logros y rankings por periodo (semanal, mensual).

## Arquitectura

**Arquitectura Base:** una sola aplicación propia (Django) que contiene la API, las reglas de negocio, la autenticación y sirve el sitio web, desplegada como un solo servicio. La misma API REST la consumen la PWA y el juego en Unity.

| Capa | Tecnología |
|---|---|
| Front (`ui/`) | React 19 + Vite 8 + `vite-plugin-pwa` + React Router 7 + Tailwind CSS 4 |
| Back (`backend/`) | Django + Django REST Framework |
| Base de datos | PostgreSQL en **Supabase** (solo como base de datos; no se usa Supabase Auth ni su API) |
| Hosting | Render, un Web Service (plan Starter) |
| CI/CD | GitHub Actions → Render (despliega `main` solo si el CI pasa) |

Las tablas las crea Django con sus migraciones; no se crean a mano en Supabase. Una migración adicional bloquea la API automática de Supabase sobre las tablas (RLS activado y sin permisos para los roles `anon` y `authenticated`).

## Datos

| Tabla | Qué guarda |
|---|---|
| **Jugador** | Usuario, contraseña (con hash), partidas, victorias, derrotas, empates, kills, puntos totales y mejor puntuación |
| **Partida** | Identificador único (`match_id`), fecha en que terminó, si fue por abandono y qué jugador la reportó |
| **Participación** | Una por jugador en cada partida: puntos, kills, resultado (victoria, derrota o empate) y si abandonó |

Reglas que respetan los datos:

- Todas las partidas duran **10 minutos**, por eso no se guarda la duración.
- Gana quien tenga más puntos; si quedan iguales, es **empate**.
- **Quien abandona pierde** automáticamente.
- El juego envía los datos **solo al terminar** la partida, y cada partida se registra **una sola vez** (`match_id` único).

## API

| Método y ruta | Sesión | Uso |
|---|---|---|
| `POST /api/auth/registro/` | No | Crear cuenta; devuelve token y jugador |
| `POST /api/auth/login/` | No | Iniciar sesión; devuelve token y jugador |
| `POST /api/auth/logout/` | Sí | Cerrar sesión |
| `GET /api/ranking/` | No | Top 10 por puntos totales |
| `GET /api/yo/` | Sí | Estadísticas del jugador |
| `GET /api/yo/partidas/` | Sí | Historial de partidas del jugador |
| `POST /api/partidas/` | Sí | El juego reporta una partida terminada |
| `GET /api/health/` | No | Render revisa que el servicio esté vivo |

## Sesiones e integración con el juego

- Se usa **Token de Django REST Framework** para la PWA y para Unity: al iniciar sesión el servidor devuelve un token y el cliente lo manda en cada petición (`Authorization: Token <token>`).
- **El login es obligatorio para jugar en línea.** Unity no se conecta a Photon sin sesión y guarda el `id` del jugador en sus propiedades de Photon.
- Durante la partida, el MasterClient lleva el marcador (puntos y kills) en las propiedades de Photon, para que los dos clientes vean lo mismo.
- **Fin normal (10 min):** el MasterClient arma el reporte final y lo manda por RPC a los dos jugadores; **los dos** lo envían a la API. El servidor guarda el primero y responde `409` al segundo. Así la partida se registra aunque uno de los dos se desconecte justo al terminar.
- **Abandono:** el jugador que se queda reporta la partida; él gana y el que salió pierde con `abandono = true`.
- **Sin internet al terminar:** Unity guarda el reporte y lo reintenta al volver al menú o al iniciar sesión.

La guía paso a paso (backend y Unity) se le entregó a G. González en PDF.

## Diseño

Estilo **neobrutalismo cartoon**, ambientado en una juguetería de noche: bordes gruesos, sombras duras sin difuminar y colores planos y saturados, suavizados con esquinas redondeadas, tipografía juguetona y animaciones. Los osos se muestran en low poly (imágenes provisionales hasta tener los modelos finales del juego).

- **Colores principales:** `night` `#241a55` (fondo), `ink` `#1b1030` (bordes y texto sobre claro), `paper` `#fffaf0` (texto sobre oscuro), `sun` `#ffd23f` (color principal), con acentos `pink` `#ff5fa2`, `sky` `#3ec6ff`, `mint` `#5be3b0` y `tangerine` `#ff8a3d`.
- **Tipografía de la PWA:** Lilita One (títulos y botones) y Fredoka (texto). El juego mantiene la suya (Comic Neue, ver GDD).
- Diseño **mobile first** y adaptativo; respeta la preferencia de "reducir movimiento".

La guía completa está en el README del repositorio de la PWA.

## Calendario

| Cuándo | Qué se hace |
|---|---|
| 6–9 oct | Repositorio creado, proyecto base React + Vite + PWA plugin y CI |
| 10-oct | Arquitectura, modelo de datos, sesiones, endpoints y guía de estilos definidos; propuesta de interfaz maquetada |
| 11-oct | Entrega académica *Diseño preproyecto PWA* (README con la propuesta y diagramas) |
| 19-oct al 1-nov | **Sin trabajo de backend** — G. González está 100% en el Núcleo PvP del juego |
| Semana 2–8 nov | Proyecto Django, modelo de datos, migraciones, registro/login y `POST /api/partidas/` — G. González |
| Semana 9–13 nov | Ranking, panel, despliegue en Render y conexión del juego real (Jesús envía el resultado desde Unity) |
| 17-nov (buffer) | Prueba final de la PWA con datos reales de los playtests |

## Por qué quedó así (contexto de la decisión)

En la planeación original la PWA era un entregable **posterior** al 20-nov y no tenía cuentas de usuario. El equipo corrigió dos cosas:

1. El 20-nov es la entrega de **todo** el proyecto, así que la PWA se adelantó y corre en paralelo al juego.
2. Se agregaron **cuentas de usuario** (10-oct) para que el ranking y las estadísticas sean por jugador y el juego pueda reportar a quién corresponde cada partida.
