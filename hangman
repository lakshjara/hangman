#hangman
import random #random.choice es para escoger una palabra aleatroia de la lista

#Lista de palabras para el juego
palabras = ['python', 'programacion', 'ahorcado', 'juego', 'computadora', 'teclado', 'pantalla', 'tec', 'borregos']

#utiliza random.choice(palabras) para devolver una palabra seleccionada aleatoriamente de la lista palabras
def elige_palabra():
    return random.choice(palabras) #palabra seleccionada aleatoriamente
'''
Probando con la palabra: python
'''

#muestra el estado actual de la palabra que se está adivinando
def muestra_progreso(palabra, letras_adivinadas): 
    return ' '.join([letra if letra in letras_adivinadas else '_' for letra in palabra]) #.join unie todos los elementos del iterable y crea una cadena y la devuelve como salida al usuario

'''
Intentos restantes: 6
_ _ _ _ _ _
'''

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


'''
Probando con la palabra: python 
¡Bienvenido al juego del Ahorcado!
La palabra tiene 6 letras.

Intentos restantes: 6
_ _ _ _ _ _
Adivina una letra: o
¡Bien hecho! La letra 'o' está en la palabra.
'''

if __name__ == '__main__':

    jugar()
