# Ingresar un número natural, para descomponer en las sumas de números naturales
class Numeronatural:

    # Metodo que solita ingresar un número natural y retorna el dato
    def ingresar_dato(self):
        numero = int(input("Ingrese un numero natural: "))
        return numero

    # Metodo que descopone el numero natural y lo guarda como string en una lista
    def calcular(self, natural):

        if natural > 0:
            print(f"Número ingresado {natural}")
            
            inicio = natural
            lista = []
            cadena = ''

            while natural > 0:
                natural -= 1
                for i in range(inicio):
                    resul = natural + i
                    if resul == inicio:
                        cadena = str(natural) + "+" + str(i)
                        lista.append(cadena)

            print(lista)

            cadena = ''
            # Ciclo para calcular factorial
            factorial_total = 1
            while inicio > 1:
                factorial_total = factorial_total * inicio
                inicio -= 1
            print(f'Factorial: {factorial_total}')
        

        else:
            print("El número no es natural")

dato = Numeronatural()              # Instacia de la clase Numeronatural
num = int(dato.ingresar_dato())     # Llamar al metodo ingresar dato de la clase Numeronatural
dato.calcular(num)                  # Llamar al metodo calcularnumero)
