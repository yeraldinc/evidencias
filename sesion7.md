<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->

#### Actividad: Clase Producto con Métodos Sobrecargados


> Crea una clase llamada Producto que representará productos en una tienda en línea. La clase debe tener los siguientes atributos privados:
>
- nombre (String): El nombre del producto.
- precio (double): El precio del producto.
- cantidad (int): La cantidad de unidades disponibles del producto.<br>
>
>La clase Producto debe tener los siguientes constructores sobrecargados:
>
- Un constructor por defecto que inicialice el nombre como "Desconocido", el precio como 0.0 y la cantidad como 0.
- Un constructor que tome como argumentos el nombre y el precio del producto, y establezca la cantidad en 0.
- Un constructor que tome como argumentos el nombre, el precio y la cantidad del producto.
>
>La clase Producto debe tener los siguientes métodos:
>
- calcularValorTotal(): Un método que calcule y devuelva el valor total del producto en base a su precio y cantidad.
- mostrarInformacion(): Un método que muestre por consola la información del producto, incluyendo el nombre, precio, cantidad y valor total.
>
>Además, debes agregar los siguientes métodos sobrecargados:
>
- incrementarCantidad(): Un método sobrecargado que incremente la cantidad en 1 unidad.
>
- incrementarCantidad(int cantidadIncrementar): Un método sobrecargado que permita incrementar la cantidad en una cantidad específica proporcionada como argumento.
>
- actualizarPrecio(double nuevoPrecio): Un método sobrecargado que permita actualizar el precio del producto en dólares con un nuevo valor proporcionado como argumento.
>
>actualizarPrecio(double nuevoPrecio, String moneda): Un método sobrecargado que permita actualizar el precio del producto en dólares con un nuevo valor proporcionado como argumento, teniendo en cuenta la moneda especificada y utilizando las tasas de conversión adecuadas. Debes asumir tasas de conversión fijas para las monedas admitidas.
>
>actualizarPrecio(double nuevoPrecio, String moneda, double tasaCambio): Un método sobrecargado que permita actualizar el precio del producto en dólares con un nuevo valor proporcionado como argumento, teniendo en cuenta la moneda especificada y la tasa de cambio proporcionada.
>
>
>En el método main, crea tres instancias de la clase Producto utilizando los diferentes constructores, muestra la información de los productos y realiza algunas operaciones para probar los métodos sobrecargados, incluyendo la actualización de precios en euros y pesos colombianos con tasas de conversión específicas.

~~~
CLASE 7

                public class Producto {
                    
                public String nombre;
                public double precio;
                public int cantidad;

                //Constructores
                    public Producto() {
                        this.nombre = "Desconocido";
                        this.precio = 0.0;
                        this.cantidad = 0;
                    }
                    public Producto(String nombre, double precio) {
                        this.nombre = nombre;
                        this.precio = precio;
                        this.cantidad = 0;
                    
                }

                    public Producto(String nombre, double precio, int cantidad) {
                        this.nombre = nombre;
                        this.precio = precio;
                        this.cantidad = cantidad;
                        
                    }
                    //metodos
                    
                    public double calcularValorTotal(){
                        return precio * cantidad;
                    }
                    
                    public void mostrarInformacion() {
                        System.out.println("Informacion del produto");
                        System.out.println("nombre: " + nombre);
                        System.out.println("precio: " + precio);
                        System.out.println("cantidad: " + cantidad);
                        System.out.println("Valor total: " + calcularValorTotal());
                        
                    }
                    // Metodo Sobrecargados
                    
                    public void incrementarCantidad(){
                    cantidad++;}
                

                    public void incrementarCantidad(int cantidadIncrementar){
                    cantidad += cantidadIncrementar;
                    }
                    //Precio dolar
                    public void actualizarPrecio(double nuevoPrecio) {
                        precio = nuevoPrecio;
                    }
                    
                    //Precio Euro
                    public void actualizarPrecio(double nuevoPrecio, String moneda){
                        double tasaCambio = 1.0;
                        if (moneda.equals("Euros")){
                            tasaCambio = 0.85;
                        } else if (moneda.equals("Peso colombiano: ")){
                            
                        }
                        
                        precio = nuevoPrecio * tasaCambio;
                        
                    }
                    
                    //Precio moneja espefica
                    
                    public void actualizarPrecio (double nuevoprecio, String modena, double tasaCambio){
                        if (modena.equals("Dolares")){
                            precio = nuevoprecio;
                        } else {
                            precio = nuevoprecio * tasaCambio;
                        }
                    }
                }

                MAIN


                public class Actividad7 {

                    public static void main(String[] args) {
                        Producto p1 = new Producto ();
                        Producto p2 = new Producto ("Producto 2", 15.0);
                        Producto p3 = new Producto ("Producto 3", 20, 5);
                        
                        p1.mostrarInformacion();
                        p2.mostrarInformacion();
                        p3.mostrarInformacion();
                        
                        
                        p1.incrementarCantidad();
                        p2.incrementarCantidad(1);
                        p3.actualizarPrecio(2.5);
                        p3.incrementarCantidad();
                        p2.actualizarPrecio(30, "euros");
                        p2.actualizarPrecio(15, "peso Colombiano", 4000);
                        
                        
                        p1.mostrarInformacion();
                        p2.mostrarInformacion();
                        p3.mostrarInformacion();
                        
                        
                        
                    }
    
   ~~~



