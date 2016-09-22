##Patrones de Diseño

Los *patrones de diseño* son la base para la búsqueda de soluciones a problemas comunes en el desarrollo de software y otros ámbitos referentes al diseño de interacción o interfaces.

Un patrón de diseño resulta ser una solución a un problema de diseño. Para que una solución sea considerada un patrón debe poseer ciertas características. Una de ellas es que debe haber comprobado su **efectividad** resolviendo problemas similares en ocasiones anteriores. Otra es que debe ser reutilizable, lo que significa que es aplicable a diferentes problemas de diseño en distintas circunstancias.

##Patrón Singleton

En ingeniería de software, el patrón singleton (instancia única en inglés) es un patrón de diseño diseñado para restringir la creación de objetos pertenecientes a una clase o el valor de un tipo a un único objeto.

Su intención consiste en garantizar que una clase sólo tenga una instancia y proporcionar un punto de acceso global a ella.

El patrón singleton se implementa creando en nuestra clase un método que crea una instancia del objeto sólo si todavía no existe alguna. Para asegurar que la clase no puede ser instanciada nuevamente se regula el alcance del constructor (con modificadores de acceso como protegido o privado).

La instrumentación del patrón puede ser delicada en programas con múltiples hilos de ejecución. Si dos hilos de ejecución intentan crear la instancia al mismo tiempo y esta no existe todavía, sólo uno de ellos debe lograr crear el objeto. La solución clásica para este problema es utilizar exclusión mutua en el método de creación de la clase que implementa el patrón.

Las situaciones más habituales de aplicación de este patrón son aquellas en las que dicha clase controla el acceso a un recurso físico único (como puede ser el ratón o un archivo abierto en modo exclusivo) o cuando cierto tipo de datos debe estar disponible para todos los demás objetos de la aplicación.

El patrón singleton provee una única instancia global gracias a que:

La propia clase es responsable de crear la única instancia.
Permite el acceso global a dicha instancia mediante un método de clase.
Declara el constructor de clase como privado para que no sea instanciable directamente.

Una implementación correcta en el lenguaje de programación Java es la siguiente:

```java
public class Singleton {
    private static final Singleton INSTANCE = new Singleton();

    // El constructor privado no permite que se genere un constructor por defecto.
    // (con mismo modificador de acceso que la definición de la clase) 
    private Singleton() {}

    public static Singleton getInstance() {
        return INSTANCE;
    }
}
```

##Factory Method

En diseño de software, el patrón de diseño Factory Method consiste en utilizar una clase constructora (al estilo del Abstract Factory) abstracta con unos cuantos métodos definidos y otro(s) abstracto(s): el dedicado a la construcción de objetos de un subtipo de un tipo determinado. Es una simplificación del Abstract Factory, en la que la clase abstracta tiene métodos concretos que usan algunos de los abstractos; según usemos una u otra hija de esta clase abstracta, tendremos uno u otro comportamiento.

##Patrón Builder

Como Patrón de diseño, el patrón builder (Constructor) es usado para permitir la creación de una variedad de objetos complejos desde un objeto fuente (Producto), el objeto fuente se compone de una variedad de partes que contribuyen individualmente a la creación de cada objeto complejo a través de un conjunto de llamadas a interfaces comunes de la clase Abstract Builder.

##ADB en android

Las siglas ADB significan Android Debug Bridge y se corresponden con una herramienta de software que nos permite interactuar con nuestro smartphone Android desde un PC. Así, por ejemplo, a través de ADB podemos ejecutar comandos para copiar archivos desde la computadora al teléfono o viceversa, flashear un revocery o el firmware completo e incluso reiniciar el dispositivo en modo recovery. 

Básicamente, en el ADB es la manera de cambiar profundamente el software de nuestro smartphone o por lo menos acceder a él. Por supuesto, todo esto se hace posible a través de un cable USB con el que conectamos el smartphone a la computadora. 

##Operador final en Java

En una aplicación posiblemente nos encontremos con algún valor que permanece constante durante la ejecución. Podemos definirla como una variable común pero perderíamos el control. Por allí, en algún descuido, se cambiaría de valor pero no nos enteraríamos. Podemos agregar a la definición de la variable el modificador final, que indica que a esa variable solo se le puede asignar un valor u objeto una única vez. La sintaxis es la siguiente:

```java
final tipo_variable nombre_de_variable = valor;
```

##Sobrecarga de Operadores

La sobrecarga de operadores es uno de los mecanismos que nos permite ampliar las capacidades de los lenguajes de programación orientados a objetos. Algunos lenguajes que soportan ésta característica son:

* C
* C#
* C++
* Python
* Java

##Gradle

Es una herramienta para automatizar la construcción de nuestros proyectos, por ejemplo las tareas de compilación, testing, empaquetado y el despliegue de los mismos. Es muy flexible para la configuración, pero además ya tiene armadas las tareas para las mayoría de los proyectos por default. Esta herramienta es usado por grandes proyecto “Open Source” como “Spring”, “Hibernate”, y “Grails”.

##Inyección de Dependencias

En inglés Dependency Injection, es un patrón de diseño orientado a objetos, en el que se suministran objetos a una clase en lugar de ser la propia clase quien cree el objeto. El término fue acuñado por primera vez por Martin Fowler.














