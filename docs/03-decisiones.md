# 3. Decisiones (tomadas y pendientes)

Tomado de la lista **🔴 Decisiones urgentes** y de la tarjeta **✅ Hecho** en Trello.

## Decisiones ya tomadas (resueltas)

### [RESUELTO] 1v1 en línea con Photon PUN2

El equipo usará **Photon PUN2** para el multiplayer en línea. Se descartaron: LAN, Steam Relay (Steam Datagram Relay / Steamworks Networking) y peer-to-peer manual.

**Motivo:** paquete oficial para Unity con componentes listos (`PhotonView`, RPCs), capa gratuita suficiente (20 CCU) para el proyecto, y no depende de que los jugadores tengan Steam abierto ni de estar en la misma red física.

**Comparativa que se evaluó:**

| Opción | Dificultad real | Veredicto |
|---|---|---|
| 1v1 en la misma PC (sin red) | Muy baja | La más simple, pero el equipo decidió ir por online real |
| **Photon PUN2** | Media | **Elegida** — paquete oficial, free tier, sin depender de Steam ni de LAN |
| Steam Relay (SDR) | Media, más fricción inicial | Gratis sin tope, pero requiere Steam abierto en cada prueba |
| LAN (misma red física) | Media-alta para este equipo | Mismo nivel de código que Photon pero obliga a estar en la misma red para probar — malo para trabajo remoto |
| Peer-to-peer manual | Alta | Descartado — semanas de trabajo solo en la capa de red |

**Impacto en el plan:** las tareas de la Fase 3 (Núcleo PvP) se reescribieron para trabajo en red. **Los NPCs de camuflaje NO se sincronizan por red** — cada cliente los simula de forma local e independiente; solo se sincronizan los 2 jugadores humanos (posición, animación, armas y golpes).

### Marcas de los osos y tipografía

**Responsable:** Angel + Hugo Baeza. *(Completada.)*

Usar marcas parodia u originales en los osos, no marcas reales (riesgo legal si se publica el juego). Revisar la licencia de Comic Sans; alternativa libre casi idéntica: **Comic Neue**.

## Decisiones pendientes (con fecha límite)

### Confirmar entregables oficiales con la profesora

**Responsable:** Angel + Guillermo Martínez. **Fecha límite:** 30-sep-2026.

Preguntar a la Prof. Chavarría / Prof. Mascote si piden un formato específico de organigrama, acta, memoria o presentación, y si el tablero de Trello (y este documento) cuentan como evidencia de gestión del proyecto.

### Plan B si falla Photon en la presentación en vivo

**Responsable:** Angel + Dylan. **Fecha límite:** 13-nov-2026 (cierre de Fase 4).

Con multiplayer en línea, hay riesgo de que el día de la entrega falle el internet del salón, el Wi-Fi de alguna PC, o el servicio de Photon. Un demo en vivo que no conecta frente al docente es el peor escenario.

Opciones a decidir:
- Video de respaldo grabado de una partida completa, listo para mostrar si falla la conexión en vivo.
- Y/o un modo de práctica local mínimo (contra un NPC simple) solo para poder mostrar las mecánicas si el online no conecta.

Ensayar la conexión real varios días antes, no el mismo día de la entrega (ver [10-semana-colchon.md](10-semana-colchon.md), ítems del 17 y 19 de noviembre).

### Steam, ¿debe estar listo para el 20-nov?

**Resuelto por recomendación del Scrum Master (28-sep):** NO. Steam se queda fuera del 20-nov. Razones:
1. Cuesta 100 USD reales — hay que decidir gastarlo, no es solo trabajo.
2. Valve revisa manualmente antes de publicar (Steam Direct); el tiempo de revisión no lo controla el equipo.
3. Lo que probablemente califica la profesora es que el juego, la PWA y el app funcionen, y que la estrategia de Steam esté bien explicada en la presentación de negocio (ya existe en el pitch deck) — no que exista una tienda real y pagada.

Para la entrega del 20-nov se distribuye el build por **itch.io** o un link de descarga directo (el "Plan B" que el equipo ya tenía contemplado en su documento de negocio).

## Decisiones de diseño incorporadas al GDD (ver documento completo)

- **Condición de victoria:** la partida dura 10-15 min y **gana quien tenga más puntos** al agotarse el tiempo; al morir, el jugador respawnea y el combate continúa (no es muerte súbita). Confirmado por Guillermo Martínez (PO) con la hoja de balance del equipo — ver [05-gdd-v1.md · Sección 6](05-gdd-v1.md#6-puntos-y-condiciones-de-victoriaderrota). Esto resuelve una contradicción entre los documentos originales del equipo (uno hablaba de "gana quien tenga más puntos al final del tiempo", otro de "ser el último en pie") a favor de la primera versión.
- **Oso "policía" (IA que vigila agresión a NPCs):** descartado del MVP. Ver [08-post-entrega-y-fuera-del-mvp.md](08-post-entrega-y-fuera-del-mvp.md).
