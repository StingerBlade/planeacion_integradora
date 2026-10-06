# U1E4 — Documento de diseño del proyecto integrador

**Materia:** 10N Optativa: Creación de Videojuegos · Prof. Enrique Mascote · IDGS 101N
**Equipo:** Turbo Studios · **Juego:** Little Bearstards
**Entrega:** domingo 4-oct-2026, 23:59 · PDF `U1E4_TurboStudios.pdf` · 15 % · rúbrica (heteroevaluación)

**Documento editable:** Google Docs, carpeta de Drive `101N/mascote` → [U1E4_TurboStudios](https://docs.google.com/document/d/1dvZfNnCs3BMLmb5zgk7mE7xWHq2dYJkjXyjP2McGP48/edit). Sigue el formato de las entregas anteriores de la materia (U1E1, U1E2).

**Versión en presentación:** [assets/U1E4_TurboStudios_actualizado.pptx](assets/U1E4_TurboStudios_actualizado.pptx) — mismo contenido que el PDF, en formato de diapositivas y ya con el ajuste de la pistola de dardos (50 de daño / 2 impactos) incorporado.

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
| Armas MVP | Aguja de coser (25/golpe) y pistola de dardos estilo Nerf (50/dardo: elimina en 2 impactos, 3 con casco; 6 dardos, fase 2; antes 35/dardo, ajustado a propuesta del PO). Golpe a la cabeza = oneshot, aun con casco. |
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

## Ajustes posteriores a la primera versión

- **4-oct-2026 — Pistola de dardos:** Guillermo Martínez (PO) propuso en el grupo del equipo que la pistola elimine en 2 tiros, para que sin fallar se pueda eliminar al rival 3 veces y remontar si se va perdiendo. Se cambió el daño de 35 a **50 por dardo** (2 impactos; 3 con casco). Actualizado en el documento U1E4 (secciones 6 y alcance) y en el GDD.

