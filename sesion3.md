<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 
#### Actividad: Análisis de la Clase 'Jugadores' en Java"
>
>Analizar y comprender las diferentes partes de la clase "Jugadores" proporcionada. La clase representa a los jugadores de un equipo deportivo y contiene atributos y métodos para gestionar la información de los jugadores. El objetivo principal es identificar y comprender las distintas secciones de la clase, incluyendo sus atributos y métodos.
>
>Examinar detenidamente la clase "Jugadores" proporcionada en el enunciado.
Identificar y etiquetar cada una de las siguientes partes de la clase: <br>
a. Atributos (variables de instancia) <br>
b. Constructor <br>
c. Métodos de acceso (getters) para cada atributo <br>
d. Métodos de modificación (setters) para cada atributo <br>
e. Método "toString()" para representación en cadena <br>
>Crear una presentación de diapositivas que incluya:
Una diapositiva introductoria con el título de la actividad.
Diapositivas etiquetadas para cada parte de la clase identificada en el paso 2.
Diapositivas explicativas que detallen las funciones y utilidades de las partes de la clase.
>Presentar la presentación de diapositivas al grupo, compartiendo los hallazgos y conclusiones.

<p> public class Jugadores {
  
  private String nombre;
  private int edad;
  private String posicion;
  private int numero_camiseta;
  private String equipo;
  
  public Jugadores(String nombre, int edad, String posicion, int numero_camiseta, String equipo) {
    this.nombre = nombre;
    this.edad = edad;
    this.posicion = posicion;
    this.numero_camiseta = numero_camiseta;
    this.equipo = equipo;
  }
  
  public String getNombre() {
    return nombre;
  }

  public void setNombre(String nombre) {
    this.nombre = nombre;
  }

  public int getEdad() {
    return edad;
  }

  public void setEdad(int edad) {
    this.edad = edad;
  }

  public String getPosicion() {
    return posicion;
  }

  public void setPosicion(String posicion) {
    this.posicion = posicion;
  }

  public int getNumero_camiseta() {
    return numero_camiseta;
  }

  public void setNumero_camiseta(int numero_camiseta) {
    this.numero_camiseta = numero_camiseta;
  }

  public String getEquipo() {
    return equipo;
  }

  public void setEquipo(String equipo) {
    this.equipo = equipo;
  }

  public String toString() {
    return "Jugadores{" +
        "nombre='" + nombre + '\'' +
        ", edad=" + edad +
        ", posicion='" + posicion + '\'' +
        ", numero_camiseta=" + numero_camiseta +
        ", equipo='" + equipo + '\'' +
        '}';
  }

} </p>
>
>
>
<!-- Su documentación aquí -->

### https://drive.google.com/file/d/1Q3D36qaJFUgLeiTEmBAugyReiaoxIsxr/view?usp=sharing




