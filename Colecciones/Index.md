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
