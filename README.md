# Definir una clase para crear para la serie Fibonacci
# Utilizando funciones y bucles

class Serie_Fibonacci:

    def calcular(self,n):
        a, b = 0,1
        while a < n:
            print(a, end=' ')
            a, b = b, a+b

    def ingresar_dato(self):
        pregunta = 'Ingrese un número: '
        numero =  int(input(pregunta))
        return numero
        
#Instancia de clase
serie =  Serie_Fibonacci()
numero = serie.ingresar_dato()
serie.calcular(numero)
