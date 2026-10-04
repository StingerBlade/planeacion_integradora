# 7. Armas y objetos

> Actualizado el 4-oct-2026 con lo definido en el documento de diseño U1E4 (ver [entregas/u1e4-documento-diseno.md](../../entregas/u1e4-documento-diseno.md)). Valores calculados sobre vida base 100 (125 con casco); se pueden ajustar tras los playtests.

**Regla general:** portar un arma delata al jugador, porque los NPCs nunca llevan armas. Los objetos (boosts y curación) **no son visibles** sobre el oso; su efecto solo se ve en el HUD de quien los recoge.

## Armas del MVP (Esencial)

| Arma | Daño | Golpes para eliminar | Comportamiento |
| --- | --- | --- | --- |
| Aguja de coser | 25 por golpe · cabeza: oneshot | 4 (5 con casco) | Cuerpo a cuerpo, alcance corto, sin munición, un golpe cada 0.6 s. Permite la kill con sigilo (+350). |
| Pistola de dardos (estilo Nerf, dardos de tachuela) | 35 por dardo · cabeza: oneshot | 3 (4 con casco) | A distancia, 6 dardos en total, sin recarga. Aparece una sola vez, anunciada, al iniciar la fase 2. Cada eliminación con ella vale +400 (puntos dobles). Es la misma "pistola de juguete" del Portafolio 1. |

## Armas fuera del MVP (Deseable)

| Arma | Daño propuesto | Comportamiento |
| --- | --- | --- |
| Espada de madera | 30 por golpe | Cuerpo a cuerpo, más alcance que la aguja, más lenta (1 golpe/s). |
| Lanzallamas (spray + mechero) | 10 cada 0.5 s | Alcance corto, 5 s de combustible. |
| Ratonera explosiva | 50 en área | Trampa en el suelo que explota al pisarla. |
| Trampa de ratones | 15 + inmoviliza 2 s | Trampa en el suelo que atrapa al que la pisa. |

Descartados: estambre como arma, resortes y daño por desmembramiento.

## Objetos especiales

| Objeto | Efecto | Prioridad |
| --- | --- | --- |
| Rollo de hilo | Cura 25 de vida sin pasar del máximo. Única forma de curarse. | Esencial |
| Casco | Boost invisible: vida máxima de 100 a 125 hasta ser eliminado. | Esencial |
| Caja de galletas (costurero) | Cura 50 de vida sin pasar del máximo. | Deseable |
| Bandana roja | Boost invisible: +25 % de daño cuerpo a cuerpo hasta ser eliminado. | Deseable |
| Gorro de hélice | Boost invisible: +20 % de velocidad hasta ser eliminado. | Deseable |
| Cajas de cartón y botes de basura | Escondites interactivos. | Deseable |


<details>
<summary>Historial: versión anterior a U1E4 (antes del 4-oct-2026), conservada sin cambios</summary>

## 7. Armas y objetos

El arsenal incluye armas blancas, de fuego y trampas terrestres, todo con una temática de costura o estilo cartoon.

| Objeto | Descripción / función |
| --- | --- |
| Agujas para coser / Estambre | Armas blancas básicas o utilitarias |
| Trampa de ratones | Elemento de movilidad o trampa |
| Spray para pelo y mechero | Lanzallamas improvisado |
| Pistola de dardos con tachuelas | Arma especial de rondas finales (se anuncia su llegada); munición limitada (6 disparos); otorga puntos dobles al impacto |
| Ratoneras explosivas | Trampa terrestre |
| Rollos de hilo | Curación menor (Healing Boost menor) |
| Caja de galletas (costurero) | Curación mayor (Healing Boost mayor) |
| Casco | Power-up de "armadura" |

</details>

---
[← Puntos y condiciones de victoria](06-puntos-condiciones-victoria.md) · [Índice GDD](00-indice.md) · [Siguiente: Niveles y mapas →](08-niveles-mapas.md)
