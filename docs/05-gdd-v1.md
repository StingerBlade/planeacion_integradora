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

> Actualizado el 4-oct-2026 con el documento de diseño U1E4 ([entregas/u1e4-documento-diseno.md](entregas/u1e4-documento-diseno.md)).

- Combate PvP con armas recolectables.
- Interacción con NPCs: un golpe elimina a un NPC y penaliza −50.
- Sigilo y camuflaje: actuar como NPC (caminar sin arma). Escondites (cajas, botes) = **Deseable**.
- Detección: solo **correr, brincar o portar un arma** delatan al jugador.
- Golpe crítico a la cabeza = oneshot (aun con casco) + respawn.
- Vida 100 que **nunca se regenera sola**: solo se cura con rollo de hilo.
- 3 fases por tiempo: Luces apagadas → Mercancía nueva → Remate final.

> **Importante:** se descarta la mecánica de "policía" que detecta agresiones a NPCs (aparecía en el Portafolio 1), ya no se construye. Única consecuencia de dañar a un NPC: penalización de puntos. Ver [08-post-entrega-y-fuera-del-mvp.md](08-post-entrega-y-fuera-del-mvp.md).

## 6. Puntos y condiciones de victoria/derrota

> Regla única, confirmada por Guillermo Martínez (PO) con la hoja de balance del equipo.

La partida dura **10–15 minutos** y **gana quien tenga más puntos** al agotarse el tiempo. Al ser eliminado, el jugador **respawnea** en un punto aleatorio con 100 de vida y la partida sigue — no es muerte súbita.

**Puntaje** (decide quién gana la partida):
- Kill normal: **+200**
- Kill con sigilo: **+350**
- Kill con la pistola de dardos: **+400** (puntos dobles)
- Matar a un NPC: **−50** (penalización)

Al terminar cada partida se envían resultado y puntos a la PWA de estadísticas (**Esencial**). El ranking también se basa en partidas ganadas/perdidas.

**Confirmado:** fuente = hoja de balance "BEARSTARDS/BASTARDOSOS" (ver [game-design/assets/hoja-de-balance-bearstards.png](game-design/assets/hoja-de-balance-bearstards.png)). Esta sección reemplaza una versión anterior que decía "por eliminación", que era incorrecta.

## 7. Armas y objetos

**MVP (Esencial):**
- Aguja de coser: cuerpo a cuerpo, 25 de daño (4 golpes; 5 con casco).
- Pistola de dardos estilo Nerf (= "pistola de juguete"): 35 por dardo (3 impactos; 4 con casco), 6 dardos sin recarga, aparece anunciada al iniciar la fase 2, +400 por kill.
- Rollo de hilo: cura 25.
- Casco: boost **invisible**, vida máxima 100 → 125 hasta morir.

**Fuera del MVP (Deseable):** espada de madera (30), lanzallamas spray + mechero (10 cada 0.5 s), ratonera explosiva (50 en área), trampa de ratones (15 + inmoviliza 2 s), caja de galletas (cura 50), bandana (+25 % fuerza, invisible), gorro de hélice (+20 % velocidad, invisible), escondites.

Detalle completo en [game-design/gdd-v1.0/07-armas-objetos.md](game-design/gdd-v1.0/07-armas-objetos.md).

## 8. Niveles y mapas

Un único escenario: **"La Juguetería"**, dividido en 3 pasillos. Estanterías como muros; juguetes inanimados que bloquean la vista; ambientación de tienda departamental. Progresión en 3 fases de un tercio del tiempo cada una: **Luces apagadas** (sigilo), **Mercancía nueva** (aparece la pistola) y **Remate final** (la mitad de los NPCs vuelve a los estantes). La oficina de la tienda queda como segundo nivel **Deseable**.

## 9. Estilo visual y vestimenta

- Low poly.
- Vestimenta: **no aplica como mecánica**; todos los osos comparten modelo con marcas y accesorios parodia (nunca marcas reales). Los boosts no se ven como ropa.
- Rostro de los osos jugadores: gesto de enojo sutil, solo visible de cerca.
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
- Condición de victoria única: por puntaje al agotarse el temporizador, con respawn (no es muerte súbita).

**Pendiente real del equipo:**
- Confirmar con la profesora si Trello + este documento cuentan como evidencia oficial (vence 30-sep).
- Licencia tipográfica/marcas parodia (vence 1-oct).
- Plan B si falla Photon en vivo (antes del cierre de Fase 4, 13-nov).
