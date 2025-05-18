# Bucles o sentencias de repetición en Java

Los bucles permiten ejecutar un bloque de código varias veces, dependiendo de una condición. Son fundamentales para automatizar tareas repetitivas y recorrer estructuras de datos.

## Tipos de bucles en Java

### 1. Bucle while

Ejecuta el bloque de código mientras la condición sea verdadera. La condición se evalúa antes de cada iteración.

```java
while (condicion) {
    // Código a ejecutar mientras la condición sea verdadera
}
```
**Uso:** Cuando no sabes cuántas veces se repetirá el ciclo y depende de una condición.

---

### 2. Bucle do-while

Ejecuta el bloque de código al menos una vez y luego repite mientras la condición sea verdadera. La condición se evalúa después de cada iteración.

```java
do {
    // Código a ejecutar al menos una vez
} while (condicion);
```
**Uso:** Cuando necesitas que el bloque se ejecute al menos una vez, sin importar la condición inicial.

---

### 3. Bucle for

Se utiliza cuando conoces de antemano cuántas veces quieres repetir el bloque de código.

```java
for (inicialización; condición; actualización) {
    // Código a ejecutar en cada iteración
}
```
**Uso:** Ideal para recorrer arreglos o repetir un bloque un número específico de veces.

---

### 4. Bucle for-each (for mejorado)

Especialmente útil para recorrer colecciones y arreglos de manera sencilla.

```java
for (Tipo elemento : coleccion) {
    // Código a ejecutar para cada elemento
}
```
**Uso:** Cuando quieres recorrer todos los elementos de un arreglo o colección sin preocuparte por los índices.

---
