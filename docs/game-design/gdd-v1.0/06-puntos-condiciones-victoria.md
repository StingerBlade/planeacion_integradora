# 6. Sistema de puntos y condiciones de victoria/derrota

El Portafolio 1 describía dos reglas de finalización incompatibles (una por tiempo/puntos, otra por eliminación — ver [huecos argumentales](../07-huecos-argumentales.md)). **Confirmado por Guillermo Martínez (Product Owner), con base en la hoja de balance del equipo:** la regla correcta es por puntaje, no por eliminación directa.

**Condición de victoria/derrota (la que se programa).** La partida dura 10-15 minutos y gana quien tenga más puntos al terminar el tiempo. Al ser eliminado, el jugador **respawnea** (vuelve a aparecer) y la partida continúa — no es "una muerte y se acabó". El combate es continuo durante toda la duración de la partida; morir una vez no termina el duelo, solo le cuesta el intento al jugador eliminado (y le da los puntos de la kill al otro).

**Puntaje (decide quién gana la partida):**

| Evento | Puntos |
| --- | --- |
| Kill normal | +200 (eliminación de un oso) |
| Kill con sigilo | +350 (eliminación sin ser visto) |
| Kill con la pistola de dardos | +400 (puntos dobles, definido en U1E4) |
| Matar a un NPC (bot) | –50 (penalización; un bot eliminado resta puntos) |

Al terminar cada partida, el resultado y los puntos se envían a la PWA de estadísticas (**Esencial** desde U1E4). El ranking del jugador (visible en la PWA) también se basa en partidas ganadas y perdidas, además del puntaje por partida.

**Fuente:** hoja de balance ("BEARSTARDS / BASTARDOSOS", infografía de una página) subida por Guillermo Martínez — ver [docs/game-design/assets/hoja-de-balance-bearstards.png](../assets/hoja-de-balance-bearstards.png). Esa misma hoja, en el panel "El oso", todavía dice "su objetivo: ser el último en pie", que es la frase vieja que causaba la confusión con "eliminación" — el panel "Sistema de puntos" (el mismo documento) y la confirmación directa del PO son los que mandan.

> ✅ Esta sección reemplaza la versión anterior de este GDD, que decía "la partida es por eliminación" — esa interpretación era incorrecta. Avisar a quien haya programado o documentado la regla de eliminación en otro lado (Trello, Portafolio 1, repositorio de Unity) para que se actualice.

---
[← Mecánicas principales](05-mecanicas-principales.md) · [Índice GDD](00-indice.md) · [Siguiente: Armas y objetos →](07-armas-objetos.md)
