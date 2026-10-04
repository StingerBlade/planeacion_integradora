# 4. Personajes

**Jugables.** Osos de peluche con marcas parodia (no marcas reales, por riesgo legal). Son los únicos personajes capaces de correr, brincar, recoger objetos y atacar. Movimiento tipo muñeco de trapo (ragdoll / Fall Guys), arqueando las extremidades hacia atrás al correr. Su rostro es un poco distinto al de los NPCs: cejas fruncidas y gesto de enojo, una diferencia sutil que solo se nota de cerca (ver [Sección 9](09-estilo-visual-vestimenta.md)).

**NPCs.** Otros osos de peluche merodeando el mapa, controlados por IA simple (patrullar, detenerse, quedarse quietos), casi idénticos visualmente a los jugadores. Nunca corren, brincan ni portan armas. Sirven de camuflaje: un jugador puede mezclarse entre ellos para ocultar su identidad. Un golpe de cualquier arma elimina a un NPC (y le resta 50 puntos al atacante). No atacan ni persiguen. Se simulan localmente en cada cliente (no se sincronizan por red).

**Atributos de personaje.**

| Atributo | Valor base | Qué representa |
| --- | --- | --- |
| Vida | 100 | Al llegar a 0 el oso es eliminado y reaparece con vida completa. **Nunca se regenera sola**: solo se recupera con el rollo de hilo. |
| Relleno | — | Representación visual de la vida: el oso pierde relleno conforme recibe daño. |
| Velocidad | Caminar / correr | Caminar es la velocidad de los NPCs; correr es más rápido pero delata. |
| Armadura | 0 | Vida extra del casco: +25, hasta 125. Se pierde al ser eliminado. |
| Fuerza | Daño base del arma | Daño de los ataques cuerpo a cuerpo. |

---
[← Público objetivo](03-publico-objetivo.md) · [Índice GDD](00-indice.md) · [Siguiente: Mecánicas principales →](05-mecanicas-principales.md)
