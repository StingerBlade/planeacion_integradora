# Backlog del producto (Fases 2-5)

Fuente: lista "📋 Backlog del producto (Fases 2-5)" del tablero de Trello.

## Fase 2 — 5 al 18 oct: Osos y escenario jugable

Dos semanas. Lideran Hugo Baeza y G. González.

El movimiento del oso debe quedar listo para sincronizarse por red en la Fase 3 (Photon PUN2).

Semana 1 (5-11 oct) y Semana 2 (12-18 oct): checklist con la tarea exacta de cada persona por semana (ver tarjeta en Trello).

**Entregable al cierre (18-oct):** oso jugable con animaciones, moviéndose en el escenario de 3 pasillos, con una primera prueba de sincronización en red.

## Fase 3 — 19 oct al 1 nov: Núcleo PvP

Dos semanas. Lideran Dylan Muñoz (red), Jesús Castilla y G. González.

Multiplayer con Photon PUN2. Importante: los NPCs (juguetes de camuflaje) NO se sincronizan por red, cada cliente los simula localmente — solo se sincronizan los 2 jugadores humanos (posición, animación, armas y golpes).

**Fuera del MVP:** el oso "policía" (IA que vigila si se agrede a los NPCs) NO se construye en esta fase. El castigo de -50 puntos por matar a un NPC ya cubre ese propósito. Se revisa solo si sobra tiempo después de tener el MVP completo.

Semana 3 (19-25 oct) y Semana 4 (26 oct-1 nov): checklist con la tarea exacta de cada persona por semana.

**Entregable al cierre (1-nov):** un duelo 1v1 jugable completo ENTRE DOS COMPUTADORAS DISTINTAS conectadas por Photon, aunque se vea sin pulir.

## Fase 4 — 2 al 13 nov: Primera versión jugable

Dos semanas. Dylan programa el HUD y los menús (además de la sala/lobby de Photon); Guillermo Martínez y G. González consiguen e integran música/SFX; el resto integra y corrige bugs.

Guillermo Martínez está dedicado casi de tiempo completo a la app en Flutter y no toma otras tareas del videojuego aparte de audio.

Semana 5 (2-8 nov) y Semana 6 (9-13 nov): checklist con la tarea exacta de cada persona por semana.

**Entregable al cierre (13-nov):** build jugable de principio a fin con HUD, menús, lobby de Photon, NPCs y armas, sin bugs bloqueantes.

## Fase 5 — 14 al 20 nov: Pulido y entrega

Una semana, todo el equipo. Termina viernes 20 de noviembre con la ENTREGA FINAL.

Ver checklist con la secuencia exacta de la semana (en Trello).

## Después del 20-nov: PWA de ranking (Django)

**Responsable:** G. González (API/backend en Django).

Según el propio plan del equipo, la PWA se construye después de entregar el juego. Antes del 20-nov, G. González solo bocetea el esquema de datos (qué guarda cada partida: jugador, resultado, puntos) para no rediseñar nada después, sin que le quite tiempo al Núcleo PvP.

## Después del 20-nov: App móvil (Flutter)

**Responsables:** Guillermo Martínez y Jesús Castilla (ambos desarrollan la app en Flutter).

Arranca de lleno después de entregar el juego (20-nov). Guillermo Martínez sigue siendo el Product Owner formal del proyecto aunque su tiempo de desarrollo esté en Flutter. Jesús mantiene sus tareas del videojuego (NPCs, vida/daño, detección, puntos, documentación) hasta el 20-nov; su parte de Flutter arranca después, igual que la de Guillermo Martínez.

## Después del 20-nov: Publicación en Steam

**Responsables:** Ángel + Dylan (construyen y publican). Guillermo Martínez aprueba como Product Owner antes de publicar.

Cuota de Steam Direct, ficha de tienda, trailer y wishlist. Plan B si algo falla: itch.io. Dylan ya es quien genera el build final de Windows, así que le queda natural encargarse también de subirlo a Steam.

## Fuera del MVP: Oso policía — IA que vigila agresión a NPCs

**Responsable:** Jesús Castilla (cuando se retome).

Del documento original: "la policía del juego es capaz de detectar cuando los NPCs están siendo agredidos". Se descarta del MVP por decisión del equipo (27-sep): el castigo de -50 puntos por matar a un NPC ya desincentiva lastimar inocentes, sin necesitar una IA extra que vigile y reaccione.

Solo se construye si el MVP (Fases 1-5) queda listo con tiempo de sobra antes del 20-nov. Si no, se trata como mejora post-entrega, igual que la PWA y la app de Flutter.

---
[← Sprint Fase 1](03-sprint-fase1.md) · [Siguiente: Hecho →](05-hecho.md)
