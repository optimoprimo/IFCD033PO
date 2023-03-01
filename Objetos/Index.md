- [Ménu](../README.md)

# Objetos

¿Cómo crear un objeto?

````java 
public class Automovil {

	private String nSerie;

	private boolean encendido;

	private int velocidad;

	public String getnSerie() {
		return nSerie;
	}

	public void setnSerie(String nSerie) {
		this.nSerie = nSerie;
	}

	public boolean isEncendido() {
		return encendido;
	}

	public void setEncendido(boolean encendido) {
		this.encendido = encendido;
	}

	public int getVelocidad() {
		return velocidad;
	}

	public void setVelocidad(int velocidad) {
		this.velocidad = velocidad;
	}
}
````

Para cerar un objeto de una clase utilizamos el operador new

La sintaxis es la siguiente;
````java
    // Tipo variables  --- Nomrbe variable --- = ---- new --- constructor
    Automovil               miCoche            =      new     Automovil();
````
Si una clase no tienen ningun  constructor, por defecto Java le añade el constructor vacio. Pero una clase puede tener uno o mas constructores definidos por nosotros.

````java 
public class Automovil {

	private String nSerie;

	private boolean encendido;

	private int velocidad;

	
	public Automovil() {
		super();
		// TODO Auto-generated constructor stub
	}
	
	public Automovil(String nSerie, boolean encendido, int velocidad) {
		super();
		this.nSerie = nSerie;
		this.encendido = encendido;
		this.velocidad = velocidad;
	}


	public String getnSerie() {
		return nSerie;
	}

	public void setnSerie(String nSerie) {
		this.nSerie = nSerie;
	}

	public boolean isEncendido() {
		return encendido;
	}

	public void setEncendido(boolean encendido) {
		this.encendido = encendido;
	}

	public int getVelocidad() {
		return velocidad;
	}

	public void setVelocidad(int velocidad) {
		this.velocidad = velocidad;
	}
}
````

¿Por que hemos creado los metodos setter y getter?
Para controlar como cambiamos los atributos de nuestros objetos.

# toString()

````java 
	@Override
	public String toString() {
		return "Automovil [nSerie=" + nSerie + ", encendido=" + encendido + ", velocidad=" + velocidad + "]";
	}
````

Podemos sobreescribir el metodo toString() para mostrar en pantalla los datos de nuestros objetos.

# equals(Object obj)

````java 
	@Override
	public boolean equals(Object obj) {
		if (this == obj)
			return true;
		if (obj == null)
			return false;
		if (getClass() != obj.getClass())
			return false;
		Automovil other = (Automovil) obj;
		return encendido == other.encendido && Objects.equals(nSerie, other.nSerie) && velocidad == other.velocidad;
	}
````

Podemos sobreescribir el metodo equals(Object obj) para poder comparar objetos creados por nosotros.