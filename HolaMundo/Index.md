- [Ménu](../README.md)

# Hola Mundo

## Opciones al crear nuestro proyecto Java

<img alt="PNG" src="../Imagenes/HolaMundo/Opciones.PNG" />

- Proyect name: "HolaMundo" sera el nombre de nuestro proyecto
- JRE: sera la versión que utilizaremos. En este caso utilizaremos la 17
- Module: desmarcarmos esta opción. Esto hara que no nos genere un module-info para nuestro proyecto.

## Estructura del proyecto

- HolaMundo
  - JRE System Library
  - src

JRE son las apis basicas de java, y src es el directorio donde crearemos nuestro clases java.

## Crearemos nuestra primera clase

File -> new -> Class

<img alt="PNG" src="../Imagenes/HolaMundo/NuevaClase.PNG" />

Por ahora solo le daremos nombre a nuestra clase y la crearemos con las opciones por defecto.

```java
    public class HolaMundo {

    }
````

Por defecto, las aplicaciones java tiene una función inicial (main) que es punto de inicio de la aplicación. La syntaxis de la función siempre es la misma ->

```java
    public static void main (String[] args) {

    }
````
y se lo añadiremos a nuestra clase junto con un mensaje para decir "Hola Mundo"

```java
    public class HolaMundo {
        public static void main (String[] args) {
    	        System.out.print("Hola Mundo");
            }
    }
````

## Ejecutar el programa

Originalmente habria que compilar la clase y luego ejecutarla con los comandos javac y java. Pero el ide nos ayuda a desarrollar y se encarga por nostros.
Flecha verde.

## Bonus

Si queremos ejecutar nuestra Hola Mundo de una forma más grafica.

```java
import javax.swing.JOptionPane;

public class HolaMundo {
    public static void main (String[] args) {
    	JOptionPane.showMessageDialog(null, "Hola Mundo");
    }
}
````

El import trae a nuestra clase el codigo necesario para poder ejecutar la función que queremos
