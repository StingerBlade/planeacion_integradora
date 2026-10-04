# 7. Evaluación de huecos argumentales

Aplicando el método de "Cómo encontrar huecos argumentales" al Portafolio 1 (ambas versiones), se encontró una contradicción real entre secciones del propio documento del equipo, y algunos puntos menores.

## Contradicción principal: dos condiciones de victoria distintas

El documento define la condición de victoria de dos formas incompatibles en secciones distintas:

| Sección del Portafolio 1 | Qué dice sobre cómo termina la partida |
| --- | --- |
| "Objetivo Principal del Jugador" y "Sistema de Puntos" | La partida dura 10-15 min y **gana quien tenga más puntos al final del tiempo** (no requiere eliminar al rival) |
| "Condiciones generales de victoria, derrota o finalización" | Victoria = **ser el último en pie (vivo)**; la partida **finaliza al quedar solo un jugador con vida** (elimina al rival, no hay temporizador) |
| "Pruebas" (sección 7) | Confirma la primera versión: "la partida se terminará al terminar el temporizador y ganará el jugador con la mayor cantidad de puntos" |

Estas dos reglas producen partidas distintas: en una, un jugador puede "ganar por puntos" sin haber eliminado nunca al rival (basta con golpear NPCs con sigilo, aunque eso mismo esté penalizado si son inocentes); en la otra, la partida no puede terminar hasta que alguien muera, sin importar el tiempo. El equipo necesita elegir una sola regla antes de programarla — ahora mismo dos secciones del mismo documento describen dos juegos distintos.

> **Resuelto en el GDD v1.0 (confirmado por el PO con la hoja de balance del equipo):** la regla correcta es la de la primera fila de la tabla — gana quien tenga más puntos al agotarse el temporizador de 10-15 min. Morir no termina la partida: el jugador respawnea y el combate sigue hasta que se acaba el tiempo. La frase "último en pie" que aparece en otras partes de los documentos del equipo es la que estaba desactualizada. Ver [GDD v1.0 · Sección 6](gdd-v1.0/06-puntos-condiciones-victoria.md).

## Otros puntos a revisar (menores)

- **Solución obvia no descartada:** si ambos juguetes saben que solo puede sobrevivir uno y que moverse los delata, ¿por qué no intentan escapar de la tienda en vez de pelear? El documento no explica qué se lo impide (¿puertas cerradas?, ¿alarma?). No es necesariamente un error, pero conviene una línea que lo bloquee explícitamente.
- **Causalidad de fondo sin resolver:** no se explica por qué los peluches cobran consciencia esa noche en particular. Puede quedarse como regla del mundo no explicada (común en historias de juguetes), pero es una decisión consciente, no un olvido, así que vale la pena que el equipo decida si le importa justificarlo.
- **Tono/público:** el público objetivo declarado es "mayores de 13 años" con una estética de peluches, pero la mecánica central es eliminar/incinerar juguetes con golpes críticos a la cabeza. No es un hueco argumental, pero conviene que el equipo confirme que el tono (humor negro/violencia estilizada tipo Fall Guys) es el buscado para esa clasificación de edad.
- **Prueba de eliminación:** todos los elementos documentados (armas, trampas, curación, power-ups, los 3 pasillos) tienen una función clara dentro de la mecánica; no se detectó contenido decorativo sin propósito.

---
[← Pitch y siguientes pasos](06-pitch-siguientes-pasos.md) · [Índice](00-indice.md)
