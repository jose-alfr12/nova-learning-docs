# Métodos, parámetros y argumentos en Java

En Java, un **método** es un bloque de código que realiza una tarea específica y puede ser reutilizado en diferentes partes de un programa. Los métodos permiten organizar el código, evitar repeticiones y facilitar el mantenimiento.

## ¿Qué es un método?

Un método es una función definida dentro de una clase. Tiene un nombre, puede recibir parámetros y ejecutar instrucciones.

**Ejemplo en Java:**

```java
public void mostrarMensaje() {
    System.out.println("Bienvenido al sistema.");
}
```

---

## Parámetros y argumentos

- **Parámetros:** Son variables declaradas en la definición del método y representan los datos que el método necesita para funcionar.
- **Argumentos:** Son los valores concretos que se pasan al método cuando se invoca.

**Ejemplo:**

```java
public void imprimirSuma(int a, int b) { // a y b son parámetros
    System.out.println("La suma es: " + (a + b));
}

imprimirSuma(5, 3); // 5 y 3 son argumentos
```

---

## Palabras clave en la declaración de métodos

En la declaración de un método pueden aparecer varias palabras clave que modifican su comportamiento:

- **public:** El método es accesible desde cualquier otra clase.
- **private:** El método solo es accesible dentro de la misma clase.
- **protected:** El método es accesible dentro del mismo paquete y por subclases.
- **static:** El método pertenece a la clase y no a una instancia. Se puede llamar sin crear un objeto de la clase.
    - Ejemplo: `public static void mostrarMensaje()`
    - Uso: Métodos utilitarios o el método principal de un programa.
- **void:** Indica que el método no devuelve ningún valor.
    - Ejemplo: `public void mostrarMensaje()`
    - Uso: Cuando el método solo realiza una acción y no retorna datos.

---

## Ejemplo de una situación real

Supongamos que en un sistema escolar se necesita mostrar un mensaje de bienvenida personalizado para cada estudiante. Se puede crear un método que reciba el nombre del estudiante como parámetro y muestre el mensaje correspondiente:

```java
public void darBienvenida(String nombre) {
    System.out.println("Bienvenido, " + nombre + "!");
}

// Llamada al método:
darBienvenida("Carlos"); // Imprime: Bienvenido, Carlos!
```