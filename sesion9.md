<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 



<!-- Su documentación aquí -->

## Actividad: Ejericio POO
>
## Conversor de Unidades
>
>El ejercicio consiste en crear una aplicación de convertidor de unidades en Java que implemente una superclase, subclases, herencias, constructores, métodos abstractos. La aplicación debe realizar conversiones de longitud, temperatura, divisas y peso.
>
>
1. Completar la implementación de la aplicación de convertidor de unidades en Java, siguiendo las instrucciones de la sesión 9.
>
>
## Superclase Conversor
```java
    public abstract class Conversor {
        protected String unidadOrigen;
        protected String unidadDestino;

        public Conversor(String unidadOrigen, String unidadDestino) {
            this.unidadOrigen = unidadOrigen;
            this.unidadDestino = unidadDestino;
        }
        
        public abstract double convertir(double cantidad);
    }
```
## Subclase Temperatura

```java
    public class Temperatura extends Conversor {

        public Temperatura(String unidadOrigen, String unidadDestino) {
            super(unidadOrigen, unidadDestino);
        }

        @Override
        public double convertir(double cantidad) {
            if (unidadOrigen.equals("Celsius") && unidadDestino.equals("Fahrenheit")) {
                // Celsius a Fahrenheit
                return (cantidad * 9 / 5) + 32;
            } else if (unidadOrigen.equals("Fahrenheit") && unidadDestino.equals("Celsius")) {
                // Fahrenheit a Celsius
                return (cantidad - 32) * 5 / 9;
            } else if (unidadOrigen.equals("Celsius") && unidadDestino.equals("Kelvin")) {
                // Celsius a Kelvin
                return cantidad + 273.15;
            } else if (unidadOrigen.equals("Kelvin") && unidadDestino.equals("Celsius")) {
                // Kelvin a Celsius
                return cantidad - 273.15;
            } else if (unidadOrigen.equals("Fahrenheit") && unidadDestino.equals("Kelvin")) {
                // Fahrenheit a Kelvin
                double celsius = (cantidad - 32) * 5 / 9;
                return celsius + 273.15;
            } else if (unidadOrigen.equals("Kelvin") && unidadDestino.equals("Fahrenheit")) {
                // Kelvin a Fahrenheit
                double celsius = cantidad - 273.15;
                return (celsius * 9 / 5) + 32;
            } else {
                throw new IllegalArgumentException("Unidades de temperatura no compatibles");
            }
        }
    }
```
 ## Subclase Longitud

  
>
>complementar código:
- Metros a Pies.
- Pies a Metros.
- Kilómetros a Millas.
- Millas a Kilómetros.
- Centímetros a Pulgadas.
- Pulgadas a Centímetros.
- Yardas a Metros.
- Metros a Yardas.
- Millas Náuticas a Kilómetros.
- Kilómetros a Millas Náuticas.
- Micrómetros a Milímetros.
- Milímetros a Micrómetros.
- Decímetros a Metros.
- Metros a Decímetros.
>
>
```java
    public class Longitud extends Conversor {

            public Longitud(String unidadOrigen, String unidadDestino) {
                super(unidadOrigen, unidadDestino);
            }

            @Override
            public double convertir(double cantidad) {
                // Código 
                return 0;
            }
            if(unidadOrigen.equals("Metros") && unidadDestino.equals("Pies")){
                        double resultado = cantidad * 3.28084;
                        return resultado;
                    } else if (unidadOrigen.equals("Pies") && unidadDestino.equals("Metros")) {
                        double resultado = cantidad * 0.3048;
                        return resultado;
                    } else if (unidadOrigen.equals("Kilometros") && unidadDestino.equals("Millas")) {
                        double resultado = cantidad * 0.621371;
                        return resultado;
                    } else if (unidadOrigen.equals("Millas") && unidadDestino.equals("Kilometros")) {
                        double resultado = cantidad * 1.60934;
                        return resultado;
                    } else if (unidadOrigen.equals("Centimetros") && unidadDestino.equals("Pulgadas")) {
                        double resultado = cantidad * 0.393701;
                        return resultado;
                    } else if (unidadOrigen.equals("Pulgadas") && unidadDestino.equals("Centimetros")) {
                        double resultado = cantidad * 2.54;
                        return resultado;
                    } else if (unidadOrigen.equals("Yardas") && unidadDestino.equals("Metros")) {
                        double resultado = cantidad * 0.9144;
                        return resultado;
                    } else if (unidadOrigen.equals("Metros") && unidadDestino.equals("Yardas")) {
                        double resultado = cantidad * 1.09361;
                        return resultado;
                    } else if (unidadOrigen.equals("Millas Nauticas") && unidadDestino.equals("Kilómetros")) {
                        double resultado = cantidad * 1.852;
                        return resultado;
                    } else if (unidadOrigen.equals("Kilómetros") && unidadDestino.equals("Millas Nauticas")) {
                        double resultado = cantidad * 0.539957;
                        return resultado;
                    } else if (unidadOrigen.equals("Micrometros") && unidadDestino.equals("Milimetros")) {
                        double resultado = cantidad * 0.001;
                        return resultado;
                    } else if (unidadOrigen.equals("Milimetros") && unidadDestino.equals("Micrometros")) {
                        double resultado = cantidad * 1000;
                        return resultado;
                    } else if (unidadOrigen.equals("Decimetros") && unidadDestino.equals("Metros")) {
                        double resultado = cantidad * 0.1;
                        return resultado;
                    } else if (unidadOrigen.equals("Metros") && unidadDestino.equals("Decimetros")) {
                        double resultado = cantidad * 10;
                        return resultado;
                    }else {
                        throw new IllegalArgumentException("Longitudes no compatibles");
                    }

    }       
```              
>
## Subclase Peso

