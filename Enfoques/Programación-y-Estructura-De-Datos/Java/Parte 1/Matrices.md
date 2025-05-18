# Matrices en Java

Una **matriz** es un array de dos dimensiones (también llamado array bidimensional) que permite almacenar datos en forma de tabla, con filas y columnas. Las matrices son útiles para representar datos tabulares, como tablas, tableros de juegos, imágenes, etc.

## Declaración y creación de matrices

### Declarar una matriz

```java
int[][] matriz;
String[][] nombres;
```

### Crear una matriz

```java
matriz = new int[3][4]; // Matriz de 3 filas y 4 columnas
nombres = new String[2][2]; // Matriz de 2x2 de cadenas
```

También se puede declarar y crear en una sola línea:

```java
double[][] valores = new double[5][3];
```

### Inicializar una matriz con valores

```java
int[][] numeros = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

---

## Acceso y modificación de elementos

Para acceder o modificar un elemento, se usan dos índices: el de la fila y el de la columna.

```java
int x = numeros[1][2]; // Accede al elemento en la fila 1, columna 2 (valor 6)
numeros[0][0] = 10;    // Cambia el valor en la fila 0, columna 0 a 10
```

---

## Recorrer una matriz

Se utilizan bucles anidados para recorrer todas las filas y columnas:

```java
for (int i = 0; i < numeros.length; i++) {
    for (int j = 0; j < numeros[i].length; j++) {
        System.out.print(numeros[i][j] + " ");
    }
    System.out.println();
}
```

---

## Matrices de más dimensiones

Java permite crear arrays de más de dos dimensiones (por ejemplo, `int[][][]`), aunque en la práctica las matrices de dos dimensiones son las más comunes.

---
