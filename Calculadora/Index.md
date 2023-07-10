- [Menú](../README.md)

# Calculadora

Vamos a desarrollar nuestro primer proyecto. Será una calculadora que nos ayude a sumar, restar, multiplicar y dividir números.

Para ello tenemos que saber que tipos de variables tenemos:

| Nombre| Tipo de dato| Tamaño | valor por defecto| Conversión |
| --- | --- | --- | --- | --- |
| byte | números | de -128 a 127  | 0 | Byte.parseByte("") |
| short | números | de -32.768 a 32.767 | 0 | Short.parseShort("") |
| int | números | de -2^31 a 2^31-1 | 0 | Integer.parseInt("") |
| long | números | de -2^63 a 2^63-1 | 0L | Long.parseLong("") |
| float | números con decimal | 32 bits | 0.0f | Float.parseFloat("") |
| double | números con decimal | 64 bits | 0.0 | Double.parseDouble("")|
| char | cualquier caracter | unicode de 16 bits | 'u0000' | - |
| boolean | verdadero o falso | true o false | false | Boolean.parseBoolean("") |
| String | cadenas de texto | - | null | String.valueOf("") |

Ejemplos

````java
    public class Calculadora{
        public static void main (String[] args){
            byte variable1 = 1;
            short variable2 = 121;
            int variable3 = 1234;
            long variable4 = 4444L;
            float variable5 = 5.5f;
            double variable6 = 6.6;
            char caracter = 'A';
            String cadena = "Hola Mundo";
            
            byte variable7 = Byte.valueOf("1");
            short variable8 = Short.valueOf("1");
            int variable9 = Integer.valueOf("1");
            long variable10 = Long.valueOf("1");
            float variable11 = Float.valueOf("1");
            double variable12 = Double.valueOf("1");
            String cadena3 = String.valueOf(variable12);
        }
    }
````

Las variables se definen de la siguiente forma ->

- primero el tipo de dato (byte, short, int...)
- luego el nombre de la variable (siguiendo las reglas de nombres)
- por último el valor de la variable se puede asignar cuando se define o más tarde

````java
    int miNumero;
    miNumero = 10;
    int miNumero2 = 20;
````

## Operaciones

Una vez que sabemos que tipos de variables tenemos vamos a ver que tipo de operaciones tenemos:

| Tipo| Unario| Binario |
| --- | --- | --- |
| + | hace positivo un número | suma dos números |
| - | hace negativo un número | resta dos números |
| * | - | multiplica dos números |
| / | - | divide dos números |
| % | -| nos devuelve el resto de una división |

Ejemplos

````java
public class Calculadora {
	public static void main(String[] args) {
		// Defino dos variables
		double variable1 = 5.5;
		double variable2 = 3.3;

		// Probamos los diferentes operadores
		System.out.println("Suma de los dos números es igual a " + (variable1 + variable2));
		System.out.println("Resta de los dos números es igual a " + (variable1 - variable2));
		System.out.println("Multiplicación de los dos números es igual a " + (variable1 * variable2));
		System.out.println("Division de los dos números es igual a " + (variable1 / variable2));
		System.out.println("Modulo de los dos números es igual a " + (variable1 % variable2));

		// Probamos los operadores unarios
		double variable3 = -9;
		double variable4 = 5;

		System.out.println("Hacemos un número positivo ya negativo " + (-variable3));
		System.out.println("Hacemos un número negativo que ya era positivo " + (-variable4));
	}
}
````

Igual que en la vida real, las operaciones se realizan de derecha a izquierda, pero hay operadores que tienen una preferencia.

````java
public class Calculadora {
	public static void main(String[] args) {
		// Defino 3 variables
		double variable1 = 1;
		double variable2 = 2;
		double variable3 = 3;
		
		System.out.println("Los operadores de multiplicar y dividir se ejecutan antes que los de sumar y restar");
		System.out.println(variable1 + variable2 * variable3);
		
		System.out.println("Podemos hacer que se ejecute antes cosas incluyendolos entre paréntesis");
		System.out.println((variable1 + variable2) * variable3);
	}
}
````

Estos operadores solo funcionan con los valores númericos, con las cadenas de texto solo podemos utilizar el operador + y resulta la unión de las dos cadenas

````java
public class Calculadora {
	public static void main(String[] args) {
		// Defino 2 variables
		String variable1 = "Hola";
		String variable2 = "Mundo";
		
		System.out.println(variable1+variable2);
	}	
}
````

## Interactuar con la pantalla

````java
import java.util.Scanner;

public class Calculadora {
	public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
       
        System.out.println("Introduce un texto");  
        String miVariable = sc.nextLine(); 
        System.out.println("El texto introducido es "+ miVariable);
        
