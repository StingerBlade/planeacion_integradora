# Sprint actual: Fase 1 (28 sep – 4 oct)

Fuente: lista "🚀 Sprint actual (Fase 1 · 28 sep-4 oct)" del tablero de Trello. Todas vencen el 4-oct.

## Ángel Arras (SM) — GDD v1 y coordinación

Rol: Scrum Master.

Entregable: GDD v1.0 (duelo 1v1 EN LÍNEA vía Photon PUN2, mapa de 3 pasillos, NPCs de camuflaje simulados localmente en cada cliente, SIN oso policía en el MVP) y ceremonias de la semana agendadas.

> El contenido completo de este GDD v1.0 ya está desarrollado en [docs/game-design/gdd-v1.0/](../game-design/gdd-v1.0/00-indice.md) y también se actualizó directamente en esta tarjeta de Trello.

## Guillermo Martínez (PO) — Balance y backlog

Rol: Product Owner.

Entregable: hoja de balance cerrada y backlog de la Fase 2 priorizado en el tablero.

> **Entregada.** La hoja de balance es la infografía de una página "BEARSTARDS/BASTARDOSOS" — ver [docs/game-design/assets/hoja-de-balance-bearstards.png](../game-design/assets/hoja-de-balance-bearstards.png). De ahí sale el sistema de puntos confirmado en [GDD v1.0 · Sección 6](../game-design/gdd-v1.0/06-puntos-condiciones-victoria.md). En Trello la tarjeta aparece asignada a "Joel Ardido Nuñez" — es la cuenta de Google de Guillermo Martínez, no un integrante nuevo.

## Hugo Baeza — Concept art y escenario

Rol: Modelado 3D.

Entregable: guía de estilo low poly aprobada y boceto del escenario de 3 pasillos.

## G. González — Arquitectura del proyecto Unity

Rol: Desarrollo.

Entregable: repositorio de GitHub listo, con carpetas, prefabs y convención de commits definidos. Nota: los prefabs de jugador deben quedar preparados para instanciarse en red más adelante (carpeta `Resources`, que es lo que pide `PhotonNetwork.Instantiate`).

> **Tarea adicional agregada hoy (4-oct), a petición propia:** arrancar el HUD de vida (barra) y el feedback visual al recibir daño — la parte de lógica/datos. Pidió explícitamente que alguien más se encargue del diseño visual del HUD (botones, layout), ya que él no hace diseño; esa parte se le asignó a Dylan (ver abajo).

## Jesús Castilla — Prototipo de NPC

Rol: Desarrollo (IA).

Entregable: prototipo de NavMesh con un NPC que patrulla, sin arte final.

## Dylan Muñoz — Configurar Photon PUN2

Rol: Desarrollo (red).

Entregable: cuenta de Photon creada, SDK de PUN2 importado, 2 instancias conectadas a una sala de prueba, y un prototipo mínimo donde un objeto placeholder se mueve sincronizado entre las 2 instancias (PhotonView + PhotonTransformView). Documentar en 1 página cómo usar PhotonView/RPCs para el equipo, y apoyar a G. González con la arquitectura del repo para que los prefabs queden listos para instanciarse en red.

> ⚠️ **Esta tarea terminó resuelta por G. González**, no por Dylan — la tarjeta de Trello aparece completa pero con G. González como miembro. Dylan no tuvo participación activa en esta fase, y tampoco tiene cuenta en el tablero de Trello.

## Dylan Muñoz — Diseño del HUD (tarea nueva, agregada hoy 4-oct)

Rol: Desarrollo (red / integración).

Entregable: diseño visual del HUD — botones, layout de la barra de vida, temporizador y puntos en pantalla. Es la contraparte de diseño/UI del HUD funcional que ya construye G. González (datos/lógica). Decidido en el chat del equipo: como Dylan ya tenía contemplado el HUD completo más adelante (Fase 4, Semana 5), tiene sentido que adelante la parte visual ahora. Se le asigna explícitamente para que empiece a aportar al equipo.

---
[← Decisiones urgentes](02-decisiones-urgentes.md) · [Siguiente: Backlog Fases 2-5 →](04-backlog-fases-2-5.md)
