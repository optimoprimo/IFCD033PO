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