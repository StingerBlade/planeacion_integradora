# 7. App móvil (Flutter)

**Responsable:** Guillermo Martínez (con apoyo de Jesús desde la semana del 2-nov).

**FECHA DE INICIO: 28 de septiembre de 2026.**
**FECHA DE FIN: 13 de noviembre de 2026.**

Ya **no** es un extra post-entrega: se necesita lista, junto con el videojuego, para la presentación del 20-nov.

## Alcance mínimo (MVP)

Una sola pantalla que muestra la tabla de ranking, **sin login ni navegación extra**. Depende de la API de la PWA ([06-pwa.md](06-pwa.md)) para los datos reales, pero arranca antes usando datos de prueba (mock) para no bloquear el desarrollo.

## Calendario

| Cuándo | Qué se hace |
|---|---|
| Ahora (Fase 1, desde 28-sep) | Crear el proyecto Flutter y armar la pantalla de ranking con datos de prueba (mock) — Guillermo Martínez |
| 5-oct al 1-nov | Pulir la interfaz con datos de prueba, sin depender todavía de la PWA real — Guillermo Martínez |
| Semana 2–8 nov | Conectar la pantalla a la API real de la PWA en cuanto G. González la tenga lista — Guillermo Martínez |
| Semana 9–13 nov | Probar con datos reales de partidas y generar un build de prueba (APK) — Guillermo Martínez y Jesús |
| 17-nov (buffer) | Prueba final del app con datos reales de los playtests |

## Por qué arranca antes que la PWA

Guillermo Martínez tiene más disponibilidad (solo PO + audio del juego, ninguna tarea de desarrollo del core), así que construye la interfaz con datos inventados desde la primera semana. Cuando G. González tenga la API real lista (2-nov en adelante), solo falta conectar la pantalla ya construida — esto reduce el riesgo de que ambos equipos (PWA y app) se bloqueen mutuamente cerca de la fecha límite.

## Jesús se suma

Jesús Castilla co-desarrolla la app con Guillermo Martínez, pero solo a partir de la semana del 2-nov — antes de eso está enfocado al 100% en las tareas de IA/detección/puntos del videojuego (ver [04-cronograma-fases.md](04-cronograma-fases.md)).
