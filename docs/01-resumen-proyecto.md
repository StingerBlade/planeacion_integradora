# 1. Resumen del proyecto

## Qué es

Proyecto integrador del equipo **Turbo Studios**. El videojuego se llama **Little Bearstards** (alterno: *Bastardosos*) — PC, género **Stealth PvP con deducción social y acción**, hecho en **Unity (C#)**, con arte 3D en **Blender**.

- **Jugadores:** 2 (duelo 1 vs 1).
- **Duración de partida:** 10–15 minutos.
- **Público objetivo:** jugadores +13 años.
- **Multiplayer:** en línea, vía **Photon PUN2**.
- **Mapa:** un único escenario, "La Juguetería", dividido en 3 pasillos.

## Premisa (resumen)

Una juguetería en transición a tienda de videojuegos está por cerrar. En el último pasillo quedan los últimos osos de peluche sin vender; de noche cobran consciencia y descubren que serán incinerados si no son vendidos antes del cierre. Dos de ellos deciden eliminarse entre sí para ser el único superviviente y así ser comprados. Las armas están repartidas por los pasillos; los jugadores pueden mezclarse entre NPCs (otros juguetes) para ocultar su identidad.

Ver el detalle completo en [05-gdd-v1.md](05-gdd-v1.md).

## Equipo (6 personas)

| Nombre | Rol Scrum | Área técnica principal |
|---|---|---|
| **Angel David Arras Orozco** | Scrum Master | Coordinación, backlog operativo (cubre al PO), GDD, audio |
| **Guillermo Martínez (Delgadillo)** | Product Owner | App móvil en Flutter (con Jesús), música/SFX |
| **Víctor Hugo Baeza Rocha** | Developer | Arte 3D, animación, VFX |
| **Ángel Guillermo González Gómez** | Developer | Gameplay y arquitectura del videojuego; backend/API de la PWA en Django; música/SFX |
| **Jesús Arturo Castilla González** | Developer | IA/NPCs, detección y puntos; documentación técnica; co-desarrollo de la app Flutter |
| **Dylan Muñoz Flores** | Developer (Lead técnico de integración y red) | Photon, sincronización, integración de sistemas, build final, HUD/menús, Steam (post-entrega) |

Asesoras: Prof. Blanca Chavarría / Prof. Mascote (UTCH, IDGS101N).

## Fechas clave

| Fecha | Qué pasa |
|---|---|
| 21–27 sep 2026 | Arranque / planeación inicial (Fase 1 original) |
| 28 sep – 4 oct 2026 | Sprint actual: cierre de Fase 1 |
| **13 de noviembre de 2026** | **Todo feature-complete**: juego + PWA + app Flutter |
| 14–20 de noviembre de 2026 | **Semana de colchón** (pruebas, bugs, pulido, ensayo — sin features nuevas) |
| **20 de noviembre de 2026 (viernes)** | **ENTREGA FINAL** de todo el proyecto |
| Después del 20-nov | Publicación en Steam (fuera del alcance de la entrega) |

## Plataformas y stack técnico

- **Juego:** Unity, C#, Blender, Photon PUN2 (multiplayer online).
- **PWA de ranking:** Django (Python).
- **App móvil:** Flutter (Dart).
- **Gestión del proyecto:** Trello (tablero "Little Bearstards - Proyecto Integrador").
- **Control de versiones:** Git + GitHub (se evaluó Plastic/Unity Version Control y se descartó el cambio por tiempo; ver [09-repositorio-ci-cd.md](09-repositorio-ci-cd.md)).
