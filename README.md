# Proyecto de Evaluación de Póker en Java

Este repositorio agrupa distintas prácticas desarrolladas en Java relacionadas con el juego de póker Texas Hold'em y Omaha. Cada práctica aborda una funcionalidad concreta, desde la simulación de partidas hasta el cálculo de equity, evaluación de manos y gestión de rangos.

## Índice de Prácticas

### 1. **Juego Heads-Up de Póker**
Simulación de partidas uno contra uno (Heads-Up) en la modalidad Texas Hold'em.

**Características:**
- Dos jugadores con stacks, turnos de apuestas y lógica básica.
- Reparto de cartas (2 privadas + 5 comunitarias).
- Evaluación automática de la mano ganadora.
- Estructura modular: clases para cartas, baraja, jugador, mesa y motor del juego.

---

### 2. **Evaluador de Manos de Póker (NLHE)**
Sistema en línea de comandos que analiza y compara manos de jugadores.

**Características:**
- Evaluación de jugadas con 5, 6 o 7 cartas.
- Detección de draws: gutshot, open-ended, flush draw.
- Comparación entre 2 a 9 jugadores con 2 cartas privadas y 5 comunitarias.
- Soporte para modalidad Omaha (opcional): 4 cartas privadas y uso exacto de 2 + 3 comunitarias.
- Entrada/salida mediante ficheros de texto.
- Implementación completamente en Java.

---

### 3. **Evaluación de Rangos en Póker (NLHE)**
Herramienta gráfica para representar, calcular y analizar rangos pre-flop.

**Apartados obligatorios:**
- **Representación gráfica de rangos**: cuadrícula interactiva tipo PokerStove.
- **Conversión texto ↔ cuadrícula** con soporte de operadores (`+`, `-`, `s`, `o`).
- **Cálculo del rango según un porcentaje de manos iniciales**, usando rankings predefinidos.
- **Cómputo de combos** y **probabilidades** de tipos de jugadas (overpair, top pair, trío, color, etc.) dado un rango y un board de 3-5 cartas.

**Características técnicas:**
- GUI con soporte textual y visual.
- Gestión de manos, combos y evaluaciones probabilísticas.

---

### 4. **Calculadora de Equity de Póker**
Aplicación gráfica para calcular la probabilidad de ganar o empatar (equity) en cada fase de una mano.

**Equity por fases:**
- Pre-flop
- Flop
- Turn
- River

**Configuración flexible:**
- Cartas asignadas aleatoriamente o manualmente a cada jugador (hasta 6).
- Board personalizable manual o aleatoriamente.
- Comparación validada con herramientas profesionales como PokerStove y Equilab.

**Opcional 1 – Botón de Fold:**
- Permite eliminar jugadores en cualquier fase.
- El equity se recalcula considerando solo los jugadores activos.

**Opcional 2 – Soporte Omaha:**
- Cada jugador tiene 4 cartas privadas.
- Se calcula el equity respetando las reglas: usar exactamente 2 cartas de mano + 3 del board.

---

## Requisitos Generales

- Java 8 o superior.
- IDE recomendado: IntelliJ IDEA, Eclipse o NetBeans.
- Sistema operativo compatible con Java.

---

## Autores

- Mario López Díaz  
- Ignacio Gutiérrez Sánchez

