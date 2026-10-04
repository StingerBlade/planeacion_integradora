# 6. PWA de ranking (Django)

**Responsable:** G. González (con apoyo de Jesús para conectar el juego).

**FECHA DE INICIO (código real): 2 de noviembre de 2026.**
**FECHA DE FIN: 13 de noviembre de 2026.**

> El boceto del esquema de datos se hace antes, en la Fase 1, pero el código empieza hasta el 2-nov — G. González está 100% enfocado en el Núcleo PvP del juego hasta el 1-nov.

Ya **no** es un extra post-entrega: se necesita lista, junto con el videojuego, para la presentación del 20-nov.

## Alcance mínimo (MVP)

Para que sea realista en el tiempo disponible:
- Un endpoint para **registrar el resultado de una partida** (`POST /resultados`).
- Un endpoint para **consultar el ranking** (`GET /ranking`).
- Una página web simple con la tabla de ranking.
- **Sin** cuentas de usuario ni historial detallado.

Esquema de datos sugerido por partida: jugador, resultado (ganó/perdió), puntos, fecha.

## Calendario

| Cuándo | Qué se hace |
|---|---|
| Ahora (antes del 18-oct) | Bocetar el esquema de datos y definir los 2 endpoints — G. González |
| 19-oct al 1-nov | **Sin trabajo de PWA** — G. González está 100% en el Núcleo PvP del juego |
| Semana 2–8 nov | Proyecto Django + modelo de datos + endpoint `POST /resultados` funcionando — G. González |
| Semana 9–13 nov | Endpoint `GET /ranking` + página web simple con la tabla + desplegar + conectar el juego real (Jesús envía el resultado desde Unity al terminar cada partida) — G. González |
| 17-nov (buffer) | Prueba final de la PWA con datos reales de los playtests |

## Integración con el juego

Cuando termina cada duelo, el juego (vía Jesús, dueño del sistema de puntos) hace un `POST` al endpoint de resultados con el ganador, el perdedor y los puntos de la partida. Esto depende de que el endpoint ya exista — por eso está calendarizado para la semana 6 (9–13 nov), después de que G. González lo construya en la semana 5.

## Por qué quedó así (contexto de la decisión)

En la planeación original (documento de negocio del equipo), la PWA estaba listada como algo a construir **después** del 20-nov. El equipo corrigió esto: el 20-nov es la fecha de entrega de **todo** el proyecto, no solo del juego. Por eso la PWA se adelantó y ahora corre en paralelo al desarrollo del juego, concentrando el trabajo pesado en las semanas donde G. González ya terminó la parte más crítica del Núcleo PvP (después del 1-nov).
