# Clases y objetos en Java

En Java, **las clases y los objetos** son conceptos fundamentales de la programación orientada a objetos (POO). Permiten modelar entidades del mundo real y sus comportamientos dentro de un programa.

---

## ¿Qué es una clase?

Una **clase** es una plantilla o modelo que define las características (atributos) y comportamientos (métodos) que tendrán los objetos creados a partir de ella. Es como un plano para construir objetos.

**Ejemplo de la vida real:**  
Piensa en la clase `Coche`. Todos los coches comparten características (marca, modelo, color) y comportamientos (acelerar, frenar, encender). La clase define cómo será cualquier coche, pero no es un coche en sí misma.

**Ejemplo en Java:**

```java
public class Coche {
    // Atributos (características)
    String marca;
    String modelo;
    String color;

    // Métodos (comportamientos)
    void encender() {
        System.out.println("El coche está encendido.");
    }

    void acelerar() {
        System.out.println("El coche está acelerando.");
    }
}
```

---

## ¿Qué es un objeto?

Un **objeto** es una instancia concreta de una clase. Es un elemento real que tiene valores específicos para sus atributos y puede ejecutar los métodos definidos en la clase.

**Ejemplo de la vida real:**  
Si la clase es `Coche`, un objeto sería un coche específico:  
- Marca: Toyota  
- Modelo: Corolla  
- Color: Rojo

**Ejemplo en Java:**

```java
public class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Coche
        Coche miCoche = new Coche();
        miCoche.marca = "Toyota";
        miCoche.modelo = "Corolla";
        miCoche.color = "Rojo";

        // Usar los métodos del objeto
        miCoche.encender();
        miCoche.acelerar();
    }
}
```

---

## Resumen de términos clave

- **Clase:** Plantilla que define atributos y métodos.
- **Objeto:** Instancia concreta de una clase.
- **Atributos:** Variables que representan las características del objeto.
- **Métodos:** Funciones que representan los comportamientos del objeto.

---

## Más ejemplos de la vida real

### Clase Persona

```java
public class Persona {
    String nombre;
    int edad;

    void saludar() {
        System.out.println("Hola, mi nombre es " + nombre);
    }
}
```

**Crear objetos:**

```java
Persona persona1 = new Persona();
persona1.nombre = "Ana";
persona1.edad = 25;
persona1.saludar(); // Imprime: Hola, mi nombre es Ana

Persona persona2 = new Persona();
persona2.nombre = "Luis";
persona2.edad = 30;
persona2.saludar(); // Imprime: Hola, mi nombre es Luis
```

---

Las clases y objetos permiten organizar el código de manera lógica y reutilizable, facilitando la representación de entidades y comportamientos del mundo real en los programas Java.

## Uso de clases múltiples: Ejemplo con relación entre clases

En Java, puedes crear programas más robustos y realistas utilizando varias clases que interactúan entre sí. Esto permite modelar relaciones del mundo real, como la relación entre un vehículo y su motor.

---

### Ejemplo: Clases Coche y Motor

Supongamos que queremos representar un coche que tiene un motor. Podemos definir dos clases: `Coche` y `Motor`. La clase `Coche` tendrá un atributo de tipo `Motor` y podrá usar los métodos de esa clase.

```java
public class Motor {
    int caballosDeFuerza;

    void fullThrottle() {
        System.out.println("¡El motor está a máxima potencia!");
    }
}

public class Coche {
    String marca;
    String modelo;
    Motor motor; // Relación: un coche tiene un motor

    void mostrarInfo() {
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Caballos de fuerza: " + motor.caballosDeFuerza);
    }
}
```

**Crear objetos y usar métodos de ambas clases:**

```java
Motor miMotor = new Motor();
miMotor.caballosDeFuerza = 150;

Coche miCoche = new Coche();
miCoche.marca = "Ford";
miCoche.modelo = "Mustang";
miCoche.motor = miMotor;

miCoche.mostrarInfo(); // Muestra información del coche y su motor
miCoche.motor.fullThrottle(); // Llama al método fullThrottle del motor
```

**Salida:**
```
Marca: Ford
Modelo: Mustang
Caballos de fuerza: 150
¡El motor está a máxima potencia!
```

---

### Ventajas de usar clases múltiples

- Permite dividir el código en componentes independientes y reutilizables.
- Facilita la representación de relaciones entre entidades (por ejemplo, un coche tiene un motor).
- Hace el código más organizado, escalable y fácil de mantener.

---
