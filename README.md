# Ingresar un número natural, para descomponer en las sumas de números naturales
class Numeronatural:

    def __init__(self, numero):
        self.numero = numero

    # Metodo que solita ingresar un número natural y retorna el dato
    def ingresar_dato(self):
        self.numero = input("Ingrese un numero natural: ")
        self.validar(self.numero)

    def validar(self, numero):
        if '.' in self.numero:
            print('Por favor ingresar un número sin decimales')
        else:
            print('Dato Correcto')
            self.numero = int(self.numero)
            self.calcular(numero)

    # Metodo que descopone el numero natural y lo guarda como string en una lista
    def calcular(self, natural):

        natural = int(natural)
        
        # Condión para validar si el número es Natural
        if self.numero > 0:
            print(f"Número ingresado {natural}")
            
            inicio = natural
            lista = [] # Lista vacía
            cadena = ''

            while self.numero > 0:
                self.numero -= 1
                for i in range(inicio):
                    resul = natural + i
                    if resul == inicio:
                        cadena = str(natural) + "+" + str(i)
                        lista.append(cadena)
                    """
                    if resul < inicio:
                        j = i
                        while resul < inicio:
                            resul = natural + j
                            if resul == inicio:
                                cadena = str(natural) + "+" + str(i)
                                lista.append(cadena)
                    """
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

dato = Numeronatural(0)              # Instacia de la clase Numeronatural
dato.ingresar_dato()     # Llamar al metodo ingresar dato de la clase Numeronatural
#dato.validar(self.numero)
#dato.calcular(self.numero)                  # Llamar al metodo calcular
