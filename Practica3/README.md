# Calculadora de Equity de Poker

## Descripción

Esta aplicación permite calcular el **equity** (probabilidad de ganar o empatar) de cada jugador en cada una de las fases de una mano de póker: **pre-flop, flop, turn y river**. Está diseñada con una interfaz gráfica (GUI) que reproduce las funcionalidades de herramientas como **PokerStove** y **Equilab**.

La aplicación admite un máximo de **6 jugadores** por mano, y permite configurar tanto las cartas de los jugadores como el board (mesa) de forma manual o aleatoria.

## Características

### Parte obligatoria

- Cálculo del equity de cada jugador en todas las fases de la mano:
  - Pre-flop
  - Flop
  - Turn
  - River
- Configuración flexible:
  - Asignación aleatoria de manos
  - Asignación manual de cartas a cada jugador
  - Configuración aleatoria o manual del board
- Resultados precisos validados frente a herramientas estándar (PokerStove, Equilab)
- Soporte para hasta **6 jugadores**

### Parte opcional 1 – Botón de Fold

- Permite eliminar jugadores en cualquier fase de la mano
- El cálculo de equity se adapta dinámicamente al número de jugadores activos
- Simula situaciones reales donde algunos jugadores hacen fold en distintas calles

### Parte opcional 2 – Modalidad Omaha

- Cálculo del equity en partidas de **Omaha**
- Se respetan las reglas de la modalidad:
  - Cada jugador forma su jugada con exactamente **2 cartas propias** y **3 del board**

## Requisitos

- Java (versión 8 o superior)
- IDE recomendado: IntelliJ IDEA, Eclipse o NetBeans
- Sistema operativo compatible con Java

## Instrucciones de uso

1. Compilar y ejecutar la aplicación desde tu entorno de desarrollo.
2. Seleccionar el número de jugadores (hasta 6).
3. Asignar cartas manualmente o usar la opción aleatoria.
4. Definir el board (mesa) manualmente o de forma aleatoria.
5. Calcular el equity en cada fase de la mano (pre-flop, flop, turn, river).
6. (Opcional) Usar el botón de "Fold" para eliminar jugadores antes de avanzar.
7. (Opcional) Activar la modalidad Omaha para calcular según sus reglas.

## Verificación de resultados

Puedes comparar los resultados de equity con los obtenidos por las herramientas:

- [PokerStove](http://www.pokerstove.com/)
- [Equilab](https://www.pokerstrategy.com/poker-tools/equilab-holdem/)

Estas herramientas permiten validar el funcionamiento y precisión de la aplicación.

## Autores

- **Mario López Díaz**  
- **Ignacio Gutiérrez Sánchez**
