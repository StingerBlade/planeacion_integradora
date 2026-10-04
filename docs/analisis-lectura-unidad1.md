# Análisis: lectura de Moodle (Unidad 1) vs. plan del equipo

Comparación hecha al inicio de este trabajo entre los contenidos de Moodle de la Unidad 1 del curso "Creación de Videojuegos" (lecturas "De la idea al concepto", "Historia y estructura narrativa", "Causa, consecuencia y progresión narrativa", "Cómo encontrar huecos argumentales" y sus actividades prácticas) y lo que ya estaba planeado por el equipo en Trello, antes de tener acceso al Portafolio 1.

## Lo que sí estaba cubierto en Trello (en ese momento)

- GDD v1 en construcción (Fase 1, responsable Ángel Arras, vence 4-oct).
- Concept art / guía de estilo / escenario (Hugo Baeza).
- Arquitectura del proyecto Unity, prototipo NPC, configuración Photon PUN2.
- Roles del equipo, hitos, decisiones urgentes, backlog de fases 2-5.

## Huecos detectados en ese momento (antes de leer el Portafolio 1)

1. **No había ninguna tarjeta de trabajo narrativo/preproducción visible en Trello**, que es justo el tema de la lectura: premisa y sinopsis, cadena causal, beat sheet, matriz de información, ficha de concepto v0.1/v0.2 y pitch, verbos del jugador. *(Al revisar después el Portafolio 1 se confirmó que este trabajo sí existía — ver [docs/game-design/](game-design/00-indice.md) — solo no estaba reflejado en Trello.)*
2. **Entregables calificables de Moodle que no se veían reflejados como tarjetas/tareas en Trello:**
   - Documento técnico de requerimientos de hardware/software (assign 3212).
   - Reporte de investigación de clasificación de videojuegos (assign 4474).
   - Cuadro de comparación de clasificación (workshop 4475).
   - El Documento de diseño final (assign 4479) pide explícitamente: género, público objetivo, historia, personajes, niveles, armas, vestimenta y objetos especiales — en ese momento el GDD planeado en Trello no mencionaba historia/personajes/vestimenta, solo mecánica y balance. *(Resuelto: el [GDD v1.0](game-design/gdd-v1.0/00-indice.md) ya cubre los siete elementos.)*
3. **Detalle de redacción a vigilar:** el assign 4478 pide describir el proceso usando "assets, sprites y tiles", lenguaje típico de un juego 2D, pero el proyecto es 3D low-poly (oso 3D, props, animaciones). No es un error del plan, pero al redactar ese entregable conviene traducir la terminología (assets 3D, prefabs, etc.) para que calce con lo que pide la rúbrica. *(El propio Portafolio 1 ya responde "no aplican los sprites en este proyecto" y describe tiles solo para UV maps — ver [docs/portafolio-1](portafolio-1/06-desarrollo.md).)*
4. **No se veía el "público objetivo" definido en ningún lado** (ni edad, ni experiencia previa esperada, ni sesión casual/exigente). *(Resuelto: Portafolio 1 lo define como "jugadores mayores de 13 años" — ver [GDD v1.0 · Público objetivo](game-design/gdd-v1.0/03-publico-objetivo.md).)*

## Estado actual

Con acceso al Portafolio 1 completo, la mayoría de estos huecos ya estaban resueltos en un documento que no se había compartido en Trello. El trabajo de esta sesión consistió en:

1. Confirmar y corregir la ficha de concepto/beat sheet con el lore real (ver [docs/game-design/](game-design/00-indice.md)).
2. Detectar una contradicción real que el propio Portafolio 1 nunca resolvió: dos condiciones de victoria distintas en secciones distintas del mismo documento (ver [docs/game-design/07-huecos-argumentales.md](game-design/07-huecos-argumentales.md)).
3. Construir el GDD v1.0 definitivo resolviendo esa contradicción y las demás decisiones pendientes (local vs. online, oso policía) — ver [docs/game-design/gdd-v1.0/](game-design/gdd-v1.0/00-indice.md).
4. Transcribir a Markdown las secciones del Portafolio 1 que no estaban en el GDD (planificación, desarrollo, pruebas, conclusión y viabilidad) — ver [docs/portafolio-1/](portafolio-1/00-indice.md).
5. Documentar el contexto completo de Trello (roles, hitos, decisiones urgentes, backlog) — ver [docs/equipo/](equipo/00-roles.md).

---
[← Índice general](game-design/00-indice.md)
