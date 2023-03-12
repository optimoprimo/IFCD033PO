- [Menú](../README.md)

# IO y NIO


## Ejemplo BufferedReader

En este ejemplo, se utiliza la clase BufferedReader para leer el contenido del archivo línea por línea. En el bloque try-with-resources, se crea un objeto BufferedReader y se lo inicializa con un objeto FileReader que representa al archivo que se quiere leer.

Luego, se utiliza un bucle while para recorrer cada línea del archivo y se imprime por consola. Finalmente, el bloque catch maneja cualquier excepción que pueda ocurrir durante la lectura del archivo.

````java 

import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class LeerArchivo {

    public static void main(String[] args) {
        String rutaArchivo = "ruta_del_archivo"; // Cambiar por la ruta de tu archivo
        
        try (BufferedReader bufferedReader = new BufferedReader(new FileReader(rutaArchivo))) {
            String lineaActual;
            while ((lineaActual = bufferedReader.readLine()) != null) {
                System.out.println(lineaActual);
            }
        } catch (IOException e) {
            System.out.println("Error al leer el archivo.");
            e.printStackTrace();
        }
    }

}

````

## Ejemplo BufferedWriter

En este ejemplo, se utiliza la clase BufferedWriter para escribir en un archivo. En el bloque try-with-resources, se crea un objeto BufferedWriter y se lo inicializa con un objeto FileWriter que representa al archivo en el que se quiere escribir.

Luego, se escribe el texto en el archivo utilizando el método write() del objeto BufferedWriter. Finalmente, el bloque catch maneja cualquier excepción que pueda ocurrir durante la escritura del archivo.

````Java
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;

public class EscribirArchivo {

    public static void main(String[] args) {
        String rutaArchivo = "ruta_del_archivo"; // Cambiar por la ruta de tu archivo
        
        try (BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(rutaArchivo))) {
            String textoAEscribir = "Este es el texto que quiero escribir en el archivo.";
            bufferedWriter.write(textoAEscribir);
        } catch (IOException e) {
            System.out.println("Error al escribir en el archivo.");
            e.printStackTrace();
        }
    }

}
````

### ¿Que es el try-with-resource?

Un recurso en Java es un objeto que necesita ser cerrado una vez que se ha terminado de usar, como un archivo, una conexión de red o una base de datos. El problema con la gestión de recursos en bloques try-catch es que, si no se cierra el recurso correctamente, puede generar problemas en el programa o en el sistema operativo.

````Java
try (/* inicialización de recursos */) {
    // código que usa los recursos
} catch (/* excepciones */) {
    // manejo de excepciones
}
````

En lugar de inicializar el recurso fuera del bloque try, como se hace en un bloque try-catch normal, se inicializa dentro de los paréntesis del try. Esto hace que los recursos sean automáticamente cerrados al final del bloque try, sin importar si el código dentro del bloque genera una excepción o no.

Es importante tener en cuenta que los recursos deben implementar la interfaz AutoCloseable o Closeable para poder ser utilizados con try-with-resources. Esto se debe a que estas interfaces proporcionan los métodos close() necesarios para cerrar el recurso de manera segura.

En resumen, try-with-resources es una forma conveniente y segura de manejar recursos en Java, ya que garantiza que los recursos se cierren correctamente sin importar las excepciones que se generen dentro del bloque try.


## Escribir y recuperar Objetos

Clase Persona a serializar

En Java, Serializable es una interfaz que se utiliza para marcar una clase como "serializable", lo que significa que sus objetos se pueden convertir en una secuencia de bytes que luego se pueden almacenar en un archivo, enviar a través de una red o guardar en cualquier otro medio de almacenamiento.

````Java

class Persona implements Serializable {
    private String nombre;
    private String apellido;
    private int edad;
    
    public Persona(String nombre, String apellido, int edad) {
        this.nombre = nombre;
        this.apellido = apellido;
        this.edad = edad;
    }
    
    public String getNombre() {
        return nombre;
    }
    
    public String getApellido() {
        return apellido;
    }
    
    public int getEdad() {
        return edad;
    }
    
    @Override
    public String toString() {
        return nombre + " " + apellido + " (" + edad + ")";
    }
}
````

````Java

import java.io.*;

public class GuardarYRecuperarObjeto {

    public static void main(String[] args) {
        String rutaArchivo = "ruta_del_archivo"; // Cambiar por la ruta de tu archivo
        
        // Objeto a guardar en el archivo
        Persona personaAGuardar = new Persona("Juan", "Pérez", 25);
        
        try (ObjectOutputStream objectOutputStream = new ObjectOutputStream(new FileOutputStream(rutaArchivo))) {
            // Escribir objeto en el archivo
            objectOutputStream.writeObject(personaAGuardar);
        } catch (IOException e) {
            System.out.println("Error al guardar el objeto en el archivo.");
            e.printStackTrace();
        }
        
        try (ObjectInputStream objectInputStream = new ObjectInputStream(new FileInputStream(rutaArchivo))) {
            // Leer objeto del archivo
            Persona personaLeida = (Persona) objectInputStream.readObject();
            System.out.println("Persona leída del archivo: " + personaLeida);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error al leer el objeto del archivo.");
            e.printStackTrace();
        }
    }

}

````