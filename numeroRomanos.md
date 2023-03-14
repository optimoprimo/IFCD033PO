````java

public class Inicio {

	public static void main(String[] args) {

		// Dado un número del 1 al 10
		// sacarlo por pantalla
		// en numeros romanos
		int numero = 49;
		while (numero >= 0) {
			if (numero >= 50) {
				System.out.print("L");
				numero -= 50;
				continue;
			}
			if (numero >= 40) {
				System.out.print("XL");
				numero -= 40;
				continue;
			}
			
			if (numero >= 10) {
				System.out.print("X");
				numero -= 10;
				continue;
			}
			if (numero == 9) {
				System.out.print("IX");
				numero -= 9;
				continue;
			}
			if (numero >= 5) {
				System.out.print("V");
				numero -= 5;
				continue;
			}
			if (numero == 4) {
				System.out.print("IV");
				numero -= 4;
				continue;
			}
			if (numero >= 1) {
				System.out.print("I");
				numero -= 1;
				continue;
			}
		}

//		switch (numero) {
//		case 1:
//			System.out.print("I");
//			break;
//		case 2:
//			System.out.print("II");
//			break;
//		case 3:
//			System.out.print("III");
//			break;
//		case 4:
//			System.out.print("IV");
//			break;
//		case 5:
//			System.out.print("V");
//			break;
//		case 6:
//			System.out.print("VI");
//			break;
//		case 7:
//			System.out.print("VII");
//			break;
//		case 8:
//			System.out.print("VIII");
//			break;
//		case 9:
//			System.out.print("IX");
//			break;
//		case 10:
//			System.out.print("X");
//			break;
//		}

		/*
		 * 1 -> I 2 -> II 3 -> III 4 -> IV 5 -> V 6 -> VI 7 -> VII 8 -> VIII 9 -> IX
		 * 10-> X 11-> XI 40-> XL 50-> L
		 */

//		String[] array = { "", "I", "II", "III", "IV", "V", "VI", "VII", "VIII", "IX", "X" };
//		System.out.print(array[numero]);
	}

}


````
