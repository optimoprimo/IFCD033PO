# IFCD033PO
Formación JAVA

## Programación de aplicaciones con Java

- [Introducción](Introducción/Index.md)
- [Características de Java](Caracteristicas/Index.md)
- [Instalación](Instalación/Index.md)
- [HolaMundo](HolaMundo/Index.md)
- [Calculadora](Calculadora/Index.md)
- [Bucles](Bucles/Index.md)
- [Objetos](Objetos/Index.md)
- [Colecciones](Colecciones//Index.md)
- [IO-NIO](IO-NIO/Index.md)
- [BBDD](bbdd/Index.md)
- [Ejercicios](Ejercicios//Index.md)


Borrador

````java

public class Inicio {

	public static int numero10 = 10;
	
	public static void main(String[] args) {
		String texto = "Hola mundo que tal estas";
		char valor = 'A';
		char[] arrayChar = {'H','o','l','a'};
		// comprobar antes de llamar a un metodo
		// que es diferente de  null
		if(texto != null) {
			// ChartAt para sacar un caracter
			//System.out.print(texto.charAt(0));
			//System.out.print(texto.substring(5,10));
			//System.out.print(texto.toLowerCase());
			//System.out.print(texto.contains("Mundo"));
//			System.out.print(texto.indexOf("o"));
//			System.out.print(texto.lastIndexOf("o"));
			//System.out.print(texto.endsWith(".pdf"));
			//System.out.print(texto.equalsIgnoreCase("hola"));
			//System.out.print(texto.length());
			
			String[] array = texto.split(" ");
			for(String x : array) {
				System.out.println(x);
			}
		}
		
		// Notacion snake
		String texto_para_concatenar;
		
		// Notacion CamelCase
		String textoParaConcatenar;

		// dado un String
		// saber si es un palindromo
		// si leido de delante para atras
		// es igual de atras a adelante
		String ejercicio = 
				"ana lleva al oso la avellana";
	}

}

````
