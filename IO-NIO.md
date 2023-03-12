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

public class Animal implements Serializable{

	private static final long serialVersionUID = 2L;
	
	private String nombre;
	private boolean mamifero;
	
	public Animal(String nombre) {
		super();
		this.nombre = nombre;
	}

	public String getNombre() {
		return nombre;
	}

	public void setNombre(String nombre) {
		this.nombre = nombre;
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


````sql

CREATE TABLE Persons (
    PersonID int Primary key,
    LastName varchar(255),
    City varchar(255)
);

INSERT INTO Persons VALUES(1,"Alain","Vitoria");
INSERT INTO Persons VALUES(2,"Paco","Vitoria");
INSERT INTO Persons VALUES(3,"Sara","Vitoria");
INSERT INTO Persons VALUES(4,"Alfredo","Bilbao");
INSERT INTO Persons VALUES(5,"Mercedes","Bilbao");

````

