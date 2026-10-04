# U1E4 — Documento de diseño del proyecto integrador

**Materia:** 10N Optativa: Creación de Videojuegos · Prof. Enrique Mascote · IDGS 101N
**Equipo:** Turbo Studios · **Juego:** Little Bearstards
**Entrega:** domingo 4-oct-2026, 23:59 · PDF `U1E4_TurboStudios.pdf` · 15 % · rúbrica (heteroevaluación)

**Documento editable:** Google Docs, carpeta de Drive `101N/mascote` → [U1E4_TurboStudios](https://docs.google.com/document/d/1dvZfNnCs3BMLmb5zgk7mE7xWHq2dYJkjXyjP2McGP48/edit). Sigue el formato de las entregas anteriores de la materia (U1E1, U1E2).

## Contenido del documento

Ficha técnica · 1. Género · 2. Público objetivo · 3. Historia · 4. Personajes · 5. Niveles · 6. Armas · 7. Vestimenta · 8. Objetos especiales · Alcance del proyecto.

## Decisiones de diseño que fija (resumen)

| Tema | Decisión |
| --- | --- |
| Victoria | Más puntos al agotarse el tiempo (10-15 min); respawn en punto aleatorio con 100 de vida. |
| Puntos | Kill +200 · kill con sigilo +350 · kill con pistola de dardos +400 · NPC −50. |
| Detección | Solo correr, brincar o portar un arma delatan al jugador. |
| NPCs | Casi idénticos; mueren de un golpe; nunca corren, brincan ni portan armas. |
| Vida | 100, nunca se regenera sola; solo se cura con rollo de hilo (+25). |
| Armas MVP | Aguja de coser (25/golpe) y pistola de dardos estilo Nerf (35/dardo, 6 dardos, fase 2). Golpe a la cabeza = oneshot, aun con casco. |
| Boosts | Invisibles. Casco: vida máx. 125 (Esencial). Bandana +25 % fuerza y gorro de hélice +20 % velocidad (Deseables). |
| Fases | 1. Luces apagadas · 2. Mercancía nueva (llega la pistola) · 3. Remate final (la mitad de los NPCs vuelve a los estantes). |
| Vestimenta | No aplica como mecánica; único rasgo distinto: rostro enojado sutil de los osos jugadores. |
| Fuera del MVP | Escondites, espada, lanzallamas, ratoneras, trampa de ratones, caja de galletas, bandana, gorro, oficina, modo local, audio/voces. |
| Esencial nuevo | Estadísticas en la PWA (antes estaba como Deseable). |

**Cambios respecto a planes anteriores que el equipo debe tener en cuenta:**
- Los escondites interactivos pasaron a Deseable; por eso la fase 3 reduce NPCs en lugar de cerrar escondites.
- El casco ya no es armadura visible: es vida extra invisible.
- Correr ya no es lo único que delata: también brincar y portar arma; atacar no está en la lista.

Ver el detalle técnico en el [GDD v1.0](../game-design/gdd-v1.0/00-indice.md).
