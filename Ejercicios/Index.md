- [Ménu](../README.md)

# Ejercicios

## Operaciones

### Operaciones 1

Crearemos dos variables numéricas primitivas (byte, short, int ...) y probaremos a sumarlas, restarlas, dividirlas, multiplicarlas y guardarlas en una tercera variable.

### Operaciones 2

Crearemos dos variables numericos Objeto (Byte, Short, Integer ...) y probaremos a sumarlas, restarlas, dividirlas, multiplicarlas y guardarlas en una tercera variable.

### Operaciones 3

Dada una variable numérica, cambiarle el signo. Si es + hacerla -.

<details><summary>Respuesta</summary>
````java
		Integer var = 10;
		//cambiamos de signo con el operador - 
		System.out.print(-var);
````
</details>

### Operaciones 4

Calcular el resto de una división. 29/7 el resto debería dar 1.

<details><summary>Respuesta</summary>
````java
		// Calculamos el modulo de una división con el operador %
		System.out.print(29%7);
````
</details>

## String

### String 1

Dado un texto, mostar por pantalla si contiene una 'a'

<details><summary>Respuesta</summary>
````java
		String var = "Hola Mundo";
		System.out.print(var.concat("a"));
````
</details>

### String 2

Dado un texto, mostar por pantalla si empieza por 'a'

<details><summary>Respuesta</summary>
````java
		String var = "Hola Mundo";
		System.out.print(var.startsWith("a"));
````
</details>

### String 3

Dado un texto, mostar por pantalla si termina por 'a'

<details><summary>Respuesta</summary>
````java
		String var = "Hola Mundo";
		System.out.print(var.endsWith("a"));
````
</details>

### String 4

Dado un texto, mostar por pantalla su ultimas dos letras

<details><summary>Respuesta</summary>
````java
		String var = "Hola Mundo";
		System.out.print(var.substring(var.length()-2));
````
</details>

## Bucles

### Bucles 1

Mostraremos por pantalla los primeros 50 números desde 0 al 50;

<details><summary>Respuesta</summary>
````java
		for (int i = 0; i <=50 ; i ++) {
			System.out.println(i);
		}
````
</details>

### Bucles 2

Mostraremos por pantalla los primeros 50 números desde 50 al 0;

<details><summary>Respuesta</summary>
````java
		for (int i = 50; i >= 0 ; i --) {
			System.out.println(i);
		}
````
</details>

### Bucles 3

Mostraremos por pantalla un mensaje que pida un campo hasta que tecleen por pantalla "salir"

- Diferenciar Mayusculas y minusculas

<details><summary>Respuesta</summary>
  - Ver ejercicio piedra, papel y tijera
</details>

### Bucles - Operaciones 4

Calcular el factorial de un número

<details><summary>Respuesta</summary>

````java
		Integer numero = 5;
		Integer respeusta= 1;
		for (int i = numero; i > 1 ; i --) {
			respeusta *= i;
		}
		System.out.println(respeusta);
````

</details>

## Objetos

### Objetos 1

Crear una clase "Avion" y definir los atributos

- numero pasajeros
- aerolinia

### Objetos 2

Crear una clase "Piloto" y definir los atributos

- nombre
- edad
- cargo

### Objetos y listas 3

Crear sobre la clase "Avion" un atributo para almacenar varios "Pilotos"

## Listas

### Listas 1

Crear una lista de textos y mostrar ordenados alfabéticamente

### Listas 2

Crear una lista de "Pilotos" y mostrarla ordenados por el campo Nombre

### Ejercicio Piedra Papel o Tijera

````java
import javax.swing.JOptionPane;

public class Errores {

	public static void main(String[] args) {
		// 1 - piedra
		// 2 - papel
		// 3 - tijeras
		
		JOptionPane.showConfirmDialog(null, "una opcion");
		
		Integer opcion = pedirTexto();
		Integer opcion2 = opcionOrdenador();
		
		System.out.print(opcion);
		System.out.print(opcion2);
		
		String mensaje = "perder";
		
		if(opcion.equals(opcion2)) {
			mensaje = "empate";
		}
		if(opcion.equals(1) && opcion2.equals(3)) {
			mensaje = "ganar";
		}
		if(opcion.equals(2) && opcion2.equals(1)) {
			mensaje = "ganar";
		}
		if(opcion.equals(3) && opcion2.equals(2)) {
			mensaje = "ganar";
		}
		
		devolverMensaje(mensaje);
	}

	public static Integer pedirTexto() {
		Integer opcion;
		do {
			try {

				String texto = JOptionPane.showInputDialog("Elige una opción \n 1-Piedra \n 2-Papel \n 3-Tijera", null);
				opcion = Integer.parseInt(texto);
				if (opcion.equals(1) || opcion.equals(2) || opcion.equals(3)) {
					return opcion;
				} else {
					JOptionPane.showMessageDialog(null, "No me has metido una opcion valida");
				}

			} catch (Exception e) {
				JOptionPane.showMessageDialog(null, "Ehhhh no me has metido un número");
			}
		} while (true);
	}

	public static void devolverMensaje(String variable) {

		switch (variable) {
		case "ganar": {
			JOptionPane.showMessageDialog(null, "Has ganado");
			break;
		}
		case "perder": {
			JOptionPane.showMessageDialog(null, "Has perdido");
			break;
		}
		case "empate": {
			JOptionPane.showMessageDialog(null, "Has empatado");
			break;
		}

		}
	}

	public static Integer opcionOrdenador() {
		
			Double numero = Math.random();

			if (numero < 0.3) {
				return 1;
			}

			if (numero < 0.6) {
				return 2;
			}

			if (numero < 0.9) {
				return 3;
			}
		
			return opcionOrdenador();

	}
}
````
