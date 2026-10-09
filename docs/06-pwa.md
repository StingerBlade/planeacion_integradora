# 6. PWA de ranking

**Responsable:** Angel Arras (front, `ui/`) y G. González (back, `backend/`), con apoyo de Jesús para conectar el juego.

**FECHA DE INICIO (backend real): 2 de noviembre de 2026.**
**FECHA DE FIN: 13 de noviembre de 2026.**

> El boceto del esquema de datos se hace antes, en la Fase 1, pero el backend empieza hasta el 2-nov — G. González está 100% enfocado en el Núcleo PvP del juego hasta el 1-nov.

## Stack y decisiones (actualizado 9-oct-2026)

| Capa | Decisión |
|---|---|
| Front | React 19 + Vite 8 + `vite-plugin-pwa`, carpeta `ui/` |
| Back | Django + Django REST Framework, carpeta `backend/` **en el mismo repositorio** (monorepo) |
| Base de datos | **PostgreSQL en Supabase**, usado solo como Postgres administrado (sin la API ni el auth de Supabase). *El proyecto de Supabase aún no está creado.* |
| Hosting | **Render**, un solo Web Service plan Starter (**$7/mes**): Django sirve la API bajo `/api/` y el build de Vite con WhiteNoise. Mismo dominio, sin CORS. |
| CI | GitHub Actions: `frontend-ci` (lint + build) y `backend-ci` (ruff + migraciones + tests con Postgres temporal), en PR y push a `main`/`development` |
| CD | Render despliega solo si el CI pasa (`autoDeployTrigger: checksPass`) |

Todo el detalle, la guía para el backend y los pasos de puesta en marcha están en el [README del repositorio de la PWA](https://github.com/StingerBlade/BEARSTARDS_PWA).

## Estado al 9-oct-2026

El repositorio [`BEARSTARDS_PWA`](https://github.com/StingerBlade/BEARSTARDS_PWA) ya existe (creado el 6-oct) y tiene un proyecto base en `ui/`: React + Vite + `vite-plugin-pwa`. Se agregaron los workflows de CI y el blueprint de Render. Todavía no hay pantallas, backend ni API.

**Pendientes de infraestructura:**
- [ ] Crear el proyecto de Supabase y obtener la cadena *Session pooler*.
- [ ] Crear el servicio en Render desde `render.yaml` y capturar `DATABASE_URL` y `ALLOWED_HOSTS`.
- [ ] Exigir los checks de CI en la rama `main` (GitHub → Settings → Branches).
- [ ] G. González: crear `backend/` con proyecto `config`, `requirements.txt`, endpoint `/api/health/` y la configuración de WhiteNoise/`DATABASE_URL`.

Ya **no** es un extra post-entrega: se necesita lista, junto con el videojuego, para la presentación del 20-nov.

## Alcance mínimo (MVP)

Para que sea realista en el tiempo disponible:
- Un endpoint para **registrar el resultado de una partida** (`POST /api/resultados`).
- Un endpoint para **consultar el ranking** (`GET /api/ranking`).
- Una página web simple con la tabla de ranking.
- **Sin** cuentas de usuario ni historial detallado.

Esquema de datos sugerido por partida: jugador, resultado (ganó/perdió), puntos, fecha.

## Calendario

| Cuándo | Qué se hace |
|---|---|
| 6–9 oct (adelantado) | Repositorio creado, proyecto base React + Vite + PWA plugin, CI y blueprint de Render |
| Antes del 18-oct | Bocetar el esquema de datos y definir los 2 endpoints — G. González; crear Supabase y Render |
| 19-oct al 1-nov | **Sin trabajo de backend** — G. González está 100% en el Núcleo PvP del juego (el front puede avanzar) |
| Semana 2–8 nov | Proyecto Django + modelo de datos + endpoint `POST /api/resultados` funcionando — G. González |
| Semana 9–13 nov | Endpoint `GET /api/ranking` + página web con la tabla + desplegar + conectar el juego real (Jesús envía el resultado desde Unity al terminar cada partida) — G. González |
| 17-nov (buffer) | Prueba final de la PWA con datos reales de los playtests |

## Integración con el juego

Cuando termina cada duelo, el juego (vía Jesús, dueño del sistema de puntos) hace un `POST` al endpoint de resultados con el ganador, el perdedor y los puntos de la partida. Esto depende de que el endpoint ya exista — por eso está calendarizado para la semana 6 (9–13 nov), después de que G. González lo construya en la semana 5.

## Por qué quedó así (contexto de la decisión)

En la planeación original (documento de negocio del equipo), la PWA estaba listada como algo a construir **después** del 20-nov. El equipo corrigió esto: el 20-nov es la fecha de entrega de **todo** el proyecto, no solo del juego. Por eso la PWA se adelantó y ahora corre en paralelo al desarrollo del juego, concentrando el trabajo pesado en las semanas donde G. González ya terminó la parte más crítica del Núcleo PvP (después del 1-nov).
