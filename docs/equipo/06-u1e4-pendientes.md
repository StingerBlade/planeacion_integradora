# U1E4 — Pendientes del entregable académico (Trello)

Fuente: lista "🚀 Sprint actual (Fase 1 · 28 sep-4 oct)", tarjetas con prefijo `[U1E4]`. Son tareas nuevas encontradas al revisar el tablero (no estaban cuando se escribió el resto de esta documentación). "U1E4" parece ser la cuarta entrega de la Unidad 1 del curso.

## [U1E4] (PO) Confirmar condición de victoria única — ✅ resuelta

**Responsable:** Product Owner (Guillermo Martínez). Apoya: Scrum Master (Ángel Arras) agenda el espacio en Sprint Review.

**Qué faltaba:** el Portafolio 1 se contradice (victoria por eliminación vs. victoria por temporizador/puntos — ver [huecos argumentales](../game-design/07-huecos-argumentales.md)).

**Decisión confirmada por el PO (con la hoja de balance del equipo):**
- [x] Gana quien tenga más puntos al agotarse el temporizador de 10-15 min — **no** es por eliminación directa.
- [x] Al ser eliminado, el jugador respawnea y la partida continúa; morir no termina el duelo.
- [x] Confirmar que se descarta el oso policía (sigue vigente, solo queda la penalización de -50 puntos).

Ver la regla completa en [GDD v1.0 · Sección 6](../game-design/gdd-v1.0/06-puntos-condiciones-victoria.md). Pendiente: registrar esta decisión como comentario en la tarjeta de Trello correspondiente, con fecha, para cumplir el criterio de terminado original de la tarjeta.

## [U1E4] (PO) Priorizar tabla "Alcance del proyecto" (Esencial / Deseable)

**Responsable:** Product Owner. Apoyan: Developers y Scrum Master.

**Qué falta:** el documento U1E4 exige una tabla final "Alcance del proyecto" (Elemento | Descripción | Prioridad | Criterio de terminado) que hoy no existe en ningún documento.

**Propuesta de prioridad (pendiente de que el PO la apruebe o corrija):**

| Esencial (sin esto el juego no cumple su propuesta) | Deseable (solo después de que funcione el núcleo) |
| --- | --- |
| Movimiento y cámara del jugador | Pistola de dardos, ratoneras explosivas, lanzallamas, trampa de ratones |
| Mapa La Juguetería (3 pasillos) con colisiones | Casco / atributos armadura, fuerza y relleno |
| Multijugador 1v1 en línea (Photon PUN2) | Puntaje y ranking, PWA |
| NPCs con IA simple y camuflaje | Voces, música original, ragdoll avanzado |
| Sistema de vida + golpe crítico a la cabeza (oneshot/respawn) | Segundo nivel (oficina) |
| Victoria por puntaje al agotar el temporizador (con respawn) | Modo local de respaldo (Plan B de Photon) |
| Mínimo 2 armas (aguja de coser + una de distancia) | |
| 1 curación (rollo de hilo) y HUD básico | |

**Decisión requerida:** el PO marca cada elemento como Esencial o Deseable, y confirma si Photon se queda como Esencial (riesgo del multijugador).

## [U1E4] (PO) Cerrar lista definitiva de armas, objetos y vestimenta

**Responsable:** Product Owner. Apoya: Scrum Master (documenta la decisión).

**Qué falta — los documentos del equipo no coinciden:**
- Portafolio 1 menciona "pistola de juguete" y el GDD "pistola de dardos con tachuelas": ¿son la misma arma?
- Casco (power-up de armadura): aparece solo en un lugar; ¿entra al juego?
- Resortes: estaban en la lluvia de ideas original y desaparecieron; ¿se descartan?
- Agujas de coser: ¿arma blanca básica o utilitaria?
- Daño por desmembramiento (lluvia de ideas): ¿se descarta?
- Oficina de la tienda ("probable" en el Portafolio 1): ¿segundo nivel o fuera de alcance?
- Vestimenta: hoy solo dice "marcas parodia". ¿Se describe (accesorios, casco) o se declara "No aplica" con justificación?

**Decisión requerida:** lista cerrada de armas (tipo, daño, alcance, munición), lista cerrada de objetos especiales (efecto), vestimenta descrita o "No aplica" justificada, confirmar un solo mapa en el MVP.

## [U1E4] (SM) Redactar secciones 1-8 del documento de diseño

**Responsable:** Scrum Master (Ángel Arras). Las decisiones de contenido vienen de las tres tarjetas del PO de arriba; aquí solo se redacta.

**Pendiente frente a la rúbrica U1E4** (base: GDD v1.0 + Portafolio 1):
- [ ] Género: justificar con texto ya existente en el Portafolio 1.
- [ ] Público objetivo: agregar experiencia previa del jugador y tipo de experiencia (hoy solo dice +13, PC, 10-15 min).
- [ ] Historia: ya completa, solo transferir.
- [ ] Personajes: agregar interacciones principales (jugador vs. rival, jugador vs. NPC) y qué hace cada atributo.
- [ ] Niveles: con un solo mapa, definir propósito, retos y progresión (fases/rondas dentro de la partida).
- [ ] Armas: separar de los objetos; agregar comportamiento, daño, alcance.
- [ ] Vestimenta: según lo que decida el PO.
- [ ] Objetos especiales: separar de las armas; detallar efecto, duración, cantidad.

## [U1E4] (SM) Portada, tabla de alcance y exportar PDF final

**Responsable:** Scrum Master (consolida y entrega); el PO aprueba el contenido.

**Pendiente:**
- [ ] Portada con nombre del videojuego y del equipo e integrantes.
- [ ] **Unificar nombre:** el GDD dice "Little Bearstards / Bastardosos" y el grupo se identifica como "**Turbo Studios**". *(Confirmado por Ángel: el equipo es Turbo Studios, el juego es Little Bearstards — sigue pendiente decidir si el PDF usa un solo nombre para todo o los mantiene separados.)*
- [ ] Tabla final "Alcance del proyecto" con las prioridades que apruebe el PO.
- [ ] Quitar del documento lo que no es evidencia de diseño (riesgos, fechas, Trello).
- [ ] Verificar que todo se plantea con vista a implementarse en Unity.
- [ ] Exportar a PDF con nombre `U1E4_NombreDelEquipo.pdf` (ej. `U1E4_TurboStudios.pdf`).

## [U1E4] (SM) Confirmar rúbrica y entregables con la profesora

**Responsable:** Scrum Master.

**Pendiente:**
- [ ] Obtener la rúbrica de U1E4 y compartirla al equipo.
- [ ] Confirmar con la profesora si el GDD y Trello cuentan como evidencia oficial (relacionado con [decisiones urgentes](02-decisiones-urgentes.md), vencía el 30-sep).
- [ ] Confirmar fecha límite exacta de U1E4 y modalidad de entrega.
- [ ] Agendar en Sprint Review el espacio para que el PO apruebe las tres tarjetas de arriba.
- [ ] Decidir si el modo local de respaldo (Plan B de Photon) entra como Deseable en la tabla de alcance.

---
[← Hecho](05-hecho.md) · [Índice general](../game-design/00-indice.md)