>Implementar código:<br>
- Kilogramos a Libras.
- Libras a Kilogramos.
- Gramos a Libras.
- Libras a Gramos.
- Kilogramos a Gramos.
- Gramos a Kilogramos.
- Toneladas a Kilogramos.
- Kilogramos a Toneladas.
- Libras a Onzas.
- Onzas a Libras.
- Gramos a Onzas.
- Onzas a Gramos.
- Toneladas a Libras.
- Libras a Toneladas.
- Toneladas a Gramos.
- Gramos a Toneladas.
- Toneladas a Miligramos.
- Miligramos a Toneladas.
- Kilogramos a Miligramos.
- Miligramos a Kilogramos.
>
```java
    public class Peso extends Conversor {

        public Peso(String unidadOrigen, String unidadDestino) {
            super(unidadOrigen, unidadDestino);
        }

        @Override
        public double convertir(double cantidad) {
            // Código 
            return 0;
        }
        if(unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 2.20462;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.453592;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 0.00220462;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 453.592;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 1000;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.001;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 1000;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.001;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Onzas")){
            double resultado = cantidad * 16;
            return resultado;
        }else if (unidadOrigen.equals("Onzas") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 0.0625;
            return resultado;
        }else if (unidadOrigen.equals("Gramos ") && unidadDestino.equals("Onzas")){
            double resultado = cantidad * 0.035274;
            return resultado;
        }else if (unidadOrigen.equals("Onzas") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 28.3495;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 2204.62;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000453592;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 1000000;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000001;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Miligramos")){
            double resultado = cantidad * 1000000000;
            return resultado;
        }else if (unidadOrigen.equals("Miligramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000000001;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Miligramos")){
            double resultado = cantidad * 1000000;
            return resultado;
        }else if (unidadOrigen.equals("Miligramos") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.000001;
            return resultado;
        }else{
            throw new IllegalArgumentException("Pesos no compatibles");
        }
    }
```
>
>
##  Subclase Divisas
>
>Implementar código:
- Dólar estadounidense a Euro.
- Euro a Dólar estadounidense.
- Dólar estadounidense a Peso colombiano.
- Peso colombiano a Dólar estadounidense.
- Euro a Peso colombiano.
- Peso colombiano a Euro.
```java
        public class Divisas extends Conversor{

            public Divisas(String unidadOrigen, String unidadDestino) {
                super(unidadOrigen, unidadDestino);
            }

            @Override
            public double convertir(double cantidad) {
                // Código
                return 0;
            }
            if (unidadOrigen.equals("Dolar") && unidadDestino.equals("Euro")){
                    double resultado = cantidad * 0.98;
                    return resultado;
                } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Dolar")) {
                    double resultado = cantidad * 1.06;
                    return resultado;
                } else if (unidadOrigen.equals("Dólar") && unidadDestino.equals("Peso colombiano")) {
                    double resultado = cantidad * 4073.34;
                    return resultado;
                } else if (unidadOrigen.equals("Peso colombiano") && unidadDestino.equals("Dólar")) {
                    double resultado = cantidad * 0.00025;
                    return resultado;
                } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Peso colombiano")) {
                    double resultado = cantidad * 4312.24;
                    return resultado;
                } else if (unidadOrigen.equals("Peso colombiano") && unidadDestino.equals("Euro")) {
                    double resultado = cantidad * 0.00023;
                    return resultado;
                }else {
                    throw new IllegalArgumentException("Divisas no compatibles");
                }
        }
```
>
2. Agregar la subclase programador que contenga siguientes conversiones:
>
- Decimal a Binario
- Decimal a Hexadecimal
- Binario a Decimal
- Hexadecimal a Binario

