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
import java.math.BigInteger;
import java.security.Timestamp;
import java.time.LocalDate;
import java.time.LocalDateTime;
import java.time.LocalTime;
import java.time.ZonedDateTime;

public class Inicio {

	public static int numero10 = 10;

	public static void main(String[] args) {
		String texto = "Hola mundo que tal estas";
		char valor = 'A';
		char[] arrayChar = { 'H', 'o', 'l', 'a' };
		// comprobar antes de llamar a un metodo
		// que es diferente de null
		if (texto != null) {
			// ChartAt para sacar un caracter
			// System.out.print(texto.charAt(0));
			// System.out.print(texto.substring(5,10));
			// System.out.print(texto.toLowerCase());
			// System.out.print(texto.contains("Mundo"));
//			System.out.print(texto.indexOf("o"));
//			System.out.print(texto.lastIndexOf("o"));
			// System.out.print(texto.endsWith(".pdf"));
			// System.out.print(texto.equalsIgnoreCase("hola"));
			// System.out.print(texto.length());

//			String[] array = texto.split(" ");
//			for(String x : array) {
//				System.out.println(x);
//			}
		}

		// Notacion snake
		String texto_para_concatenar;

		// Notacion CamelCase
		String textoParaConcatenar;

		// dado un String
		// saber si es un palindromo
		// si leido de delante para atras
		// es igual de atras a adelante
		String ejercicio = "ana lleva aal oso la avellana";
		ejercicio = ejercicio.replaceAll(" ", "");
		// System.out.print(ejercicio);

		int posicionIzquierda = 0;
		int posicionDerecha = ejercicio.length() - 1;
		boolean esPalindromo = true;
		while (posicionDerecha >= 0) {
			if (ejercicio.charAt(posicionIzquierda) != ejercicio.charAt(posicionDerecha)) {
				// los valores no son iguales
				esPalindromo = false;
				// salimos del bucle
				break;
			}
			posicionDerecha--;
			posicionIzquierda++;
		}
		// if (esPalindromo) {
//		if (esPalindromo == true) {
//			System.out.println("es palindromo");
//		} else {
//			System.out.println("No es palindromo");
//		}

//		String texto1 = "texto1";
//		String copiaTexto1 =new String("texto1");
//		
//		System.out.print(texto1==copiaTexto1);

		Integer numero = -129;
		Integer copiaNumero1 = -129;
		// System.out.print(numero);

		numero = new Integer(1);
		numero = Integer.valueOf(1);

		boolean verdaderoFalso;
		Boolean objetoBoolena = null;

		// Fechas
		LocalDate anoMesDia;
		anoMesDia = LocalDate.of(2023, 3, 13);
		anoMesDia = LocalDate.now();
		// System.out.print(anoMesDia);
		LocalTime horaMinutosSegundos;
		horaMinutosSegundos = LocalTime.of(12, 12, 12);
		horaMinutosSegundos = LocalTime.now();
		//System.out.print(horaMinutosSegundos);
		
		LocalDateTime todoJunto;
		todoJunto = LocalDateTime.now();
		//System.out.println(todoJunto.plusDays(-5));
	
		boolean palindromo = false;
//		if( true == palindromo) {
//			System.out.println("entro");
//		}else {
//			System.out.println("no entro");
//		}
		
		// Numeros altos
		BigInteger numero2 = new BigInteger("31251324123413241233412341234");
	
		// Otros tipo fecha
//		Date date = new Date();
//		Timestamp
		StringBuilder st = new StringBuilder();
		st.append("Hola");
		st.append(" mundo");
		st.insert(0, "por delante ");	
		st.delete(0, 5);
		System.out.print(st);
	}

}

````
