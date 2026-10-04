# 7. Pruebas

Plan de pruebas tal como aparece en el Portafolio 1.

## Funcionamiento de las mecánicas principales

El funcionamiento del videojuego se comprobará durante todo el desarrollo mediante pruebas realizadas después de implementar cada sistema. De esta manera, los errores podrán detectarse y corregirse antes de integrar nuevas funciones.

Después de implementar cada mecánica se realizarán pruebas para comprobar que funciona de acuerdo con el diseño del juego. Se verificará, por ejemplo, que las acciones del jugador, las interacciones y las mecánicas del PvP produzcan el resultado esperado.

**Criterio de verificación:** la mecánica deberá funcionar correctamente varias veces de forma consecutiva sin presentar comportamientos inesperados.

## Controles

Se probarán los controles de movimiento, cámara y demás acciones del jugador.

Se comprobará que:
- Las teclas o botones ejecuten la acción correspondiente.
- El personaje responda correctamente al movimiento.
- La cámara siga y se comporte correctamente.

No existan movimientos involuntarios, bloqueos o respuestas incorrectas.

## Colisiones e interacción

Se realizarán pruebas recorriendo diferentes partes del escenario para comprobar las colisiones entre el jugador, paredes, estanterías, objetos y otros elementos. También se verificarán las interacciones entre jugadores y objetos del escenario.

**Criterio de verificación:** ningún jugador deberá atravesar objetos que deberían bloquearlo ni quedar atrapado en elementos del escenario.

## Condiciones de victoria y derrota

Se probarán las diferentes situaciones que pueden provocar una victoria o derrota. Se verificará que el juego reconozca correctamente estas condiciones y que la partida termine o continúe según las reglas establecidas. **En este caso, la partida se terminará al terminar el temporizador y ganará el jugador con la mayor cantidad de puntos.**

> ⚠️ Esta frase es la que contradice a la sección "Condiciones generales de victoria, derrota o finalización" del propio Portafolio 1 (que define la victoria como "ser el último en pie"). Ver el detalle en [docs/game-design/07-huecos-argumentales.md](../game-design/07-huecos-argumentales.md) y la regla única ya fijada en [GDD v1.0 · Sección 6](../game-design/gdd-v1.0/06-puntos-condiciones-victoria.md).

## Errores o comportamientos inesperados

Durante las pruebas se registrarán los errores encontrados, indicando qué ocurrió, cómo reproducirlo y qué elemento del juego está involucrado. Los problemas se registrarán en el repositorio del proyecto mediante Issues, donde se marcarán como pendientes, en proceso o corregidos.

## Jugabilidad

Se realizarán partidas de prueba entre los integrantes del equipo para comprobar que las mecánicas, controles e interacciones funcionen correctamente durante una partida completa. También se identificarán situaciones que puedan dificultar o impedir el desarrollo normal del juego.

## Rendimiento básico

Se comprobará que el videojuego mantenga un funcionamiento fluido durante las partidas. Se observarán aspectos como la velocidad de ejecución, tiempos de carga y posibles caídas de rendimiento al utilizar varios personajes, objetos o elementos del escenario. Se espera un mínimo de 30 fotogramas por segundo como mínimo en dispositivos de entrada, 60 fotogramas en dispositivos gama media y más de 60 en equipos de gama alta.

## Verificación de problemas corregidos

Después de corregir un problema, se repetirá la prueba que originalmente permitió detectarlo. Si el error ya no se presenta, se marcará como corregido en el registro. Posteriormente, otro integrante del equipo realizará una segunda prueba para confirmar la solución y verificar que la corrección no haya generado otro problema.

---
[← Desarrollo](06-desarrollo.md) · [Índice Portafolio 1](00-indice.md) · [Siguiente: Conclusión y viabilidad →](08-conclusion-viabilidad.md)
