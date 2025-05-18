# Condicionales en Java

Los condicionales permiten tomar decisiones en el flujo de un programa, ejecutando diferentes bloques de código según se cumplan o no ciertas condiciones. Se utilizan para controlar el comportamiento del programa dependiendo de valores o resultados de expresiones lógicas.

## Tipos de condicionales en Java

En Java, los condicionales pueden clasificarse en simples, compuestos, múltiples y de selección múltiple:

### 1. if — Condicional simple

Se usa para ejecutar un bloque de código solo si una condición es verdadera.

```java
if (condicion) {
    // Código a ejecutar si la condición es verdadera
}
```
**Uso:** Cuando solo necesitas comprobar una condición.

---

### 2. if-else — Condicional compuesto

Permite ejecutar un bloque de código si la condición es verdadera y otro bloque si es falsa.

```java
if (condicion) {
    // Código si la condición es verdadera
} else {
    // Código si la condición es falsa
}
```
**Uso:** Cuando necesitas ejecutar una alternativa si la condición no se cumple.

---

### 3. if-else if-else — Condicional múltiple

Permite evaluar múltiples condiciones en orden.

```java
if (condicion1) {
    // Código si condicion1 es verdadera
} else if (condicion2) {
    // Código si condicion2 es verdadera
} else {
    // Código si ninguna condición anterior es verdadera
}
```
**Uso:** Cuando tienes varias condiciones mutuamente excluyentes.

---

### 4. switch — Selección múltiple

Se utiliza para seleccionar entre múltiples opciones posibles según el valor de una variable.

```java
switch (variable) {
    case valor1:
        // Código si variable == valor1
        break;
    case valor2:
        // Código si variable == valor2
        break;
    default:
        // Código si ningún caso coincide
}
```
**Uso:** Cuando tienes que comparar una variable contra varios valores posibles (especialmente con tipos `int`, `char`, `String` o `enum`).

---

### 5. Condicional anidado

Un condicional anidado es aquel en el que se coloca una estructura condicional dentro de otra. Esto permite tomar decisiones más complejas, evaluando condiciones adicionales solo si se cumple una condición previa.

```java
if (condicion1) {
    // Código si condicion1 es verdadera
    if (condicion2) {
        // Código si condicion2 también es verdadera
    } else {
        // Código si condicion2 es falsa
    }
} else {
    // Código si condicion1 es falsa
}
```
**Uso:** Cuando necesitas comprobar una condición solo si otra ya se ha cumplido, permitiendo decisiones jerárquicas o más detalladas.

---


