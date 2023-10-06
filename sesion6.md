<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 6


<!-- Su documentación aquí -->

#### Actividad: Clase Producto con Métodos Sobrecargados


>Crea una clase llamada Producto que representará productos en una tienda en línea. La clase debe tener los siguientes atributos privados:

-nombre (String): El nombre del producto.
-precio (double): El precio del producto.
-cantidad (int): La cantidad de unidades disponibles del producto.
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

- incrementarCantidad(): Un método sobrecargado que incremente la cantidad en 1 unidad.

- incrementarCantidad(int cantidadIncrementar): Un método sobrecargado que permita incrementar la cantidad en una cantidad específica proporcionada como argumento.

- actualizarPrecio(double nuevoPrecio): Un método sobrecargado que permita actualizar el precio del producto en dólares con un nuevo valor proporcionado como argumento.

- actualizarPrecio(double nuevoPrecio, String moneda): Un método sobrecargado que permita actualizar el precio del producto en dólares con un nuevo valor proporcionado como argumento, teniendo en cuenta la moneda especificada y utilizando las tasas de conversión adecuadas. Debes asumir tasas de conversión fijas para las monedas admitidas.

- actualizarPrecio(double nuevoPrecio, String moneda, double tasaCambio): Un método sobrecargado que permita actualizar el precio del producto en dólares con un nuevo valor proporcionado como argumento, teniendo en cuenta la moneda especificada y la tasa de cambio proporcionada.
>
>En el método main, crea tres instancias de la clase Producto utilizando los diferentes constructores, muestra la información de los productos y realiza algunas operaciones para probar los métodos sobrecargados, incluyendo la actualización de precios en euros y pesos colombianos con tasas de conversión específicas.



~~~ 
        public class Producto {
            private String nombre;
            private double precio;
            private int cantidad;

            // Constructor por defecto
            public Producto() {
                this.nombre = "Desconocido";
                this.precio = 0.0;
                this.cantidad = 0;
            }

            // Constructor con nombre y precio
            public Producto(String nombre, double precio) {
                this.nombre = nombre;
                this.precio = precio;
                this.cantidad = 0;
            }

            // Constructor con nombre, precio y cantidad
            public Producto(String nombre, double precio, int cantidad) {
                this.nombre = nombre;
                this.precio = precio;
                this.cantidad = cantidad;
            }

            // Método para calcular el valor total
            public double calcularValorTotal() {
                return precio * cantidad;
            }

            // Método para mostrar información del producto
            public void mostrarInformacion() {
                System.out.println("Nombre: " + nombre);
                System.out.println("Precio: $" + precio);
                System.out.println("Cantidad: " + cantidad);
                System.out.println("Valor Total: $" + calcularValorTotal());
            }

            // Método sobrecargado para incrementar la cantidad en 1 unidad
            public void incrementarCantidad() {
                cantidad++;
            }

            // Método sobrecargado para incrementar la cantidad en una cantidad específica
            public void incrementarCantidad(int cantidadIncrementar) {
                cantidad += cantidadIncrementar;
            }

            // Método sobrecargado para actualizar el precio en dólares
            public void actualizarPrecio(double nuevoPrecio) {
                precio = nuevoPrecio;
            }

            // Método sobrecargado para actualizar el precio en una moneda específica con tasa de conversión fija
            public void actualizarPrecio(double nuevoPrecio, String moneda) {
                double tasaCambio = 1.0; // Tasa de conversión fija (ejemplo: 1 USD = 1 EUR)
                if (moneda.equals("EUR")) {
                    precio = nuevoPrecio * tasaCambio;
                } else if (moneda.equals("COP")) {
                    // Tasa de conversión fija para pesos colombianos
                    precio = nuevoPrecio * 3500; // Ejemplo: 1 USD = 3500 COP
                }
            }

            // Método sobrecargado para actualizar el precio en una moneda específica con una tasa de cambio proporcionada
            public void actualizarPrecio(double nuevoPrecio, String moneda, double tasaCambio) {
                if (moneda.equals("EUR") || moneda.equals("COP")) {
                    precio = nuevoPrecio * tasaCambio;
                }
            }

            public static void main(String[] args) {
                // Crear instancias de Producto usando diferentes constructores
                Producto producto1 = new Producto();
                Producto producto2 = new Producto("Camiseta", 25.0);
                Producto producto3 = new Producto("Zapatos", 80.0, 2);

                // Mostrar información de los productos
                producto1.mostrarInformacion();
                producto2.mostrarInformacion();
                producto3.mostrarInformacion();

                // Realizar operaciones con los métodos sobrecargados
                producto1.incrementarCantidad(); // Incrementar cantidad en 1 unidad
                producto2.incrementarCantidad(3); // Incrementar cantidad en 3 unidades
                producto3.actualizarPrecio(90.0); // Actualizar precio en dólares
                producto2.actualizarPrecio(20.0, "EUR"); // Actualizar precio en euros
                producto3.actualizarPrecio(50000.0, "COP"); // Actualizar precio en pesos colombianos

                // Mostrar información actualizada
                producto1.mostrarInformacion();
                producto2.mostrarInformacion();
                producto3.mostrarInformacion();
            }
        }
~~~ 