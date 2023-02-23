- [Menú](../README.md)

# Clases y Objetos

Para crear un objeto de una clase lo hacemos atraves del operardor new

````java
	Persona paco = new Persona();
````

Esto llama al constructor de nuestra clase


````java
	public class Persona {

        private String sexo = "indefinido";
        private Integer piernas = 2;
        private Integer brazos = 2;

        public Persona() {
        }
    }
````

