# Atributos en Java

En Java, los **atributos** (también llamados campos o propiedades) son variables que se declaran dentro de una clase y representan las características o el estado de los objetos creados a partir de esa clase.

---

## ¿Qué es un atributo?

Un atributo es una variable asociada a una clase o a sus objetos. Cada objeto puede tener valores diferentes para sus atributos, lo que permite distinguir unos objetos de otros.

**Ejemplo de la vida real:**  
En una clase `Persona`, los atributos pueden ser el nombre, la edad y la altura. Cada persona (objeto) tendrá su propio nombre, edad y altura.

---

## Ejemplo en Java

```java
public class Persona {
    // Atributos
    String nombre;
    int edad;
    double altura;
}
```

Al crear objetos de la clase, cada uno tendrá sus propios valores para estos atributos:

```java
Persona persona1 = new Persona();
persona1.nombre = "Ana";
persona1.edad = 25;
persona1.altura = 1.68;

Persona persona2 = new Persona();
persona2.nombre = "Luis";
persona2.edad = 30;
persona2.altura = 1.75;
```

---

## Tipos de atributos

- **Atributos de instancia:** Pertenecen a cada objeto. Cada objeto tiene su propia copia.
- **Atributos de clase (static):** Pertenecen a la clase y son compartidos por todos los objetos de esa clase.

**Ejemplo de atributo de clase:**

```java
public class Persona {
    String nombre;
    int edad;
    static String especie = "Humano"; // Atributo de clase
}
```

---

## Acceso a los atributos

El acceso a los atributos puede controlarse usando modificadores de acceso como `public`, `private` o `protected`. Es recomendable usar `private` y acceder a ellos mediante métodos (getters y setters) para proteger los datos.

```java
public class Persona {
    private String nombre;

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
```

---

Los atributos permiten definir y almacenar la información relevante de los objetos en Java.

## Ejemplos más complejos de atributos

A continuación se muestran ejemplos donde los atributos se usan en clases con mayor complejidad y relaciones entre objetos.

---

### 1. Clase con atributos de diferentes tipos y objetos como atributos

```java
public class Direccion {
    String calle;
    String ciudad;
    String codigoPostal;
}

public class Persona {
    String nombre;
    int edad;
    Direccion direccion; // Un objeto como atributo

    void mostrarInfo() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Ciudad: " + direccion.ciudad);
    }
}

// Uso:
Direccion dir = new Direccion();
dir.calle = "Av. Central";
dir.ciudad = "Madrid";
dir.codigoPostal = "28001";

Persona persona = new Persona();
persona.nombre = "Lucía";
persona.edad = 28;
persona.direccion = dir;

persona.mostrarInfo();
// Salida:
// Nombre: Lucía
// Edad: 28
// Ciudad: Madrid
```

---

### 2. Atributos estáticos para contar instancias

```java
public class Producto {
    String nombre;
    double precio;
    static int contador = 0; // Atributo de clase

    public Producto(String nombre, double precio) {
        this.nombre = nombre;
        this.precio = precio;
        contador++; // Se incrementa cada vez que se crea un objeto
    }
}

// Uso:
Producto p1 = new Producto("Laptop", 1200.0);
Producto p2 = new Producto("Tablet", 500.0);
System.out.println("Productos creados: " + Producto.contador); // Imprime: 2
```

---

### 3. Uso de atributos privados y métodos de acceso

```java
public class CuentaBancaria {
    private String titular;
    private double saldo;

    public CuentaBancaria(String titular, double saldoInicial) {
        this.titular = titular;
        this.saldo = saldoInicial;
    }

    public double getSaldo() {
        return saldo;
    }

    public void depositar(double cantidad) {
        if (cantidad > 0) {
            saldo += cantidad;
        }
    }
}

// Uso:
CuentaBancaria cuenta = new CuentaBancaria("Carlos", 1000.0);
cuenta.depositar(500.0);
System.out.println("Saldo actual: " + cuenta.getSaldo()); // Imprime: 1500.0
```

---
