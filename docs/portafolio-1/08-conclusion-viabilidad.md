# 8. Conclusión y viabilidad

Transcripción de la sección 8 del Portafolio 1.

Consideramos que el proyecto "Little Bearstards" es viable dentro del tiempo disponible (23 de septiembre al 20 de noviembre) porque el alcance está bien acotado desde la fase de concepción: un solo escenario dividido en tres pasillos, una mecánica central definida (stealth PvP con sistema de detección) y un catálogo cerrado de armas y objetos, lo que evita tener que expandir contenido sobre la marcha. A esto se suma una planificación semanal con hitos concretos y responsables asignados a cada tarea, un equipo de seis integrantes con roles definidos bajo la metodología Scrum, y el apoyo de herramientas de gestión como Trello, Jira y Git/GitHub para dar seguimiento al avance. El uso de recursos externos gratuitos (animaciones de Mixamo, assets 3D del Unity Asset Store) también reduce la carga de producción de arte original y libera tiempo para la programación.

Sin embargo, identificamos varios riesgos que podrían comprometer la entrega:

- **Riesgos técnicos:** el sistema multijugador (sincronización PvP en tiempo real) es la parte más compleja del desarrollo y recae en solo tres integrantes, lo que puede convertirse en un cuello de botella si surgen problemas de latencia o sincronización. De forma similar, el sistema de detección e IA de comportamiento de los NPCs no es trivial de depurar, y los ajustes de rendimiento (animaciones tipo ragdoll, físicas, modelos 3D) suelen manifestarse tarde en el desarrollo, dejando poco margen de corrección antes de la fecha límite.
- **Riesgos de organización:** la carga de trabajo no está distribuida de manera uniforme; el grueso de la programación y el modelado recae en dos o tres personas, mientras que el resto del equipo participa principalmente en las etapas iniciales y finales. Además, existen dependencias secuenciales estrictas (la programación no puede avanzar sin los modelos 3D terminados), por lo que un retraso en una fase temprana se propagaría a todo el cronograma restante.
- **Riesgos de alcance:** elementos como la pistola especial, las trampas explosivas, la música original y el pulido visual podrían quedar incompletos o simplificarse si el tiempo se agota, ya que el núcleo jugable (movimiento, combate y condiciones de victoria/derrota) debe tener prioridad sobre los elementos secundarios.

El cronograma propuesto es alcanzable siempre que el equipo mantenga revisiones semanales bajo Scrum, detecte a tiempo cualquier atraso en las tareas dependientes y priorice las mecánicas núcleo del PvP y el sigilo por encima de elementos decorativos en caso de que el tiempo se ajuste. La mayor amenaza para la entrega no es la idea del juego en sí —que está bien delimitada— sino la ejecución técnica del componente multijugador y la corrección oportuna de errores antes de la fecha de entrega final.

> Esta autoevaluación de riesgos del propio equipo coincide con los huecos detectados en [docs/game-design/07-huecos-argumentales.md](../game-design/07-huecos-argumentales.md): el riesgo técnico de "sincronización PvP" es justo el motivo por el que conviene cerrar ya la decisión local-vs-online (ver [GDD v1.0 · Riesgos pendientes](../game-design/gdd-v1.0/11-riesgos-pendientes.md)).

---
[← Pruebas](07-pruebas.md) · [Índice Portafolio 1](00-indice.md)
