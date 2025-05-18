# Clase Math en Java

La clase `Math` en Java proporciona métodos estáticos para realizar operaciones matemáticas comunes, como exponenciación, raíces, trigonometría, logaritmos y más. A continuación se listan algunas de las funciones más utilizadas:

## Funciones principales de la clase Math

### Constantes

- `Math.PI` — Valor de π (pi)
- `Math.E` — Base de los logaritmos naturales (e)

### Funciones aritméticas

- `Math.abs(x)` — Valor absoluto de `x`
- `Math.max(a, b)` — Máximo entre `a` y `b`
- `Math.min(a, b)` — Mínimo entre `a` y `b`
- `Math.pow(a, b)` — `a` elevado a la potencia `b`
- `Math.sqrt(x)` — Raíz cuadrada de `x`
- `Math.cbrt(x)` — Raíz cúbica de `x`
- `Math.hypot(a, b)` — Hipotenusa de un triángulo rectángulo con lados `a` y `b`
- `Math.floor(x)` — Redondea hacia abajo (menor entero)
- `Math.ceil(x)` — Redondea hacia arriba (mayor entero)
- `Math.round(x)` — Redondea al entero más cercano
- `Math.rint(x)` — Redondea al entero más cercano como valor double
- `Math.copySign(mag, sign)` — Copia el signo de `sign` a `mag`

### Funciones trigonométricas

- `Math.sin(x)` — Seno de `x` (en radianes)
- `Math.cos(x)` — Coseno de `x` (en radianes)
- `Math.tan(x)` — Tangente de `x` (en radianes)
- `Math.asin(x)` — Arco seno de `x`
- `Math.acos(x)` — Arco coseno de `x`
- `Math.atan(x)` — Arco tangente de `x`
- `Math.atan2(y, x)` — Arco tangente de `y/x` considerando el cuadrante

### Funciones exponenciales y logarítmicas

- `Math.exp(x)` — e elevado a la `x`
- `Math.log(x)` — Logaritmo natural (base e) de `x`
- `Math.log10(x)` — Logaritmo en base 10 de `x`
- `Math.log1p(x)` — Logaritmo natural de (1 + x)

### Funciones aleatorias

- `Math.random()` — Devuelve un número aleatorio entre 0.0 (incluido) y 1.0 (excluido)

### Otras funciones útiles

- `Math.toDegrees(x)` — Convierte radianes a grados
- `Math.toRadians(x)` — Convierte grados a radianes
- `Math.signum(x)` — Devuelve el signo de `x` (-1.0, 0.0 o 1.0)
- `Math.ulp(x)` — Unidad en el último lugar de `x`
- `Math.nextUp(x)` — Siguiente valor flotante mayor que `x`
- `Math.nextDown(x)` — Siguiente valor flotante menor que `x`