        int numero1 = sc.nextInt();
        System.out.println("Numero1: "+numero1);
        long numero2 = sc.nextLong();
        System.out.println("Numero2: "+numero2);
        double numero3 = sc.nextDouble();
        System.out.println("Numero3: "+numero3);

        sc.close();
	}	
}
````

````java
import javax.swing.JOptionPane;

public class Calculadora {
	public static void main(String[] args) {
		String myVariable = JOptionPane.showInputDialog("Introduce un texto");
		JOptionPane.showMessageDialog(null, myVariable);
        // nos obliga a hacer una cambio de tipos de variables para trabajar con números
	}	
}
````

## Ejercicio calculadora

Punto de partida 

````java
import javax.swing.JOptionPane;

public class Calculadora {
	public static void main(String[] args) {
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
		resultado = miNumero1 + miNumero2;
		JOptionPane.showMessageDialog(null, "La suma de ambos números es " + resultado);

		// Resta
		resultado = miNumero1 - miNumero2;
		JOptionPane.showMessageDialog(null, "La resta de ambos números es " + resultado);

		// Multiplicación
		resultado = miNumero1 * miNumero2;
		JOptionPane.showMessageDialog(null, "La multiplicación de ambos números es " + resultado);

		// División
		resultado = miNumero1 / miNumero2;
		JOptionPane.showMessageDialog(null, "La división de ambos números es " + resultado);
	}

}
````

Divideremos la funcionalidad en funciones.

- [Bucles](../Bucles/Index.md)

### Curso 26/06/2023

````java
	// orden ejecutar funciones
	Operacion ope = new Operacion();
	ope.elegirOpcion();
	ope.rellenarCampos();
	ope.comprobarOpcion();
````

````java 
package Modelo;

import javax.swing.JOptionPane;

public class Operacion {

	private double numeroUno;
	private double numeroDos;

	private int respuestaNumerica;

	public Operacion() {
	}

	public double getNumeroUno() {
		return numeroUno;
	}

	public void setNumeroUno(double numeroUno) {
		this.numeroUno = numeroUno;
	}

	public double getNumeroDos() {
		return numeroDos;
	}

	public void setNumeroDos(double numeroDos) {
		this.numeroDos = numeroDos;
	}

	public void rellenarCampos() {
		String parametro = JOptionPane.showInputDialog("Introduce el primer numero");
		numeroUno = Double.parseDouble(parametro);
		String parametro2 = JOptionPane.showInputDialog("Introduce el segundo número");
		numeroDos = Double.parseDouble(parametro2);
	}

	public void sumar() {
		JOptionPane.showMessageDialog(null, "El resultado de la suma de los dos números es " + (numeroUno + numeroDos));
	}

	public void restar() {
		JOptionPane.showMessageDialog(null,
				"El resultado de la resta de los dos números es " + (numeroUno - numeroDos));
	}

	public void multiplicar() {
		JOptionPane.showMessageDialog(null,
				"El resultado de la multiplicación de los dos números es " + (numeroUno * numeroDos));
	}

	public void dividir() {
		JOptionPane.showMessageDialog(null,
				"El resultado de la división de los dos números es " + (numeroUno / numeroDos));
	}

	public void elegirOpcion() {
		String enunciado;
		enunciado = "Introduce una opcion \n 1-sumar \n 2-restar \n 3-multiplicar \n 4-dividir \n 5-salir";

		String respuesta;
		respuesta = JOptionPane.showInputDialog(enunciado);

		respuestaNumerica = Integer.parseInt(respuesta);
	}

	public void comprobarOpcion() {
		if (respuestaNumerica > 0 && respuestaNumerica < 5) {
			switch (respuestaNumerica) {
			case 1:
				sumar();
				break;
			case 2:
				restar();
				break;
			case 3:
				multiplicar();
				break;
			case 4:
				dividir();
				break;
			}
		} else {
			if (respuestaNumerica == 5) {
				JOptionPane.showMessageDialog(null, "Adios");
			} else {
				JOptionPane.showMessageDialog(null, "Me has dado una opción no valida");
			}
		}
	}

	@Override
	public String toString() {
		return "Operacion [numeroUno=" + numeroUno + ", numeroDos=" + numeroDos + "]";
	}

}
````



````java
package Vista;

import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JOptionPane;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;

public class PantallaCalculadora extends JFrame {

	private JPanel contentPane;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {

		PantallaCalculadora frame = new PantallaCalculadora();
		frame.setVisible(true);

	}

	/**
	 * Create the frame.
	 */
	public PantallaCalculadora() {
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 450, 300);
		contentPane = new JPanel();
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));

		setContentPane(contentPane);
		contentPane.setLayout(null);

		JButton btnNewButton = new JButton("New button");
		btnNewButton.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				JOptionPane.showMessageDialog(btnNewButton, "Acción");
			}
		});
		btnNewButton.setBounds(237, 22, 89, 23);
		contentPane.add(btnNewButton);
	}
}

````
