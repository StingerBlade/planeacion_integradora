# 10. Multijugador y red

**Tecnología:** Photon PUN2 (decisión del equipo, tarjeta "[RESUELTO] 1v1 en línea con Photon PUN2"). Se descartaron LAN, Steam Relay y peer-to-peer manual por: paquete oficial para Unity con componentes listos (PhotonView, RPCs), capa gratuita suficiente (20 CCU), y no depende de que los jugadores compartan red ni tengan Steam abierto.

**Qué se sincroniza por red:** únicamente los 2 jugadores humanos (posición, animación, armas y golpes).

**Qué NO se sincroniza:** los NPCs de camuflaje; cada cliente los simula localmente e independientemente, para no sobrecargar la red con IA irrelevante al resultado del duelo.

**Preparación técnica:** los prefabs de jugador deben vivir en la carpeta `Resources` para poder usarse con `PhotonNetwork.Instantiate`.

**Riesgo crítico (ver [Sección 11](11-riesgos-pendientes.md)):** se necesita un plan B para la presentación en vivo si falla la conexión de Photon el día de la entrega.

---
[← Estilo visual y vestimenta](09-estilo-visual-vestimenta.md) · [Índice GDD](00-indice.md) · [Siguiente: Riesgos y pendientes →](11-riesgos-pendientes.md)
