- [Ménu](../README.md)

# Calculadora

Vamos a desarrollar nuestro primer proyecto. Sera una claculadora que nos ayude a sumar, restar, multiplicar y dividor números.

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
        }
    }
````

Las variables se definen de la siguiente forma ->

- primero el tipo de dato (byte, short, int...)
- luego el nombre de la variable (siguiendo las reglas de nombres)
- por ultimo el valor de la variable se puede asignar cuando se define o más tarde

````java
    int miNumero;
    miNumero = 10;
    int miNumero2 = 20;
````

## Operaciones

Una vez que sabemos que tipos de variables tenemos vamos a ver que tipo de operaciones tenemos:

| Tipo| Unario| BInario |
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
		
		System.out.println("Los operadores de multiplicar y dividir se ejectuan antes que los de sumar y restar");
		System.out.println(variable1 + variable2 * variable3);
		
		System.out.println("Podemos hacer que se ejecute antes cosas incluyendolos entre parentesis");
		System.out.println((variable1 + variable2) * variable3);
	}
}
````

Estos operadores solo funcionan con los valores numericos, con las cademas de texto solo podemos utilizar el operador + y resulta la unión de las dos cadenas

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
