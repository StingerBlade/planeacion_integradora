# Histórico de sprints

Registro de lo que se logró en cada sprint, tomado del tablero de Trello (**Little Bearstards - Proyecto Integrador**) y de los repositorios. Se agrega una sección por sprint al cerrarlo; el sprint en curso se actualiza en cada review.

*Última actualización: 9-oct-2026.*

---

## Sprint 1 — Fase 1: Diseño y escenario (28-sep al 4-oct)

**Meta:** GDD v1, repositorio Unity listo, concept art, prototipo de NPC y de conexión Photon.

### Qué se logró

**Decisiones de producto y técnicas**
- Se decidió usar **Photon PUN2** para el 1v1 en línea (27-sep); se descartaron LAN, Steam Relay y P2P manual. Los NPCs de camuflaje se simulan localmente en cada cliente; solo se sincronizan los 2 jugadores.
- Se definieron las **marcas parodia** de los osos y la tipografía (alternativa libre a Comic Sans: Comic Neue) — decisión cerrada el 1-oct.
- Se confirmó la **condición de victoria única: por puntaje con respawn** (kill +200, kill sigiloso +350, matar NPC −50). Se descartó el oso policía del MVP.
- Se cerró la lista de armas, objetos y vestimenta, y la tabla de alcance Esencial/Deseable. El modo local de respaldo (Plan B de Photon) entra como Deseable.
- Ajuste de balance de la pistola de dardos (4-oct): 50 de daño por dardo (2 impactos para eliminar, 3 con casco); el golpe a la cabeza sigue siendo oneshot.

**Entregables del equipo**
| Responsable | Entregable | Estado |
|---|---|---|
| Ángel Arras (SM) | GDD v1.0 completo y ceremonias agendadas | ✅ Hecho |
| Guillermo Martínez (PO) | Hoja de balance "BEARSTARDS/BASTARDOSOS" cerrada y backlog de la Fase 2 priorizado (6-oct) | ✅ Hecho |
| Guillermo Martínez (PO) | Proyecto Flutter creado con pantallas de ranking con datos de prueba (hito del 28-sep, cerrado el 9-oct) | ✅ Hecho |
| G. González | Arquitectura del proyecto Unity (repo, carpetas, prefabs, convención de commits) | ✅ Hecho |
| G. González | Inicio del HUD de vida y feedback de daño (tarea adicional del 4-oct) | ✅ Hecho (5-oct) |
| Jesús Castilla | Prototipo de NPC con NavMesh que patrulla | ✅ Hecho |
| Configurar Photon PUN2 | Cuenta, SDK e instancias conectadas, prototipo sincronizado | ✅ Hecho (resuelto por G. González, no por Dylan) |

**Documento de diseño U1E4 (entrega académica, 15 %)**
- Secciones 1–8 redactadas, portada, tabla de alcance y PDF `U1E4_TurboStudios.pdf` preparado para Moodle (fecha límite 4-oct, 23:59).
- Versión en presentación de 16 diapositivas, con el ajuste de la pistola incorporado (PR #9).
- Tarjetas `[U1E4]` de SM y PO movidas a Hecho.

**Repositorios**
- `planeacion_integradora`: documentación completa en `docs/` (GDD, roles, cronograma, PWA, Flutter, CI/CD, semana de colchón, U1E4). 9 PRs integrados a `main`.
- `BEARSTARDS_PWA`: repositorio creado el 6-oct; proyecto base React + Vite con plugin PWA (7 al 9-oct).

### Qué NO se logró / se arrastra al Sprint 2
- **Concept art y escenario** (Hugo Baeza): guía de estilo low poly y boceto de los 3 pasillos — la tarjeta sigue abierta en "Sprint actual".
- **Diseño visual del HUD** (Dylan Muñoz): fecha límite movida al 11-oct; sigue abierta.
- **Confirmar rúbrica y entregables con la profesora**: rúbrica sin publicar al 4-oct; falta confirmar si el GDD y Trello cuentan como evidencia oficial de gestión.
- **Plan B si falla Photon** en la presentación: decisión abierta, fecha límite 13-nov.
- **Documentación de Photon** en 1 página (PhotonView/RPCs) — no hay evidencia de que se haya entregado.

### Discrepancias detectadas en Trello (para corregir)
- La tarjeta `[Fase 1] Configurar Photon PUN2` está completa, pero sus dos items de checklist aparecen sin marcar.
- Las tarjetas de Fase 1 se movieron a Hecho el 9-oct, después del cierre del sprint (4-oct): las fechas de cierre reales no reflejan cuándo se terminó el trabajo.
- La tarjeta `[U1E4] (PO) Confirmar condición de victoria…` está en Hecho pero sin marcar como completa.
- Dylan Muñoz sigue sin cuenta en Trello.

---

## Sprint 2 — Fase 2: Osos y escenario jugable (5 al 18-oct) — EN CURSO

**Meta:** oso jugable con animaciones en el escenario de 3 pasillos, con primera sincronización en red probada.

Backlog priorizado por el PO (línea de corte tras F2-06):

| ID | Prioridad | Historia |
|---|---|---|
| F2-01 | MUST | Mover al oso por la juguetería |
| F2-02 | MUST | Movimiento sincronizado entre 2 PCs (Photon) |
| F2-03 | MUST | Escenario de 3 pasillos navegable |
| F2-04 | MUST | Cámara en tercera persona |
| F2-05 | MUST | Oso final con animaciones (idle, correr, saltar) |
| F2-06 | MUST | Dos esquemas de control (**pendiente de definir**) |
| F2-07 | SHOULD | Modelos de aguja y rollo de hilo |
| F2-08 | SHOULD | Animación de golpear |
| F2-09 | COULD | Modelos de pistola de dardos y casco |
| F2-10 | COULD | Iluminación y ambientación |
| F2-11 | COULD | Boceto de la pantalla de resultado |

**Avance al 9-oct:** ninguna tarjeta F2 se ha movido a Hecho todavía. Review del sprint: 18-oct.

**Fuera del plan original pero avanzado:** el proyecto de la PWA (React + Vite + PWA plugin) y el proyecto Flutter ya arrancaron, antes del 2-nov previsto para la PWA.

---
[← Hecho](05-hecho.md) · [Índice general](../game-design/00-indice.md)
