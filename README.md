# Proyecto Final
En este proyecto se demostrará el manejo de funciones en el lenguaje de programación python, recopilando los temas vistos en la clase de pensamiento computacional para la ingeniería. 

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

# Código Juego del ahorcado
    import random #random.choice es para escoger una palabra aleatroia de la lista

    #Lista de palabras para el juego
    palabras = ['python', 'programacion', 'ahorcado', 'juego', 'computadora', 'teclado', 'pantalla', 'tec', 'borregos']

    #utiliza random.choice(palabras) para devolver una palabra seleccionada aleatoriamente de la lista palabras
    def elige_palabra():
    return random.choice(palabras) #palabra seleccionada aleatoriamente

    #muestra el estado actual de la palabra que se está adivinando
    def muestra_progreso(palabra, letras_adivinadas): 
    return ' '.join([letra if letra in letras_adivinadas else '_' for letra in palabra]) #.join unie todos los elementos del iterable y crea una cadena y la devuelve como salida al usuario

    #ejecuta el ciclo del juego
    def jugar():
        palabra = elige_palabra()
        letras_adivinadas = set()
        intentos = 6  # Número de intentos

        print("¡Bienvenido al juego del Ahorcado!")
        print(f"La palabra tiene {len(palabra)} letras.") #len devuelve el número de caracteres de una serie 

    while intentos > 0: #bucle del juego
        print(f"\nIntentos restantes: {intentos}") #\n se usa para indicar el fin de una línea y el inicio de una nueva
        print(muestra_progreso(palabra, letras_adivinadas))

        letra = input("Adivina una letra: ").lower() #lower sirve para convertir los caracteres en minúsculas

        if letra in letras_adivinadas:
            print("Ya adivinaste esa letra. Intenta con otra.")
            continue

        letras_adivinadas.add(letra) #.add inserta un solo elemento en un conjunto

        if letra in palabra:
            print(f"¡Bien hecho! La letra '{letra}' está en la palabra.") #f-string para mostrar valores de variables
        else:
            print(f"Lo siento, la letra '{letra}' no está en la palabra.")
            intentos -= 1

        if all(letra in letras_adivinadas for letra in palabra):
            print(f"\n¡Felicidades! Has adivinado la palabra '{palabra}' correctamente.")
            break
    else:
        print(f"\nTe has quedado sin intentos. La palabra era '{palabra}'. ¡Mejor suerte la próxima vez!")

    if __name__ == '__main__':

    jugar()

