- [Ménu](../README.md)

# Calculadora

Vamos a desarrollar nuestro primer proyecto. Sera una claculadora que nos ayude a sumar, restar, multiplicar y dividor números.

Para ello tenemos que saber que tipos de variables tenemos:

| Nombre| Tipo de dato| Tamaño | valor por defecto|
| --- | --- | --- | --- |
| byte | números | de -128 a 127  | 0 |
| short | números | de -32.768 a 32.767 | 0 |
| int | números | de -2^31 a 2^31-1 | 0 |
| long | números | de -2^63 a 2^63-1 | 0L |
| float | números con decimal | 32 bits | 0.0f |
| double | números con decimal | 64 bits | 0.0 |
| char | cualquier caracter | unicode de 16 bits | 'u0000' |
| boolean | verdadero o falso | true o false | false |
| String | cadenas de texto | - | null |

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
´´´´
