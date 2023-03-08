````java

import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.FileReader;
import java.io.IOException;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;

public class EscribirObjetos {

	public static void main(String[] args) throws IOException, ClassNotFoundException {

		String ruta = "C:\\Users\\INSTALADOR\\Desktop\\archivos\\noExiste\\objetos.data";

		Animal tigre = new Animal("Tigre");
		Animal leon = new Animal("León");
		Animal pajaro = new Animal("Pajaro");
		
		Coche mercedes = new Coche("Mercedes");

		FileOutputStream output = new FileOutputStream(ruta);
		ObjectOutputStream escribir = new ObjectOutputStream(output);

		escribir.writeObject(tigre);
		escribir.writeObject(leon);
		escribir.writeObject(pajaro);
		escribir.writeObject(mercedes);

		escribir.close();

		FileInputStream input = new FileInputStream(ruta);
		ObjectInputStream leer = new ObjectInputStream(input);

		try {
			Object animal = (Animal) leer.readObject();
			
			if(animal instanceof Animal) {
				System.out.print("es un animal");
			}
			
			while (animal != null) {
				Animal animalVerdadero = (Animal) animal;
				System.out.println(animalVerdadero.getNombre());
				animal = leer.readObject();
			}
		} catch (Exception e) {
			// TODO: handle exception
		}

		leer.close();
	}

}

````

````java
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.FileReader;
import java.io.IOException;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;

public class EscribirObjetos {

	public static void main(String[] args) throws IOException, ClassNotFoundException {

		String ruta = "C:\\Users\\INSTALADOR\\Desktop\\archivos\\noExiste\\objetos.data";

		Animal tigre = new Animal("Tigre");
		Animal leon = new Animal("León");
		Animal pajaro = new Animal("Pajaro");
		
		Coche mercedes = new Coche("Mercedes");

		FileOutputStream output = new FileOutputStream(ruta);
		ObjectOutputStream escribir = new ObjectOutputStream(output);

		escribir.writeObject(tigre);
		escribir.writeObject(leon);
		escribir.writeObject(pajaro);
		escribir.writeObject(mercedes);

		escribir.close();

		FileInputStream input = new FileInputStream(ruta);
		ObjectInputStream leer = new ObjectInputStream(input);

		try {
			Object animal = (Animal) leer.readObject();
			
			if(animal instanceof Animal) {
				System.out.print("es un animal");
			}
			
			while (animal != null) {
				Animal animalVerdadero = (Animal) animal;
				System.out.println(animalVerdadero.getNombre());
				animal = leer.readObject();
			}
		} catch (Exception e) {
			// TODO: handle exception
		}

		leer.close();
	}

}

````

````java
import java.io.Serializable;

public class Coche implements Serializable {
	
	private static final long serialVersionUID = 1L;
	
	private String marca;

	public Coche(String marca) {
		super();
		this.marca = marca;
	}

	public String getMarca() {
		return marca;
	}

	public void setMarca(String marca) {
		this.marca = marca;
	}
	
	
}

````
