# 6. Sistema de puntos y condiciones de victoria/derrota

El Portafolio 1 describía dos reglas de finalización incompatibles (una por tiempo/puntos, otra por eliminación — ver [huecos argumentales](../07-huecos-argumentales.md)). Este GDD fija una sola regla:

**Condición de victoria/derrota (la que se programa).** La partida es por eliminación: gana el jugador que elimina al rival; termina en cuanto uno de los dos jugadores muere. No hay victoria por temporizador ni por acumular más puntos sin eliminar al rival. El temporizador de 10-15 minutos es un límite de duración esperada de la partida, no una condición de cierre independiente.

**Puntaje (usado para ranking/estadísticas, no para decidir quién gana la partida):**

| Evento | Puntos |
| --- | --- |
| Kill normal | +200 |
| Kill con sigilo | +350 |
| Matar a un NPC (bot) | –50 (penalización) |

El ranking del jugador (visible en la futura PWA) se basa en partidas ganadas y perdidas, no en el puntaje acumulado por partida.

> Pendiente de aprobar por Guillermo Martínez (Product Owner): esta es la interpretación que resuelve la contradicción del Portafolio 1; debe confirmarse en Sprint Review antes de programarse.

---
[← Mecánicas principales](05-mecanicas-principales.md) · [Índice GDD](00-indice.md) · [Siguiente: Armas y objetos →](07-armas-objetos.md)
