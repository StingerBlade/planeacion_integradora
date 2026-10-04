# 4. Cronograma y fases

El proyecto se divide en 5 fases del videojuego, que corren en paralelo con el desarrollo de la PWA y la app Flutter (ver secciones 6 y 7). Todas las fechas están cargadas como tarjetas con fecha límite real en Trello.

## Hitos del proyecto (fechas límite en Trello)

| Hito | Fecha | Qué se entrega |
|---|---|---|
| Arranca desarrollo del App Flutter | **28-sep-2026** | Guillermo Martínez crea el proyecto Flutter y la pantalla de ranking con datos de prueba |
| Cierre Fase 1 — Diseño y escenario | **4-oct-2026** | GDD v1, repo Unity listo, concept art aprobado, prototipo de NPC y de conexión Photon funcionando |
| Cierre Fase 2 — Osos y escenario jugable | **18-oct-2026** | Oso jugable con animaciones en el escenario de 3 pasillos, primera sincronización en red probada |
| Arranca el código real de la PWA | **2-nov-2026** | G. González empieza el proyecto Django (antes solo tenía el boceto del esquema de datos) |
| Cierre Fase 3 — Núcleo PvP completo | **1-nov-2026** | Duelo 1v1 jugable completo entre 2 computadoras distintas, conectadas por Photon |
| Cierre Fase 4 — Primera versión jugable | **13-nov-2026** | Build jugable completo con HUD, menús, NPCs y armas. **También deben estar listos, con datos reales conectados: la PWA y el app Flutter.** |
| **ENTREGA FINAL** | **20-nov-2026 (viernes)** | Juego + PWA + app Flutter + documentación |

## Fase 1 — Diseño y escenario (28-sep al 4-oct)

Sprint actual. Tarjetas individuales por persona:

- **Angel (SM):** GDD v1.0 (duelo 1v1 en línea vía Photon PUN2, mapa de 3 pasillos, NPCs simulados localmente, sin oso policía) + ceremonias de la semana agendadas.
- **Guillermo Martínez (PO):** hoja de balance cerrada + backlog de la Fase 2 priorizado + arrancar el app en Flutter (proyecto + pantalla de ranking con datos de prueba).
- **Hugo Baeza:** guía de estilo low poly aprobada + boceto del escenario de 3 pasillos.
- **G. González:** repositorio de GitHub listo (carpetas, prefabs, convención de commits); prefabs del jugador preparados para instanciarse en red (carpeta `Resources`, requisito de `PhotonNetwork.Instantiate`). **Tarea adicional agregada hoy (4-oct), a petición propia:** arrancar el HUD de vida (barra) y el feedback visual al recibir daño; se integra con el sistema real de vida/daño en la Fase 3, Semana 3.
- **Jesús Castilla:** prototipo de NavMesh con un NPC que patrulla, sin arte final.
- **Dylan Muñoz — Configurar Photon PUN2:**
  1. Crear cuenta de Photon, importar el SDK PUN2 y probar conectar 2 instancias a la misma sala.
  2. Prototipo mínimo: sincronizar el movimiento de un objeto placeholder (cubo o cápsula) entre las 2 instancias usando `PhotonView` + `PhotonTransformView`.
  3. Documentar en 1 página cómo usar PhotonView y RPCs, y compartirla con G. González y Jesús antes del viernes.
  4. Apoyar a G. González con la arquitectura del repo: dejar los prefabs listos para sincronizarse en red.

## Fase 2 — Osos y escenario jugable (5 al 18 de octubre)

Lideran Hugo Baeza y G. González. El movimiento del oso debe quedar listo para sincronizarse por red en la Fase 3.

**Semana 1 (5–11 oct):**
- Hugo: modelo 3D del oso + rig.
- G. González: importar oso a Unity, movimiento básico (correr/saltar).
- Jesús: terminar escenario modular de 3 pasillos (colisiones y navmesh).
- Dylan: cámara en tercera persona funcionando.
- Angel: refinar el backlog de la Fase 3 (tarea que originalmente era de Guillermo Martínez, reasignada porque está en Flutter).
- Angel: daily + review del viernes 11-oct.

