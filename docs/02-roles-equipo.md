# 2. Roles del equipo

Tomado de las tarjetas de referencia en Trello, lista **📖 Roles del equipo**.

## Product Owner — Guillermo Martínez

Qué hace un Product Owner en este proyecto:

- Es dueño del backlog: decide el orden de prioridad de las tarjetas en "Backlog del producto".
- Define y comunica la visión del producto: qué es el MVP y qué queda fuera (ver [08-post-entrega-y-fuera-del-mvp.md](08-post-entrega-y-fuera-del-mvp.md)).
- Escribe y afina los criterios de aceptación de las historias/tarjetas antes de que se programen.
- Acepta o rechaza el trabajo terminado en cada Sprint Review (los viernes).
- Gestiona el alcance: si algo se atrasa, decide qué se recorta primero (ver la lista MoSCoW del GDD) en vez de mover la fecha de entrega.
- Es el punto de contacto del equipo con la profesora/asesores para dudas de requisitos.

**Importante:** este rol sigue siendo de Guillermo Martínez independientemente de en qué esté trabajando como desarrollador. Actualmente él también:
1. Desarrolla la app en Flutter junto con Jesús Castilla — debe estar lista para el 13-nov, junto con todo lo demás, ya que el 20-nov es la entrega de TODO (juego + PWA + app).
2. Consigue/integra música y SFX del videojuego junto con G. González.

Angel (Scrum Master) cubre el trabajo operativo diario del backlog (refinar tarjetas, bocetos, criterios de aceptación, playtests) mientras Guillermo Martínez está ocupado, pero las decisiones finales de alcance y prioridad las sigue validando él como Product Owner.

## Scrum Master — Angel Arras

Qué hace un Scrum Master en este proyecto:

- Facilita las ceremonias: planning (lunes), daily (15 min), refinamiento (miércoles), review (viernes) y retrospectiva (viernes).
- Quita impedimentos: si alguien está bloqueado, ayuda a resolverlo o lo escala.
- Mantiene el tablero de Trello al día y vigila que nadie tenga más de 2 tarjetas en progreso a la vez.
- Protege al equipo de meter más alcance del que cabe en el tiempo (evita "cosas imposibles").
- Desde el 27-sep también cubre el trabajo operativo diario del Product Owner mientras Guillermo Martínez está en Flutter: refinar backlog, bocetos, criterios de aceptación y preparar playtests.

## Developers — Hugo, G. González, Jesús, Dylan

Qué hace el equipo de desarrollo en Scrum:

- Se compromete con el trabajo del sprint en el planning y lo cumple.
- Estima y divide las tareas de sus tarjetas.
- Avisa en el daily si algo lo está bloqueando (no espera hasta el review).
- Revisa el trabajo de otro compañero antes de moverlo a "Hecho" (pull request o prueba cruzada).

### Áreas fijas (actualizado 28-sep-2026)

- **Hugo:** arte 3D (oso, armas, props, escenario), animaciones, VFX.
- **G. González:** gameplay y arquitectura del videojuego; API/backend de la PWA en Django (listo para el 13-nov); música/SFX junto con Guillermo Martínez.
- **Jesús:** NPCs con NavMesh, vida/daño/respawn, detección y puntos; documentación técnica; co-desarrolla la app en Flutter con Guillermo Martínez (listo para el 13-nov).
- **Dylan (Lead técnico de integración y red):** configura y mantiene Photon, sincronización, integración de todos los sistemas, build final, HUD y menús, y además la publicación en Steam (**confirmado:** se queda fuera del 20-nov, se hace después de la entrega, junto con Angel).

### Nota sobre carga de trabajo (riesgo, señalado por el Scrum Master)

- **G. González** termina cargando gameplay + arquitectura + backend de la PWA + audio — es mucho para una sola persona, aunque la parte de PWA cae después del cierre de la Fase 3 (1-nov), así que no choca con el núcleo del juego.
- **Dylan** y **Angel** cargan bastante en las semanas 5–6 (2–13 nov): Dylan con red + HUD + menús + integración; Angel con backlog + audio + coordinación. Si algo se atrasa ahí, lo primero que se recorta es el pulido de audio, no las fechas.

## Historial de cambios de roles (por qué quedó así)

1. Versión original del Portafolio 1: Angel = Product Owner, Guillermo Martínez = Scrum Master.
2. Corrección (documento "Little Bearstards — Idea de negocio"): se invirtió — **Guillermo Martínez = Product Owner, Angel = Scrum Master**. Esta es la versión vigente.
3. Guillermo Martínez se dedicó casi de tiempo completo al desarrollo de Flutter → Angel absorbió el trabajo operativo diario del PO (backlog, bocetos, criterios de aceptación, preparar playtests).
4. La música/SFX, que iba a ser de Angel, se reasignó a **Guillermo Martínez y G. González** a petición explícita del equipo.
5. Jesús se sumó como co-desarrollador de Flutter junto con Guillermo Martínez.
6. El backend/API de la PWA pasó de Dylan a **G. González**.
7. A Dylan se le dio más peso (sin quitarle nada de lo que ya tenía): título de "Lead técnico de integración y red" + responsabilidad de publicar en Steam.
