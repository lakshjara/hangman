# Proyecto Final
En este proyecto se demostrará el manejo de funciones en el lenguaje de programación python, recopilando los temas vistos en la clase de pensamiento computacional para la ingeniería. 

# Hangman

### Contexto
El juego del Ahorcado o "Hangman" es una actividad desafiante y divertida que se basa en deducción y desarrolla el conociemiento del vocaburario de los jugadores. Fomenta el aprendizaje de nuevas palabras resforzando así las habilidades lingüísticas y ortográficas.

Este juego consta de adivinar letras para descubrir la palabra oculta. Los jugadores deberán encontrar la palabra antes de que se terminen los intentos del juego, el cual se completa progresivamente con cada error en la adivinanza. 

### Instrucciones

Descargar el archivo y correr con terminal en:

```bash
python hangman.py
```
Descargar el archivo de texto 
```bash
animales.txt
```

Utliza el link de descarga para instalar Python
https://www.python.org/downloads/ 

### Teclas utilizadas en el juego
1. Abecedario
2. Números

### Procedimiento del juego
   
Inicio del juego: un jugador selecciona una pablabra que ocultará con guiones, cada guion representando una letra de la palabra. 

Adivinanza de Letras: Los participantes sugieren letras una por una, y cada letra correcta se revela en la posición correspondiente de los guiones. Cada error, es decir cada letra que no está en la palabra, añade una parte al dibujo del ahorcado.

Objetivo del Juego: Los jugadores deben adivinar la palabra antes de que se complete el dibujo del ahorcado, que generalmente incluye una cabeza, torso, brazos y piernas. Si logran adivinar la palabra antes de que se complete el dibujo, ganan el juego. De lo contrario, pierden.

# Algoritmo

1. Entrada:

Palabra secreta: la palabra que los jugadores deben adivinar.

Número máximo de intentos: el número máximo de errores permitidos antes de perder el juego.

2. Proceso:

Inicializar el juego.

Mostrar la cantidad de letras en la palabra secreta usando guiones bajos (_).

Inicializar una lista para las letras adivinadas correctamente.

Inicializar un contador para el número de intentos fallidos.

Mientras queden intentos y la palabra no esté completamente adivinada:
Mostrar el estado actual de la palabra con las letras adivinadas.

Solicitar al jugador una letra.

Verificar si la letra ya ha sido adivinada:
Si es así, mostrar un mensaje indicando que la letra ya fue adivinada.
Si no, proceder con la verificación.

Verificar si la letra está en la palabra secreta:
Si está, actualizar la palabra mostrada con la nueva letra y añadir la letra a la lista de letras adivinadas.
Si no está, incrementar el contador de intentos fallidos.

Mostrar el número de intentos restantes.
Verificar si el jugador ha ganado (la palabra está completamente adivinada) o ha perdido (se han agotado los intentos):
Si ha ganado, mostrar un mensaje de victoria y la palabra completa.
Si ha perdido, mostrar un mensaje de derrota y la palabra secreta.

3. Salida:

Mensaje final indicando si el jugador ganó o perdió.

La palabra secreta completa si el jugador perdió.

