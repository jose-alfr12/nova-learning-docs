# Clase JOptionPane en Java

La clase `JOptionPane` es parte del paquete `javax.swing` y se utiliza para mostrar cuadros de diálogo gráficos que permiten interactuar con el usuario mediante ventanas emergentes. Es muy útil para solicitar información, mostrar mensajes o advertencias sin necesidad de usar la consola.

## ¿Cómo se usa JOptionPane?

Para utilizar `JOptionPane`, primero debes importar la clase:

```java
import javax.swing.JOptionPane;
```

## Métodos principales

- `showMessageDialog` — Muestra un mensaje simple.
- `showInputDialog` — Solicita al usuario que ingrese un dato.
- `showConfirmDialog` — Solicita una confirmación (Sí/No/Cancelar).
- `showOptionDialog` — Permite personalizar las opciones del cuadro de diálogo.

## Ejemplos de uso

### Mostrar un mensaje

```java
JOptionPane.showMessageDialog(null, "¡Hola, mundo!");
```

### Solicitar un dato al usuario

```java
String nombre = JOptionPane.showInputDialog("¿Cuál es tu nombre?");
```

### Solicitar confirmación

```java
int respuesta = JOptionPane.showConfirmDialog(null, "¿Deseas continuar?");
if (respuesta == JOptionPane.YES_OPTION) {
    // El usuario eligió "Sí"
} else if (respuesta == JOptionPane.NO_OPTION) {
    // El usuario eligió "No"
} else if (respuesta == JOptionPane.CANCEL_OPTION) {
    // El usuario eligió "Cancelar"
}
```

## Constantes de respuesta en JOptionPane

Cuando se usa `showConfirmDialog`, el valor devuelto indica la opción seleccionada por el usuario. Las constantes más comunes son:

- `JOptionPane.YES_OPTION` — El usuario eligió "Sí" (valor 0)
- `JOptionPane.NO_OPTION` — El usuario eligió "No" (valor 1)
- `JOptionPane.CANCEL_OPTION` — El usuario eligió "Cancelar" (valor 2)
- `JOptionPane.CLOSED_OPTION` — El usuario cerró la ventana sin elegir opción (valor -1)

Estas constantes permiten saber exactamente qué botón presionó el usuario y actuar en consecuencia.

---