## subclase Programador

```java	
class Programador extends Conversor {

    public Programador(String unidadOrigen, String unidadDestino) {
        super(unidadOrigen, unidadDestino);
    }

    @Override
    public double convertir(double cantidad) {
               if (unidadOrigen.equals("Decimal") && unidadDestino.equals("Binario")) {
            return decimalABinario(cantidad);
        } else if (unidadOrigen.equals("Decimal") && unidadDestino.equals("Hexadecimal")) {
            return decimalAHexadecimal(cantidad);
        } else if (unidadOrigen.equals("Binario") && unidadDestino.equals("Decimal")) {
            return binarioADecimal(cantidad);
        } else if (unidadOrigen.equals("Hexadecimal") && unidadDestino.equals("Binario")) {
            return hexadecimalABinario(cantidad);
        } else {
            System.out.println("Conversión no válida");
            return 0.0;
        }
    }

    private double decimalABinario(double decimal) {
        // decimal a binario 
        return Double.parseDouble(Integer.toBinaryString((int) decimal));
    }

    private double decimalAHexadecimal(double decimal) {
        // decimal a hexadecimal
        return Double.parseDouble(Integer.toHexString((int) decimal));
    }

    private double binarioADecimal(double binario) {
        // binario a decimal 
         return Double.parseDouble(Integer.toString((int) binario, 2));
    }

    private double hexadecimalABinario(double hexadecimal) {
        // hexadecimal a binario
        int decimal = Integer.parseInt(Double.toString(hexadecimal), 16);
        return Double.parseDouble(Integer.toBinaryString(decimal));
    }
   
}
```	
## ejemplo
```java
public class Actividad9 {

    public static void main(String[] args) {
     
      Temperatura T1 = new Temperatura ("Celsius","Fahrenheit");
      double resultado = T1.convertir(25);
        System.out.println("la conversion de celsius a fahrenheit es: " +resultado);
        
      Temperatura T2 = new Temperatura ("Fahrenheit","Kelvin");
      double res = T2.convertir(14);
      System.out.println("la conversion de Fahrenheit a Kelvin es: " + res);  
        
      Longitud L1 = new Longitud ("Metros", "Pies");
      double resultado1 = L1.convertir(36);
      System.out.println("La conversion de metros a pies es: " +resultado1);
      
      Longitud L2 = new Longitud("Centimetros", "Pulgadas");
      resultado = L2.convertir(40);
      System.out.println("la conversion de centrimetros a pultadas es: " + resultado);
      
      Peso P1 = new Peso("Toneladas", "Kilogramos");
      resultado = P1.convertir(25);
      System.out.println("La conversion de toneladas a kilogramos es: " + resultado);
      
      Peso P2 = new Peso("Kilogramos","Toneladas");
      resultado = P2.convertir(14);
      System.out.println("La conversion de kilogramos a toneladas es: " + resultado);
              
      Programador p1 = new Programador("Decimal", "Binario");
      double resultado2 = p1.convertir(15);
      System.out.println("La conversion de decimal a binario es: " + resultado2);
      
      Programador p2 = new Programador("Decimal", "Hexadecimal");
      double resultado3 = p2.convertir(20);
      System.out.println("la conversion decimal a hexadecimal es: " + resultado3);
      
      Programador p3 = new Programador("Binario", "Decimal");
      double resultado4 = p3.convertir(1010);
      System.out.println("El resultado de binario a decimal es: " + resultado4);
      
      Programador p4 = new Programador("Hexadecimal", "Binario");
      double resultado5 = p4.convertir(0);
      System.out.println("la conversion hexadecimal a binario es: " + resultado5);
    }
}
```	


