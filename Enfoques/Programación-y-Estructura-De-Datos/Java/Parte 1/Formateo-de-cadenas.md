# Formateo de cadenas en Java

El **formateo de cadenas** es el proceso de construir textos dinámicos insertando valores de variables en una cadena, siguiendo un formato específico. Esto es útil para mostrar información de manera clara, alineada y con el número de decimales o caracteres deseados.

Java permite formatear cadenas principalmente con los métodos `String.format()` y `System.out.printf()`, que utilizan **marcadores de formato** para indicar cómo debe representarse cada valor.

---

## ¿Cómo funciona el formateo de cadenas?

El formateo de cadenas se basa en una **cadena de formato** que contiene texto normal y marcadores de formato (también llamados especificadores de formato). Cada marcador indica el tipo de dato y el formato que debe tener el valor insertado.

**Ejemplo básico:**

```java
String nombre = "Ana";
int edad = 28;
String mensaje = String.format("Nombre: %s, Edad: %d", nombre, edad);
System.out.println(mensaje); // Nombre: Ana, Edad: 28
```

---

## Estructura de un marcador de formato

Un marcador de formato tiene la siguiente estructura general:

```
%[banderas][ancho][.precisión]tipo
```

- `%` — Indica el inicio del marcador.
- `[banderas]` — Opcional. Modificadores que alteran el formato.
- `[ancho]` — Opcional. Número mínimo de caracteres a mostrar.
- `[.precisión]` — Opcional. Número de decimales o caracteres.
- `tipo` — Obligatorio. Tipo de dato a mostrar (por ejemplo, `d` para enteros, `s` para cadenas).

**Ejemplo:**

```java
System.out.printf("%08.2f", 3.1416); // Imprime: 00003.14
```
Aquí:
- `%` inicia el marcador.
- `0` es una bandera (relleno con ceros).
- `8` es el ancho mínimo.
- `.2` es la precisión (2 decimales).
- `f` indica que es un número de punto flotante.

---

## Marcadores de formato más comunes

| Marcador | Tipo de dato           | Ejemplo de uso           |
|----------|------------------------|--------------------------|
| `%d`     | Entero decimal         | `%d`, `int`              |
| `%f`     | Número de punto flotante| `%f`, `double`, `float`  |
| `%s`     | Cadena de texto        | `%s`, `String`           |
| `%c`     | Carácter               | `%c`, `char`             |
| `%b`     | Booleano               | `%b`, `boolean`          |
| `%x`     | Entero en hexadecimal  | `%x`, `int`              |
| `%o`     | Entero en octal        | `%o`, `int`              |
| `%e`     | Notación científica    | `%e`, `double`           |
| `%n`     | Nueva línea            | `%n`                     |
| `%%`     | Porcentaje literal     | `%%`                     |

---

## Banderas de formato

Las **banderas** modifican la forma en que se muestra el valor. Se colocan después del `%` y antes del ancho o tipo. Algunas de las más usadas son:

| Bandera | Descripción                                      | Ejemplo de uso             | ¿Cuándo se usa?                        |
|---------|--------------------------------------------------|----------------------------|----------------------------------------|
| `-`     | Alinea a la izquierda dentro del ancho           | `%-10s`                    | Para alinear texto a la izquierda      |
| `+`     | Muestra siempre el signo (`+` o `-`)             | `%+d`                      | Para mostrar el signo de números       |
| `0`     | Rellena con ceros a la izquierda                 | `%05d`                     | Para números con ceros iniciales       |
| `,`     | Usa separador de miles                           | `%,d`                      | Para números grandes                   |
| `(`     | Números negativos entre paréntesis               | `%(d`                      | En reportes financieros                |
| `#`     | Incluye prefijo para octal/hexadecimal           | `%#x`, `%#o`               | Para mostrar `0x` en hex, `0` en octal |
| ` `     | Espacio para números positivos                   | `% d`                      | Para alinear positivos y negativos     |

**Ejemplo con varias banderas:**

```java
System.out.printf("%,+08.2f%n", -12345.678);
// Imprime: -12,345.68 (relleno, signo y separador de miles)
```

---

