- [Ménu](../README.md)

# Colecciones

Las colecciones de Java se dividen en cuatro tipos principales: List, Set, Queue y Map. A continuación se describen las principales diferencias entre ellos, así como algunos ejemplos de cada uno:

- List:
	- Una colección ordenada de elementos que permite duplicados.
	- Permite acceder a los elementos por índice.
	- Se pueden insertar o eliminar elementos en cualquier posición de la lista.
	- Ejemplo: ArrayList, LinkedList
- Set:
	- Una colección que no permite duplicados y no tiene orden.
	- Los elementos se pueden agregar o eliminar de un conjunto.
	- Se pueden utilizar operaciones matemáticas de conjuntos como la unión, la intersección y la diferencia para manipular los elementos del conjunto.
	- Ejemplo: HashSet, TreeSet
- Queue:
	- Una colección ordenada de elementos que permite duplicados.
	- Los elementos se insertan al final de la cola y se eliminan del principio de la cola (FIFO).
	- Ejemplo: LinkedList, PriorityQueue
- Map:
	- Una colección de pares clave-valor que no permite claves duplicadas.
	- Los elementos se pueden agregar, eliminar y buscar por clave.
	- Se pueden utilizar operaciones matemáticas de mapas como la unión y la intersección para manipular los elementos del mapa.
	- Ejemplo: HashMap, TreeMap


# ejemplos
````java 

List<String> lista = new ArrayList<>();
lista.add("manzana");
lista.add("banana");
lista.add("cereza");
System.out.println(lista.get(1)); // salida: "banana"
lista.remove(0);
System.out.println(lista); // salida: "[banana, cereza]"

Set<String> conjunto = new HashSet<>();
conjunto.add("manzana");
conjunto.add("banana");
conjunto.add("cereza");
conjunto.add("banana"); // no se agregará porque es un duplicado
System.out.println(conjunto); // salida: "[cereza, banana, manzana]"


Queue<String> cola = new LinkedList<>();
cola.add("manzana");
cola.add("banana");
cola.add("cereza");
System.out.println(cola.peek()); // salida: "manzana"
cola.remove();
System.out.println(cola); // salida: "[banana, cereza]"


Map<String, String> mapa = new HashMap<>();
mapa.put("nombre", "Juan");
mapa.put("apellido", "Pérez");
System.out.println(mapa.get("nombre")); // salida: "Juan"
mapa.remove("apellido");
System.out.println(mapa); // salida: "{nombre=Juan}"

````


````java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class Listas {

	public static void main(String[] args) {
		// repaso colleciones
		// Collections

		List<Integer> lista = new ArrayList<>();
		// añadir elementos
		lista.add(1); // [ 1 ]
		lista.add(1); // [ 1, 1]
		lista.add(10);// [ 1, 1, 10]
		// recuperar elementos
		System.out.println(lista.get(2));
		// modificar
		lista.set(1, 3);// [ 1, 3, 10]
		// eliminar
		lista.remove(0);// [ 3, 10]

		System.out.println(lista);
		for (int i = 0; i < lista.size(); i++) {
			System.out.println(lista.get(i));
		}

		// Hacemos una lista de números
		List<Integer> listaNumeros = new ArrayList<>();
		listaNumeros.add(10);
		listaNumeros.add(100);
		listaNumeros.add(50);
		listaNumeros.add(1000);
		listaNumeros.add(20);

		// sacamos el número más grande
		// en este caso 1000
		Integer aux = 0;
		for (int i = 0; i < listaNumeros.size(); i++) {
			Integer valor = listaNumeros.get(i);
			if(valor> aux) {
				aux = valor;
			}
		}
		System.out.println(aux);
		// Intentad sacar el segundo más bajo
		
		Collections.sort(listaNumeros);
		System.out.println(listaNumeros.get(1));

		List<String> listaNumerosString = new ArrayList<>();
		listaNumerosString.add("10");
		listaNumerosString.add("100");
		listaNumerosString.add("50");
		listaNumerosString.add("1000");
		listaNumerosString.add("20");
		
		listaNumerosString.sort((a,b)->{
			Integer a1 =Integer.parseInt(a);
			Integer b1 = Integer.parseInt(b);
			return b1.compareTo(a1);
		});
		System.out.println(listaNumerosString.get(1));
		
		List<String> miLista3 = new ArrayList<>();
		miLista3.add("10");
		miLista3.add("100");
		miLista3.add(null);
		miLista3.add("1000");
		miLista3.add("20");
		// Eliminar los elementos nulos
	}

}

````
