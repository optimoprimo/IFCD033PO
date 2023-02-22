- [Menú](../README.md)

# Bucles

````java

public class Bucles {

	public static void main(String[] args) {

		// bucle for
		for (int i = 0; i < 100; i++) {
			System.out.println("Bucle for " + i);
		}

		// bucle while
		int j = 0;
		while (j < 100) {
			System.out.println("Bucle while " + j);
			j++;
		}

		// bucle do while
		int k = 0;
		do {
			System.out.println("Bucle do while " + k);
			k++;
		} while (k < 100);

		// zip - zap - zip-zap
		for (int i = 1; i <= 100; i++) {
			if (i % 3 == 0 && i % 5 == 0) {
				System.out.println("zip-zap");

			} else {
				if (i % 3 == 0) {
					System.out.println("zip");

				} else {
					if (i % 5 == 0) {
						System.out.println("zap");

					} else {
						System.out.println("Bucle for " + i);

					}
				}
			}
		}
		
		
	}
}
````

## Punto de partida

````java
import javax.swing.JOptionPane;

public class Calculadora {
	public static void main(String[] args) {
		// Menú con opciones
		String mensaje = JOptionPane
				.showInputDialog("Elija una opción \n 1-Sumar \n 2-Restar \n 3-Multiplicar \n 4-Dividir");
		int opcion = Integer.parseInt(mensaje);

		// pedimos los datos
		String miVariable1 = JOptionPane.showInputDialog("Introduce el primer número");
		String miVariable2 = JOptionPane.showInputDialog("Introduce el segundo número");

		// cambio las variables a tipo double
		double miNumero1;
		double miNumero2;
		miNumero1 = Double.parseDouble(miVariable1);
		miNumero2 = Double.parseDouble(miVariable2);

		// realizamos las operaciones
		// Suma
		double resultado;
		if (opcion == 1) {
			resultado = sumar(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La suma de ambos números es " + resultado);
		}

		// Resta
		if (opcion == 2) {
			resultado = restar(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La resta de ambos números es " + resultado);
		}

		// Multiplicación
		if (opcion == 3) {
			resultado = multiplicar(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La multiplicación de ambos números es " + resultado);
		}
		// División
		if (opcion == 4) {
			resultado = dividir(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La división de ambos números es " + resultado);
		}
	}

	public static double sumar(double num1, double num2) {
		return num1 + num2;
	}

	public static double restar(double num1, double num2) {
		return num1 - num2;
	}

	public static double multiplicar(double num1, double num2) {
		return num1 * num2;
	}

	public static double dividir(double num1, double num2) {
		return num1 / num2;
	}
}
````

# punto partida con switch

````java
import javax.swing.JOptionPane;

public class Calculadora {
	public static void main(String[] args) {
		// Menú con opciones
		String mensaje = JOptionPane
				.showInputDialog("Elija una opción \n 1-Sumar \n 2-Restar \n 3-Multiplicar \n 4-Dividir");
		int opcion = Integer.parseInt(mensaje);

		// pedimos los datos
		String miVariable1 = JOptionPane.showInputDialog("Introduce el primer número");
		String miVariable2 = JOptionPane.showInputDialog("Introduce el segundo número");

		// cambio las variables a tipo double
		double miNumero1;
		double miNumero2;
		miNumero1 = Double.parseDouble(miVariable1);
		miNumero2 = Double.parseDouble(miVariable2);

		// realizamos las operaciones
		// Suma
		double resultado;
		
		// con un switch
		switch (opcion) {
		case 1:
			resultado = sumar(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La suma de ambos números es " + resultado);
			break;
		case 2:
			resultado = restar(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La resta de ambos números es " + resultado);
			break;
		case 3:
			resultado = multiplicar(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La multiplicación de ambos números es " + resultado);
			break;
		case 4:
			resultado = dividir(miNumero1, miNumero2);
			JOptionPane.showMessageDialog(null, "La división de ambos números es " + resultado);
			break;
		default:
			break;
		}
	}

	public static double sumar(double num1, double num2) {
		return num1 + num2;
	}

	public static double restar(double num1, double num2) {
		return num1 - num2;
	}

	public static double multiplicar(double num1, double num2) {
		return num1 * num2;
	}

	public static double dividir(double num1, double num2) {
		return num1 / num2;
	}
}
````