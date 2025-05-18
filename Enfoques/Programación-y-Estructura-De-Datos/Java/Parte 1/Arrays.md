# Arrays en Java

Un **array** (arreglo) es una estructura de datos que permite almacenar múltiples valores del mismo tipo en una sola variable. Los arrays son útiles para manejar colecciones de datos de tamaño fijo.

## Características principales

- Todos los elementos de un array son del mismo tipo (por ejemplo, `int`, `double`, `String`).
- El tamaño del array se define al momento de crearlo y no puede cambiar.
- Los elementos se acceden mediante un índice, que comienza en 0.

---

## Declaración y creación de arrays

### Declarar un array

```java
int[] numeros;
String[] nombres;
```

### Crear un array

```java
numeros = new int[5]; // Array de 5 enteros
nombres = new String[3]; // Array de 3 cadenas
```

También se puede declarar y crear en una sola línea:

```java
double[] notas = new double[4];
```

### Inicializar un array con valores

```java
int[] edades = {18, 21, 30, 25};
String[] dias = {"Lunes", "Martes", "Miércoles"};
```

---

## Acceso y modificación de elementos

Para acceder o modificar un elemento, se usa el índice:

```java
int x = edades[2]; // Accede al tercer elemento (30)
edades[0] = 20;    // Cambia el primer elemento a 20
```

---

## Recorrer un array

Se puede usar un bucle `for` tradicional o un bucle `for-each`:

```java
for (int i = 0; i < edades.length; i++) {
    System.out.println(edades[i]);
}

for (String dia : dias) {
    System.out.println(dia);
}
```

---

## Arrays multidimensionales

Java permite crear arrays de más de una dimensión (por ejemplo, matrices):

```java
int[][] matriz = new int[3][2]; // 3 filas, 2 columnas
matriz[0][1] = 5;
```

---