**Semana 2 (12–18 oct):**
- Hugo: modelos de pistola, aguja, hilos y casco.
- G. González: animator con idle/correr/golpear + importar armas.
- Jesús: iluminación y ambientación del escenario.
- Dylan: primera sincronización en red del movimiento del oso (`PhotonView` + `PhotonTransformView`) usando el prototipo de conexión de la Fase 1.
- Angel: boceto de la pantalla de resultado.
- Angel: review 18-oct — demostrar el oso moviéndose en el escenario con 2 controles.

## Fase 3 — Núcleo PvP (19 de octubre al 1 de noviembre)

Lideran Dylan Muñoz (red), Jesús Castilla y G. González. Multiplayer con Photon PUN2.

> **Importante:** los NPCs de camuflaje **no** se sincronizan por red — cada cliente los simula localmente. Solo se sincronizan los 2 jugadores humanos.
>
> **Fuera del MVP:** el oso "policía" (IA que vigila si se agrede a los NPCs) no se construye en esta fase (ver sección 8). El castigo de −50 puntos por matar a un NPC ya cubre ese propósito.

**Semana 3 (19–25 oct):**
- G. González: integrar el HUD de vida y el feedback de daño (arrancado en Fase 1, ver arriba) con el sistema real de vida/daño/respawn.
- G. González: combate cuerpo a cuerpo sincronizado por RPC de Photon + golpe crítico a la cabeza (oneshot).
- Dylan: sala de Photon funcional — los 2 jugadores se emparejan y se instancian en red (`PhotonNetwork.Instantiate`).
- Jesús: sistema de vida, daño y respawn sincronizado por RPC/PhotonView.
- Hugo: animaciones de golpe, daño y muerte.
- Angel: escribir criterios de aceptación de "duelo jugado entre 2 PCs distintas" para el review (reasignado de Guillermo Martínez).
- Angel: vigilar que nadie tenga más de 2 tareas en progreso a la vez.

**Semana 4 (26 oct–1 nov):**
- G. González: sistema de armas en red — recoger y soltar objetos sincronizado (pistola, hilos, casco).
- Dylan: pantalla de sala (crear/unirse con código) + manejo básico de desconexión.
- Jesús: detección básica (correr, golpear o llevar arma a la vista delata al jugador ante el rival) + sistema de puntos. **No incluye IA de "policía".**
- Hugo: apoyo con VFX simples (impacto, muerte).
- Angel: preparar el playtest interno de la próxima semana (se necesitan 2 PCs o 2 instancias del juego) — reasignado de Guillermo Martínez.
- Angel: review 1-nov — jugar un duelo 1v1 completo entre 2 computadoras distintas, de principio a fin.

## Fase 4 — Primera versión jugable (2 al 13 de noviembre)

Dylan programa el HUD y los menús (además de la sala/lobby de Photon); Guillermo Martínez y G. González consiguen e integran música/SFX; el resto integra y corrige bugs. **Guillermo Martínez está dedicado casi de tiempo completo a la app en Flutter y no toma otras tareas del videojuego aparte de audio.**

**Semana 5 (2–8 nov):**
- Dylan: HUD con vida, tiempo y puntos en pantalla.
- Guillermo Martínez y G. González: conseguir música y SFX libres e integrarlos.
- Jesús: NPCs terminados — patrullaje y camuflaje del jugador entre ellos.
- G. González: integrar arte final (armas, oso) en la escena de juego.
- Dylan: integrar todos los sistemas en una escena jugable + pantalla de lobby de Photon.
- Hugo: terminar props y texturas finales del escenario.
- Angel: coordinar la integración, anotar pendientes para la Fase 5.

**Semana 6 (9–13 nov):**
- Dylan: menús de inicio, pausa y resultado.
- Jesús: ajuste de detección con los NPCs ya en el escenario final.
- Jesús: enviar el resultado de cada partida al API de la PWA (POST) al terminar el duelo, en cuanto G. González tenga el endpoint listo.
- G. González: corrección de bugs de combate y armas.
- Dylan: corrección de bugs de input y del duelo.
- Hugo: apoyo de arte donde haga falta.
- Angel: review 13-nov — primera versión completa, sin pulir.

## Fase 5 — Pulido y entrega (14 al 20 de noviembre)

Ver el detalle día por día en [10-semana-colchon.md](10-semana-colchon.md). Es la semana de colchón: solo pruebas, bugs, pulido y ensayo — nada de funcionalidad nueva.
