<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 




Actividad: Implementación de las Clases Automóvil y Motocicleta utilizando la herencia en java
Implementar las clases derivadas (Automovil y Motocicleta) que hereden de la clase base (Vehiculo) en Java.

// Clase base: Vehiculo
class Vehiculo {
    protected String marca; // Cambiamos a protegido
    protected String modelo; // Cambiamos a protegido
    private int año;

    public Vehiculo(String marca, String modelo, int año) {
        this.marca = marca;
        this.modelo = modelo;
        this.año = año;
    }

    public void mostrarInformacion() {
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Año: " + año);
    }
}

###### Implementación de la clase Automovil.
>Crear la clase Automovil como una clase derivada de Vehiculo y agregar los    siguientes atributos privados:  
>
>numPuertas (int): Número de puertas del automóvil.
tipoTransmision (String): Tipo de transmisión del automóvil (manual o automática).
>Implementar un constructor en la clase Automovil que acepte todos los atributos de Vehiculo (marca, modelo, año), así como los nuevos atributos (numPuertas y tipoTransmision). El constructor debe llamar al constructor de la clase base (Vehiculo) utilizando super().  
>
>Implementar el método mostrarInformacionAutomovil() en la clase Automovil. El nuevo método debe mostrar toda la información del automóvil, incluyendo el número de puertas y el tipo de transmisión.   
>
>Crear un objeto de la clase Automovil en el programa principal (main) y utilizarlo para probar la funcionalidad de la clase Automovil. Debe mostrar la información del automóvil utilizando el método mostrarInformacionAutomovil().   
>
>Agregar métodos adicionales a la clase Automovil según su creatividad y utilizarlos en el programa principal (main).   
>
>Implementación de la clase Motocicleta.   
Crear la clase Motocicleta como una clase derivada de Vehiculo y agregar los siguientes atributos privados:  
>
>tipo (String): El tipo de motocicleta (deportiva, crucero, etc.).
cilindraje (int): El cilindraje de la motocicleta en centímetros cúbicos (cc).
Implementar un constructor en la clase Motocicleta que acepte todos los atributos de Vehiculo (marca, modelo, año), así como los nuevos atributos (tipo y cilindraje). El constructor debe llamar al constructor de la clase base (Vehiculo) utilizando super().    
>
>Implementar el método mostrarInformacionMotocicleta() en la clase Motocicleta. El nuevo método debe mostrar toda la información de la motocicleta, incluyendo el tipo y el cilindraje.  
>
>Crear un objeto de la clase Motocicleta en el programa principal (main) y utilizarlo para probar la funcionalidad de la clase Motocicleta. Debe mostrar la información de la motocicleta utilizando el método mostrarInformacionMotocicleta().   
>
>Agregar métodos adicionales a la clase Motocicleta según su creatividad y utilizarlos en el programa principal (main).   
>
>
<!-- Su documentación aquí -->
 <p>class Vehiculo {
    protected String marca;
    protected String modelo;
    private int año;

    public Vehiculo(String marca, String modelo, int año) {
        this.marca = marca;
        this.modelo = modelo;
        this.año = año;
    }

    public void mostrarInformacion() {
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Año: " + año);
    }
}

class Automovil extends Vehiculo {
    private int numPuertas;
    private String tipoTransmision;

    public Automovil(String marca, String modelo, int año, int numPuertas, String tipoTransmision) {
        super(marca, modelo, año);
        this.numPuertas = numPuertas;
        this.tipoTransmision = tipoTransmision;
    }

    public void mostrarInformacionAutomovil() {
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Año: " + año);
        System.out.println("Número de Puertas: " + numPuertas);
        System.out.println("Tipo de Transmisión: " + tipoTransmision);
    }
}

class Motocicleta extends Vehiculo {
    private String tipo;
    private int cilindraje;

    public Motocicleta(String marca, String modelo, int año, String tipo, int cilindraje) {
        super(marca, modelo, año);
        this.tipo = tipo;
        this.cilindraje = cilindraje;
    }

    public void mostrarInformacionMotocicleta() {
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Año: " + año);
        System.out.println("Tipo: " + tipo);
        System.out.println("Cilindraje: " + cilindraje + " cc");
    }

}

public class Main {
    public static void main(String[] args) {
        Automovil automovil = new Automovil("Toyota", "Camry", 2022, 4, "Automática");
        
        automovil.mostrarInformacionAutomovil();
        
        Motocicleta motocicleta = new Motocicleta("Honda", "CBR500R", 2021, "Deportiva", 500);
        
        motocicleta.mostrarInformacionMotocicleta();
    }
} </p>






