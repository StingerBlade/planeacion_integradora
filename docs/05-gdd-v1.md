# 5. GDD v1.0 — Little Bearstards

> Tomado directo de la tarjeta de Trello `[Fase 1] Angel Arras (SM) - GDD v1 y coordinacion` (lista 🔨 En progreso). Generado por Angel a partir del Portafolio 1 del equipo y de las decisiones tomadas en la planeación. Existe también una versión completa en Word con Angel Arras.

## 1. Ficha técnica

- **Nombre:** Little Bearstards (alt. Bastardosos)
- **Género:** Stealth PvP con deducción social y acción
- **Plataforma:** PC
- **Motor:** Unity
- **Jugadores:** 2 (1v1)
- **Red:** en línea vía Photon PUN2
- **Duración:** 10–15 min
- **Edad sugerida:** +13

## 2. Historia y premisa

Una juguetería en transición a tienda de videojuegos está por cerrar. En el último pasillo quedan los últimos osos de peluche sin vender; de noche cobran consciencia y descubren que serán incinerados si no son vendidos antes del cierre. Deciden eliminarse entre sí para ser el único superviviente y así ser comprados. Las armas están repartidas por los pasillos; los jugadores pueden mezclarse entre NPCs para ocultar su identidad. El ganador termina en el baúl de juguetes (vendido); el perdedor en la basura (desechado).

## 3. Público objetivo

Jugadores +13, en PC, partidas competitivas cortas de sigilo y deducción social.

## 4. Personajes

- **Jugables:** osos con marcas parodia (no reales), únicos que corren/saltan/agarran armas, movimiento ragdoll tipo Fall Guys.
- **NPCs:** otros osos merodeando, IA simple, casi idénticos al jugador, sirven de camuflaje, **se simulan localmente** (no van por red).
- **Atributos:** vida, velocidad, armadura, fuerza, relleno.

## 5. Mecánicas principales

- Combate PvP con armas recolectables.
- Interacción con NPCs (golpearlos por error penaliza).
- Sigilo y camuflaje (esconderse o actuar como NPC).
- Detección (correr/golpear/portar arma delata).
- Golpe crítico a la cabeza = oneshot + respawn.

> **Importante:** se descarta la mecánica de "policía" que detecta agresiones a NPCs (aparecía en el Portafolio 1), ya no se construye. Única consecuencia de dañar a un NPC: penalización de puntos. Ver [08-post-entrega-y-fuera-del-mvp.md](08-post-entrega-y-fuera-del-mvp.md).

## 6. Puntos y condiciones de victoria/derrota

> Regla única, resuelve una contradicción entre los documentos originales del equipo.

La partida es **por eliminación**: gana quien elimina al rival; termina en cuanto uno de los dos muere. No hay victoria por temporizador ni por más puntos sin eliminar al rival (el timer de 10–15 min es solo duración esperada).

**Puntaje** (para ranking/estadísticas, no decide quién gana la partida):
- Kill normal: **+200**
- Kill con sigilo: **+350**
- Matar a un NPC: **−50** (penalización)

El ranking (PWA, ver sección 6 del índice) se basa en partidas ganadas/perdidas.

**Pendiente:** Guillermo Martínez (PO) debe confirmar esta regla en Sprint Review antes de programarse.

## 7. Armas y objetos

- Agujas para coser / estambre (arma blanca básica)
- Trampa de ratones (movilidad/trampa)
- Spray + mechero (lanzallamas improvisado)
- Pistola de dardos con tachuelas (especial, rondas finales, 6 disparos, x2 puntos)
- Ratoneras explosivas (trampa terrestre)
- Rollos de hilo (curación menor)
- Caja de galletas / costurero (curación mayor)
- Casco (power-up de armadura)

> Para el MVP de 8 semanas, el alcance real de armas programadas se recortó (ver Fases 2–4 en [04-cronograma-fases.md](04-cronograma-fases.md)): pistola de juguete, aguja de coser, caja de hilos (curación) y casco (armadura).

## 8. Niveles y mapas

Un único escenario: **"La Juguetería"**, dividido en 3 pasillos. Estanterías como muros que dividen secciones; juguetes inanimados como cobertura; ambientación de tienda departamental (anaqueles, luz de techo fluorescente). Un solo mapa en el MVP, sin niveles extra.

## 9. Estilo visual y vestimenta

- Low poly.
- Marcas y accesorios parodia (nunca marcas reales, riesgo legal).
- Tipografía base Comic Sans (alternativa libre: **Comic Neue**).
- Interfaz con fondo propio y voces de personajes.
- Animación ragdoll al correr.

## 10. Multiplayer y red

**Photon PUN2** (se descartaron LAN, Steam Relay, P2P manual — ver [03-decisiones.md](03-decisiones.md)): paquete oficial de Unity, capa gratis de 20 CCU, no depende de red compartida ni de Steam abierto.

Se sincronizan por red **solo los 2 jugadores humanos** (posición, animación, armas, golpes); los NPCs de camuflaje **no** se sincronizan, cada cliente los simula local. Los prefabs de jugador deben vivir en la carpeta `Resources` para `PhotonNetwork.Instantiate`.

**Riesgo crítico:** falta ejecutar el plan B si falla Photon en la presentación en vivo (ver tarjeta de decisión correspondiente en [03-decisiones.md](03-decisiones.md)).

## 11. Riesgos y pendientes antes del 4-oct

**Ya resuelto en este GDD:**
- Red online vía Photon (no local).
- Sin oso policía.
- Condición de victoria única por eliminación.

**Pendiente real del equipo:**
- Confirmar con la profesora si Trello + este documento cuentan como evidencia oficial (vence 30-sep).
- Licencia tipográfica/marcas parodia (vence 1-oct).
- Plan B si falla Photon en vivo (antes del cierre de Fase 4, 13-nov).
