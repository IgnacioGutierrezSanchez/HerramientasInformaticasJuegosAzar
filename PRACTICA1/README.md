## Evaluador de Manos de Poker (NLHE)
Este repositorio contiene una implementación en Java de un sistema para evaluar manos de poker en la modalidad No-Limit Texas Hold'em (NLHE). El objetivo es calcular la mejor jugada posible dada una o varias combinaciones de cartas, identificar draws potenciales, y comparar manos entre varios jugadores.

### Funcionamiento del Evaluador
El sistema se ejecuta desde línea de comandos pasando como parámetros el número del apartado, el fichero de entrada con las cartas, y un fichero de salida para registrar los resultados. Cada carta se representa con dos caracteres: el valor (A, K, Q, J, T, 9...2) y el palo (h, d, c, s).

Los apartados obligatorios implementan distintas situaciones de evaluación:

- Evaluación de 5 cartas: Indica la mejor mano y los posibles draws (gutshot, open-ended, flush draw).
- Evaluación con 2 cartas propias + 3-5 comunitarias: Calcula la mejor mano del jugador. Si hay 5 comunitarias, no se evalúan draws.
- Comparación entre múltiples jugadores (2-9): Evalúa y ordena a los jugadores de mejor a peor mano usando sus 2 cartas privadas y 5 comunitarias.
- También se incluye un apartado opcional que permite calcular la mejor jugada en la modalidad Omaha, donde cada jugador tiene 4 cartas y debe usar exactamente 2 junto con 3 de la mesa.

### Características Técnicas
Implementado íntegramente en Java.
Entrada y salida por ficheros de texto, sin espacios ni separadores salvo ; en algunos apartados.
Estructura modular: procesamiento de cartas, detección de jugadas, gestión de draws, comparación entre jugadores.
Libre elección del diseño interno (clases, estructuras de datos) por parte del desarrollador.

### Autores
Mario López Díaz
Ignacio Gutiérrez Sánchez

