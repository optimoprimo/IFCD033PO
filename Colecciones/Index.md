- [Ménu](../README.md)

# Colecciones

Java tiene dos grandes colecciones

- Collections
- Map

Collections se divide en 3 grandes colecciones:

- List
- Set
- Queue

Las implementaciones más usadas son:

- List -> ArrayList
- Set -> HashSet
- Queue -> LinkedList
- Map -> HashMap

Se inicializan utilizando el operador Diamante <> donde indicamos dentro de el la clase que queremos coleccionar.

El caso del mapa, necesitamos dos tipos de clases, una para la key y otro para el valor

````java
	List<String> lista = new ArrayList<>();
	Set<String> set = new HashSet<>();
	Queue<Integer> queue = new LinkedList<>();
	Map<String, Integer> mapa = new HashMap<>();
````

## Metodos cómunes

````java
import java.util.ArrayList;
import java.util.HashMap;
import java.util.HashSet;
import java.util.LinkedList;
import java.util.List;
import java.util.Map;
import java.util.Queue;
import java.util.Set;

public class Collecciones {

	public static void main(String[] args) {
		
		List<String> lista = new ArrayList<>();
		Set<String> set = new HashSet<>();
		Queue<Integer> queue = new LinkedList<>();
		Map<String, Integer> mapa = new HashMap<>();

		
		// Las listas permiten valores repetidos
		// Metodos para añadir
		lista.add("Un valor");
		lista.add("Otro valor");
		lista.add("Un utlimo valor");
		
		// Los set no permiten valores repetidos
		set.add("Un valor");
		set.add("Otro valor");
		set.add("Otro valor"); // al añadir este elemento, ya existe y no se añade a nuestro set
		
		// Las colas tambein pueden añadir elementos
		queue.add(1);
		queue.add(2);
		// Pero no se suele trabajar con estos metodos
		// para añadir un elemento a la a una cola se utiliza offer
		queue.offer(1);
		queue.offer(2);
		// para leer el siguiente elemnto de la cola
		// peek
		queue.peek(); // nos permite leer el siguiente registro a tratar
		
		// poll
		queue.poll(); // nos devuelve el siguiente elemento de la lista y lo elimina de la lista
		
		//Mapas
		// Se trata como un diccionario, almacenamos objetos y los podemos recuperar por su key
		mapa.put("uno", 1);
		mapa.put("dos", 2);
		// Para acceder a un elemento utilizaremos su key
		mapa.get("uno");
		
		
	}
	
}
````