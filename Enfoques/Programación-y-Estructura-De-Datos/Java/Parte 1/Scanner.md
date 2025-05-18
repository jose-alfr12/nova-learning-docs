# Clase Scanner en Java

La clase `Scanner` es una de las formas más sencillas y utilizadas para leer datos introducidos por el usuario en Java. Permite capturar diferentes tipos de datos (números, cadenas, etc.) desde diversas fuentes, siendo la más común la entrada estándar del teclado.

## ¿Cómo se usa Scanner?

Para utilizar `Scanner`, primero debes importar la clase:

```java
import java.util.Scanner;
```

Luego, puedes crear un objeto `Scanner` asociado a la entrada estándar (`System.in`):

```java
Scanner sc = new Scanner(System.in);
```

### Ejemplo de lectura de datos

```java
System.out.print("Introduce tu nombre: ");
String nombre = sc.nextLine();

System.out.print("Introduce tu edad: ");
int edad = sc.nextInt();

System.out.println("Hola, " + nombre + ". Tienes " + edad + " años.");
```

## Métodos principales de Scanner

- `nextInt()` — Lee un entero.
- `nextDouble()` — Lee un número decimal.
- `nextLine()` — Lee una línea completa de texto.
- `next()` — Lee la siguiente palabra (hasta un espacio).
- `nextBoolean()` — Lee un valor booleano.

---

## Flujo de entrada de Scanner

El **flujo de entrada** se refiere a la fuente desde la cual el objeto `Scanner` obtiene los datos. Por defecto, se utiliza `System.in`, que representa la entrada estándar del sistema (normalmente el teclado).

```java
Scanner sc = new Scanner(System.in); // Lee desde el teclado
```

Sin embargo, `Scanner` también puede leer datos desde archivos, cadenas de texto u otras fuentes:

```java
Scanner scArchivo = new Scanner(new File("datos.txt")); // Lee desde un archivo
Scanner scCadena = new Scanner("123 456"); // Lee desde una cadena de texto
```

El flujo de entrada determina de dónde provienen los datos que el programa va a procesar. Es importante cerrar el objeto `Scanner` cuando ya no se necesite, usando `sc.close()`, para liberar recursos.

---

