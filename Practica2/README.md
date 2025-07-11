# Evaluador de Manos de Poker (NLHE)

Este repositorio contiene una implementación en Java de un sistema para evaluar manos de poker en la modalidad No-Limit Texas Hold'em (NLHE). El objetivo es calcular la mejor jugada posible dada una o varias combinaciones de cartas, identificar draws potenciales, y comparar manos entre varios jugadores.

## Objetivo

Esta práctica consiste en calcular y representar rangos en el juego NLHE.

## Descripción

La práctica está formada por 3 apartados obligatorios y 1 opcional, de tal forma que el 70% de la calificación corresponde a la parte obligatoria y el 30% restante a la parte opcional. Para poder realizar la parte opcional es necesario haber realizado la parte obligatoria.

> No se tendrán en cuenta las partes opcionales realizadas si la parte obligatoria no está completamente implementada.

La sintaxis para representar cada carta será la misma que se utilizó en la práctica 1 (valor + palo, como `Ah`, `Td`, etc.).

---

### 2.1 Calcular rangos y su representación gráfica (obligatorio) [1.5 puntos]

Dado un rango textual, se debe generar su representación gráfica y viceversa, a través de una interfaz gráfica (GUI), como en PokerStove.

**Formato de entrada textual del rango:**

- Pares de cartas, con sufijos `s` (suited) y `o` (offsuit), separados por comas:  
  Ejemplo: `AA,JJ,ATs-A8s,76o,54o`
- Operador `+`:
  - Para parejas: incluye todas las parejas superiores.
    - Ej: `JJ+` → incluye `JJ`, `QQ`, `KK`, `AA`
  - Para no parejas: mantiene la carta más alta fija y varía la baja.
    - Ej: `T2s+` → incluye `T2s`, `T3s`, ..., `T9s`
- Operador `-`: representa un intervalo entre dos pares de cartas.
  - Ej: `ATs-A2s` → todas las suited entre AT y A2

**Interacción gráfica:**
- Selección textual genera una cuadrícula gráfica.
- Selección gráfica devuelve el rango textual equivalente.
- Mostrar el **porcentaje de manos** incluidas en el rango representado.

---

### 2.2 Calcular el rango de manos dados un ranking y un porcentaje (obligatorio) [1.5 puntos]

Se debe calcular el rango de manos correspondiente a un **porcentaje de manos iniciales**, usando un ranking elegido por el usuario.

**Ranking sugerido** (ordenado por fuerza aproximada):

AA, KK, AKs, QQ, AKo, JJ, AQs, TT, AQo, 99, AJs, ...

**Ejemplos:**
- Rango del 25% de manos iniciales.
- Rango del 70% de manos iniciales.

> Se puede usar cualquier ranking conocido (como Sklansky-Chubukov o el de PokerStove).

---

### 2.3 Contar combos y calcular probabilidades de manos hechas (obligatorio) [4 puntos]

Dado un **rango** y un **board** (3, 4 o 5 cartas), calcular:

- El número de **combos** del rango que generan **cada tipo de jugada**.
- La probabilidad de cada jugada:
  
  \[
  \text{Probabilidad} = \frac{\text{nº combos de la jugada}}{\text{nº total de combos}}
  \]

#### Jugadas consideradas:
- Escalera de color
- Poker
- Full house
- Color
- Escalera
- Trío
- Dobles parejas
- Pareja (clasificadas en: overpair, top pair, middle pair, weak pair, pocket pair below top pair)
- Carta alta

**Reglas:**
- Debe usarse al menos **una carta del rango**.
- Se eliminan combos incompatibles con el board.
- No se cuentan jugadas triviales con el board únicamente.

**Entrada del rango y board:**
- Mediante `textbox` textual o selección gráfica.

**Ejemplo 1:**  
Rango: `AA,KK,22,AKs,Q9s,65s`  
Board: `Ah Qh Jc`  
Total combos: 25  
Resultado esperado:

Trío: 3/12 → 25%
Top pair: 3/12 → 25%
Middle pair: 6/12 → 50%

## Características Técnicas

- Implementado en **Java**
- Entrada y salida mediante **ficheros de texto**
- Estructura modular: procesamiento de cartas, evaluación de jugadas, gestión de draws, comparación entre jugadores.
- Ampliable para otros modos como **Omaha** (4 cartas privadas, usar 2 de mano + 3 comunitarias)

---

## Autores

- **Mario López Díaz**  
- **Ignacio Gutiérrez Sánchez**
