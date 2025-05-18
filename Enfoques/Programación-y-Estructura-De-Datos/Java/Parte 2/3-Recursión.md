# Recursión en Java

La **recursión** es una técnica de programación en la que un método se llama a sí mismo para resolver un problema dividiéndolo en subproblemas más pequeños. Es útil cuando un problema puede definirse en términos de sí mismo, como en el cálculo de factoriales, secuencias, recorridos de estructuras de datos, entre otros.

## ¿Cómo funciona la recursión?

Un método recursivo debe tener:
- **Caso base (Halting Condition o condición de parada):** Es la condición que detiene la recursión y evita llamadas infinitas. Cuando se cumple, el método deja de llamarse a sí mismo y retorna un valor fijo.
- **Llamada recursiva:** El método se llama a sí mismo con un valor diferente, acercándose al caso base.

---

## Ejemplo: Suma recursiva de números desde k hasta 0

```java
public class Main {
    public static void main(String[] args) {
        int result = sum(10);
        System.out.println(result); // Imprime: 55
    }

    public static int sum(int k) {
        if (k > 0) {
            return k + sum(k - 1); // Llamada recursiva
        } else {
            return 0; // Caso base (condición de parada)
        }
    }
}
```

**Lógica:**  
El método `sum` suma todos los números desde `k` hasta 0. Si `k` es mayor que 0, suma `k` y llama a sí mismo con `k-1`. Cuando `k` llega a 0, retorna 0 y la recursión termina. Por ejemplo, para `sum(3)`, el flujo es:  
`3 + sum(2)` → `3 + (2 + sum(1))` → `3 + (2 + (1 + sum(0)))` → `3 + (2 + (1 + 0))` → `3 + (2 + 1)` → `3 + 3` → `6`.

---

## Otros ejemplos de recursión

### Factorial de un número

```java
public static int factorial(int n) {
    if (n == 0) {
        return 1;
    } else {
        return n * factorial(n - 1);
    }
}
```

**Lógica:**  
El método `factorial` calcula el producto de todos los enteros positivos desde `n` hasta 1. Si `n` es 0, retorna 1 (por definición matemática). Si no, multiplica `n` por el factorial de `n-1`. Por ejemplo, `factorial(4)` es `4 * factorial(3)` → `4 * 3 * factorial(2)` → `4 * 3 * 2 * factorial(1)` → `4 * 3 * 2 * 1 * factorial(0)` → `4 * 3 * 2 * 1 * 1` → `24`.

---

### Secuencia de Fibonacci

```java
public static int fibonacci(int n) {
    if (n == 0) return 0;
    if (n == 1) return 1;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
```

**Lógica:**  
El método `fibonacci` devuelve el n-ésimo número de la secuencia de Fibonacci, donde cada número es la suma de los dos anteriores. Si `n` es 0, retorna 0; si es 1, retorna 1. Para otros valores, suma el resultado de `fibonacci(n-1)` y `fibonacci(n-2)`. Por ejemplo, `fibonacci(4)` es `fibonacci(3) + fibonacci(2)` → `(fibonacci(2) + fibonacci(1)) + (fibonacci(1) + fibonacci(0))` → `(1 + 1) + (1 + 0)` → `2 + 1` → `3`.

---

## Consideraciones al usar recursión

- Siempre debe existir un **caso base** o **condición de parada** (Halting Condition) para evitar recursión infinita.
- La recursión puede ser menos eficiente que los bucles para problemas simples, pero es muy útil para problemas naturalmente recursivos (como árboles o algoritmos de búsqueda).
- El uso excesivo de recursión puede causar desbordamiento de pila (`StackOverflowError`) si las llamadas son demasiadas.

La recursión es una herramienta poderosa para resolver problemas que pueden dividirse en subproblemas similares.

## ¿Qué es la pila (stack) en recursión?

La **pila** (stack) es una estructura de datos de tipo LIFO (Last In, First Out: el último en entrar es el primero en salir) que utiliza la memoria de ejecución de los programas para gestionar las llamadas a métodos y funciones. Cada vez que se llama a un método, se crea un nuevo marco o registro de activación en la pila, que almacena información como los parámetros, variables locales y la dirección de retorno. Cuando el método termina, ese marco se elimina de la pila y el control regresa al método que lo llamó.

En la recursión, cada llamada recursiva agrega un nuevo marco a la pila. Cuando se alcanza el caso base, las llamadas comienzan a resolverse en orden inverso, eliminando marcos de la pila hasta volver al punto inicial.

Si la recursión es muy profunda (muchas llamadas anidadas), la pila puede llenarse y provocar un error llamado `StackOverflowError`.

---

## Ejemplo de la pila con el primer ejercicio

En el ejercicio de suma recursiva:

```java
public static int sum(int k) {
    if (k > 0) {
        return k + sum(k - 1);
    } else {
        return 0;
    }
}
```

Cuando se llama a `sum(3)`, la pila se comporta así:

1. `sum(3)` se llama y espera el resultado de `sum(2)` (se apila `sum(3)`)
2. `sum(2)` se llama y espera el resultado de `sum(1)` (se apila `sum(2)`)
3. `sum(1)` se llama y espera el resultado de `sum(0)` (se apila `sum(1)`)
4. `sum(0)` retorna 0 (caso base, se apila y desapila inmediatamente)

Ahora la pila se vacía resolviendo cada suma pendiente:
- `sum(1)` recibe 0, retorna `1 + 0 = 1` (se desapila)
- `sum(2)` recibe 1, retorna `2 + 1 = 3` (se desapila)
- `sum(3)` recibe 3, retorna `3 + 3 = 6` (se desapila)

Cada llamada permanece en la pila hasta que la llamada recursiva interna retorna un valor. Por eso, si la recursión es muy profunda, se puede llenar la pila y causar un `StackOverflowError`.