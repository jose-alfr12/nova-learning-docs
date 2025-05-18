# La palabra clave `return` en Java

En Java, la palabra clave `return` se utiliza dentro de un método para finalizar su ejecución y, opcionalmente, devolver un valor al lugar donde fue llamado el método.

## ¿Cómo funciona `return`?

- Si el método tiene un tipo de retorno distinto de `void`, debe usar `return` para devolver un valor de ese tipo.
- Si el método es `void`, se puede usar `return;` para terminar la ejecución anticipadamente, pero no es obligatorio.

---

## Ejemplo de método que devuelve un valor

```java
public int sumar(int a, int b) {
    return a + b; // Devuelve la suma de a y b
}
```

En este ejemplo, el método `sumar` devuelve un valor entero (`int`). El valor que se retorna puede ser utilizado en otra parte del programa:

```java
int resultado = sumar(4, 7);
System.out.println("El resultado es: " + resultado); // Imprime: El resultado es: 11
```

---

## Ejemplo de uso de `return` en un método `void`

```java
public void verificarEdad(int edad) {
    if (edad < 18) {
        System.out.println("Eres menor de edad.");
        return; // Termina la ejecución del método aquí
    }
    System.out.println("Eres mayor de edad.");
}
```

---

## Resumen

- `return valor;` finaliza el método y devuelve un valor.
- `return;` (sin valor) solo termina la ejecución del método (en métodos `void`).
- Es obligatorio usar `return` en métodos que especifican un tipo de retorno distinto de `void`.

La instrucción `return` es fundamental para controlar el flujo y la salida de los métodos en Java.

## ¿Cuándo es mejor usar `return` para terminar un método?

Usar `return` anticipado es útil en los siguientes casos:

- **Validaciones o comprobaciones iniciales:** Cuando necesitas salir del método si no se cumple una condición, evitando ejecutar el resto del código innecesariamente.
- **Evitar anidaciones profundas:** Permite simplificar el código y evitar múltiples niveles de `if-else`, haciendo el flujo más claro y fácil de leer.
- **Manejo de errores o casos especiales:** Si detectas una situación en la que el método no debe continuar (por ejemplo, datos inválidos), puedes usar `return` para salir inmediatamente.

**Ejemplo:**

```java
public void procesarUsuario(String nombre) {
    if (nombre == null || nombre.isEmpty()) {
        System.out.println("Nombre inválido.");
        return; // Sale del método si el nombre no es válido
    }
    // Resto del procesamiento solo si el nombre es válido
    System.out.println("Procesando usuario: " + nombre);
}
```

## Ejercicios prácticos con `return`

A continuación se muestran ejercicios más complejos donde se utiliza la palabra clave `return` en métodos con diferentes tipos de datos:

---

### 1. Sobrecarga de métodos con diferentes tipos de datos

```java
static int plusMethodInt(int x, int y) {
    return x + y;
}

static double plusMethodDouble(double x, double y) {
    return x + y;
}

public static void main(String[] args) {
    int myNum1 = plusMethodInt(8, 5);
    double myNum2 = plusMethodDouble(4.3, 6.26);
    System.out.println("int: " + myNum1);
    System.out.println("double: " + myNum2);
}
```

---

### 2. Método que devuelve el mayor de tres números

```java
public static int maxOfThree(int a, int b, int c) {
    if (a >= b && a >= c) {
        return a;
    } else if (b >= a && b >= c) {
        return b;
    } else {
        return c;
    }
}

// Uso:
int mayor = maxOfThree(10, 25, 17);
System.out.println("El mayor es: " + mayor);
```

---

### 3. Método que verifica si una cadena es palíndromo

```java
public static boolean esPalindromo(String texto) {
    String limpio = texto.replaceAll("\\s+", "").toLowerCase();
    String invertido = new StringBuilder(limpio).reverse().toString();
    return limpio.equals(invertido);
}

// Uso:
boolean resultado = esPalindromo("Anita lava la tina");
System.out.println("¿Es palíndromo? " + resultado);
```

---

### 4. Método que devuelve el promedio de un arreglo de números

```java
public static double calcularPromedio(int[] numeros) {
    if (numeros.length == 0) return 0;
    int suma = 0;
    for (int n : numeros) {
        suma += n;
    }
    return (double) suma / numeros.length;
}

// Uso:
int[] datos = {8, 7, 9, 10};
double promedio = calcularPromedio(datos);
System.out.println("Promedio: " + promedio);
```

---
