# Conceptos básicos de POO 🧱

## ¿Qué es la Programación Orientada a Objetos (POO)?

Es una forma de organizar el código pensando en **objetos**, parecidos a los objetos del mundo real: tienen características (datos) y pueden hacer cosas (acciones).

---

## 🐶 La analogía del perro

Pensemos en un **perro** real.

- Tiene **atributos** (características): nombre, raza, edad, color.
- Tiene **métodos** (acciones que puede hacer): ladrar, comer, correr.

Ahora bien: "Perro" en general es una **idea**, un **molde**. Cada perro concreto (Firulais, Toby, Luna) es una instancia de ese molde, con sus propios valores.

| Concepto | Analogía del perro | En código |
|---|---|---|
| **Clase** | El molde/plano de "qué es un perro" | `class Perro:` |
| **Objeto** | Un perro concreto (Firulais) | `firulais = Perro("Firulais", "Labrador")` |
| **Atributo** | Nombre, raza, edad | `self.nombre`, `self.raza` |
| **Método** | Ladrar, comer | `def ladrar(self):` |

---

## 🏗️ Clase = plano de una casa

Otra forma de verlo: una **clase** es como el **plano de una casa**. El plano define que va a tener puertas, ventanas, habitaciones... pero el plano no es habitable.

Cuando un constructor usa ese plano y construye una casa real, ahí tenemos un **objeto**: una casa concreta, en una dirección concreta, con un color de paredes concreto.

Con el mismo plano podés construir muchas casas (objetos) distintas, todas con la misma estructura pero con sus propios valores.

---

## En código (Python)

```python
class Perro:
    # El __init__ es el "constructor": se ejecuta cuando creamos un perro nuevo
    def __init__(self, nombre, raza):
        self.nombre = nombre   # atributo
        self.raza = raza       # atributo

    def ladrar(self):          # método
        print(f"{self.nombre} dice: ¡Guau guau!")


# Creamos objetos (instancias) a partir de la clase Perro
firulais = Perro("Firulais", "Labrador")
toby = Perro("Toby", "Caniche")

firulais.ladrar()  # Firulais dice: ¡Guau guau!
toby.ladrar()       # Toby dice: ¡Guau guau!

print(firulais.nombre)  # Firulais
print(toby.raza)        # Caniche
```

---

## 🔑 Resumen de conceptos clave

- **Clase**: el molde/plano. Define qué atributos y métodos va a tener cada objeto.
- **Objeto (instancia)**: algo concreto creado a partir de la clase.
- **Atributo**: un dato que guarda el objeto (su "estado").
- **Método**: una función que pertenece a la clase y describe lo que el objeto puede hacer.
- **`self`**: es la forma en que, dentro de la clase, un objeto se refiere "a sí mismo".

> 💡 **Para pensarlo fácil**: si en tu código estás describiendo *cosas* (con características y acciones), probablemente te conviene pensar en clases y objetos.
