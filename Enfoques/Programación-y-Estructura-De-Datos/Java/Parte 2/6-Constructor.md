# Constructores en Java

En Java, un **constructor** es un método especial que se utiliza para inicializar los objetos de una clase. Se llama automáticamente cuando se crea un nuevo objeto y permite asignar valores iniciales a los atributos.

---

## ¿Qué es un constructor?

Un constructor es un bloque de código con el mismo nombre que la clase y sin tipo de retorno (ni siquiera `void`). Puede recibir parámetros para establecer los valores iniciales de los atributos del objeto.

---

## Ejemplo de la vida real

Si tienes una clase `Libro`, puedes usar un constructor para crear libros con título y autor definidos desde el inicio:

```java
public class Libro {
    String titulo;
    String autor;

    // Constructor
    public Libro(String titulo, String autor) {
        this.titulo = titulo;
        this.autor = autor;
    }
}
```

**Uso:**

```java
Libro libro1 = new Libro("Cien años de soledad", "Gabriel García Márquez");
Libro libro2 = new Libro("1984", "George Orwell");
System.out.println(libro1.titulo); // Imprime: Cien años de soledad
```

---

## Tipos de constructores

- **Constructor por defecto:** No recibe parámetros. Si no defines ningún constructor, Java crea uno por defecto automáticamente.
- **Constructor parametrizado:** Recibe uno o más parámetros para inicializar los atributos.

**Ejemplo de ambos:**

```java
public class Persona {
    String nombre;
    int edad;

    // Constructor por defecto
    public Persona() {
        nombre = "Sin nombre";
        edad = 0;
    }

    // Constructor parametrizado
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

---

## Sobrecarga de constructores

Puedes definir varios constructores en una clase, siempre que tengan diferentes listas de parámetros (sobrecarga).

```java
Persona p1 = new Persona(); // Usa el constructor por defecto
Persona p2 = new Persona("Ana", 25); // Usa el constructor parametrizado
```

---

## Importancia de los constructores

- Permiten inicializar los objetos con valores válidos desde el principio.
- Mejoran la legibilidad y robustez del código.
- Facilitan la creación de objetos con diferentes configuraciones.

---