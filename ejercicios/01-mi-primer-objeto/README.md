"""
Ejercicio 1: Mi primer objeto
-------------------------------
Objetivo: completar la clase Mascota para practicar los conceptos
de clase, objeto, atributo y método.

Instrucciones:
1. Completar el método __init__ para que guarde nombre, especie y edad.
2. Completar el método saludar() para que imprima un mensaje usando
   los atributos de la mascota.
3. Completar el método cumplir_anios() para que sume 1 a la edad
   e imprima un mensaje avisando el cambio.
4. Al final del archivo, crear DOS objetos distintos de la clase
   Mascota y probar sus métodos.
"""


class Mascota:
    def __init__(self, nombre, especie, edad):
        # TODO: completar los atributos usando los parámetros
        # self.nombre = ...
        # self.especie = ...
        # self.edad = ...
        pass

    def saludar(self):
        # TODO: imprimir algo como:
        # "Hola, soy Firulais, soy un Perro y tengo 3 años"
        pass

    def cumplir_anios(self):
        # TODO: sumar 1 a self.edad
        # e imprimir algo como:
        # "¡Firulais cumplió años! Ahora tiene 4 años"
        pass


# ----------------------------------------------------
# Zona de pruebas: creá tus objetos acá abajo
# ----------------------------------------------------

# Ejemplo (descomentar y completar):
# mascota1 = Mascota("Firulais", "Perro", 3)
# mascota1.saludar()
# mascota1.cumplir_anios()

# mascota2 = Mascota(...)
# mascota2.saludar()
