# TC 1028 Proyecto Demo
Este proyecto es un ejemplo de lo que se espera en cuanto a complejidad y formato de su proyecto libre final de TC 1028. úsenlo para guiar sus decisiones de diseño y ver ejemplos de cómo se aplica PEP8. No copien código ni funciones, pueden basarse en estas pero escriban las suyas. Lo que nos interesa es que interioricen las estrategias y entiendan la lógica, para generar un pograma modular correctamente estrcuturado. Por ejemplo vean la forma en la que se separa el código en funciones que se puedan reusar en cada parte.

Con cada tema que veamos vean como se aplica en el proyecto para construir un programa. En general estre proyecto sigue estándares (PEP 8) y buenas prácticas de industria que también evaluamos en el curso, así que les sirve de ejemplo para estilo también.

En los comentarios dentro de cada función, entre parentesis, vienen las subcompetencias que demuestra esa función o ese conjunto de funciones.

espero les sea de ayuda :D
# Hangman

### contexto
El juego del Ahorcado o "Hangman" es una actividad desafiante y divertida que se basa en deducción y desarrolla el conociemiento del vocaburario de los jugadores. Fomenta el aprendizaje de nuevas palabras resforzando así las habilidades lingüísticas y ortográficas.

Este juego consta de adivinar letras para descubrir la palabra oculta. Los jugadores deberán encontrar la palabra antes de que se complete el dibujo del ahorcado, el cual se completa progresivamente con cada error en la adivinanza. 

### Instrucciones

Descargar el archivo y correr con terminal en:

```bash
python hangman.py
```

Inicio del juego: un jugador selecciona una pablabra que ocultará con guiones, cada guion representando una letra de la palabra. 

Adivinanza de Letras: Los participantes sugieren letras una por una, y cada letra correcta se revela en la posición correspondiente de los guiones. Cada error, es decir cada letra que no está en la palabra, añade una parte al dibujo del ahorcado.

Objetivo del Juego: Los jugadores deben adivinar la palabra antes de que se complete el dibujo del ahorcado, que generalmente incluye una cabeza, torso, brazos y piernas. Si logran adivinar la palabra antes de que se complete el dibujo, ganan el juego. De lo contrario, pierden.

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