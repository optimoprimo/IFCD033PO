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
