<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->

#### Actividad: Clases y métodos abstractos de la superclase "Musica" en Java

>
>
>
>Se desea crear una jerarquía de clases que permita representar diferentes tipos de música. Se ha decidido crear una superclase Musica que tenga los métodos y atributos comunes a todas las clases hijas.
>
>La superclase Musica debe tener los siguientes métodos abstractos:
>
- play(): reproduce la música.
- stop(): detiene la reproducción de la música.
- pause(): pausa la reproducción de la música.
- next(): avanza a la siguiente canción.
- previous(): retrocede a la canción anterior.
>
>Además, la superclase Musica debe tener un atributo titulo que indique el título de la canción.
>
>Crear las clases hijas necesarias para representar diferentes tipos de música, como por ejemplo:
>
1. _Cancion:_ representa una canción en general.<br> 
- Atributos Privados: Declarar dos atributos privados, artista (nombre del artista de la canción) y album (nombre del álbum de la canción).
>
- Constructor: Implementar un constructor que acepte tres parámetros: titulo, artista y album, y que inicialice adecuadamente los atributos de la clase "Cancion". Utiliza la palabra clave super para llamar al constructor de la clase base "Musica" pasando el titulo como argumento.
>
- Métodos Anulados (Override): Implementar los métodos anulados (override) de la clase base "Musica" para las acciones de reproducción (play), detención (stop), pausa (pause), avanzar (next) y retroceder (previous) en la reproducción de la canción. Cada uno de estos métodos debe imprimir un mensaje informativo adecuado en la consola.

2. _BandaSonora:_ representa una banda sonora de una película o serie de televisión.
>
- Atributos Privados: Declarar un atributo privado, pelicula (nombre de la película a la que pertenece la banda sonora).
>
- Constructor: Implementar un constructor que acepte dos parámetros: titulo y pelicula, y que inicialice adecuadamente los atributos de la clase "BandaSonora". Utiliza la palabra clave super para llamar al constructor de la clase base "Musica" pasando el titulo como argumento.
>
- Métodos Anulados (Override): Implementar los métodos anulados (override) de la clase base "Musica" para las acciones de reproducción (play), detención (stop), pausa (pause), avanzar (next) y retroceder (previous) en la reproducción de la banda sonora. Cada uno de estos métodos debe imprimir un mensaje informativo adecuado en la consola.
>
3.  _Album:_ representa un álbum de música.
>
- Atributos Privados: Declarar un atributo privado, canciones (una lista de objetos de tipo "Cancion" que representan las canciones del álbum).
>
- Constructor: Implementar un constructor que acepte dos parámetros: titulo (título del álbum) y canciones (una lista de canciones del álbum), y que inicialice adecuadamente los atributos de la clase "Album". Utiliza la palabra clave super para llamar al constructor de la clase base "Musica" pasando el titulo como argumento.
<>
- Métodos Anulados (Override): Implementar los métodos anulados (override) de la clase base "Musica" para las acciones de reproducción (play), detención (stop), pausa (pause), avanzar (next) y retroceder (previous) en la reproducción del álbum. Cada uno de estos métodos debe imprimir un mensaje informativo adecuado en la consola y luego ejecutar las acciones correspondientes en cada canción del álbum.
>
>Cada clase hija debe implementar los métodos abstractos de la superclase Musica de manera adecuada para su tipo de música.


## solución

#### super clase Musica

~~~

        public abstract class Musica {
            
            public String tituloCancion;

            public Musica(String tituloCancion) {
                this.tituloCancion = tituloCancion;
            }

            public void setTituloCancion(String tituloCancion) {
                this.tituloCancion = tituloCancion;
            }
            public abstract void   play(); 
            public abstract void   stop(); 
            public abstract void   pause(); 
            public abstract void   next (); 
            public abstract void   previous(); 
            
        }
~~~

 #### clase hija Cancion

~~~
        public class Cancion extends Musica {
            
            private String artista;
            private String Album;

            public Cancion(String artista, String Album, String tituloCancion) {
                super(tituloCancion);
                this.artista = artista;
                this.Album = Album;
                
                
            }

            @Override
            public void setTituloCancion(String tituloCancion) {
                super.setTituloCancion(tituloCancion); 
            }

            @Override
            public void play() {
                System.out.println("Reproduccir");
                
            }

            @Override
            public void stop() {
                System.out.println("Parar");
            }

            @Override
            public void pause() {
            System.out.println("Pausar"); 
            }

            @Override
            public void next() {
                System.out.println("Siguiente");
            } 
        
            @Override
            public void previous() {
                System.out.println("Anterior");
            }   
        
        
            }
 ~~~

 #### BandaSonora

 ~~~
        public class BandaSonora extends Musica {
            
            private String pelicula;

            public BandaSonora(String pelicula, String tituloCancion) {
                super(tituloCancion);
                this.pelicula = pelicula;
            }

            @Override
            public void play() {
                
                System.out.println("Reproduccir Pelicula");
                
            }

            @Override
            public void stop() {
                System.out.println("Para pelicula");
                    
            }

            @Override
            public void pause() {
                System.out.println("Pausar pelicula");        
                
            }

            @Override
            public void next() {
                System.out.println("Adelantar pelicula");
                
                
            }

            @Override
            public void previous() {
                System.out.println("Retroceder pelicula");
                
            
            }

            
        }
~~~

#### Album
~~~
        public class Album extends Musica{
            
            private String canciones;

            public Album(String canciones, String tituloCancion) {
                super(tituloCancion);
                this.canciones = canciones;
            }

            @Override
            public void play() {
                System.out.println("Reproduccir Album");
                
            
            }

            @Override
            public void stop() {
                System.out.println("Para album");
                
            }

            @Override
            public void pause() {
                System.out.println("Pausar album");
                
            }

            @Override
            public void next() {
            System.out.println("siguiente album");
                
            }

            @Override
            public void previous() {
                System.out.println("Anterior album");
                
                
            }
            
        }
~~~

#### lista del album

~~~
    public class Album extends Musica {
        private List<Cancion> canciones;

        public Album(String titulo, List<Cancion> canciones) {
            super(titulo);
            this.canciones = canciones;
        }

        @Override
        public void play() {
            System.out.println("Reproduciendo el álbum: " + getTitulo());
            for (Cancion cancion : canciones) {
                cancion.play();
            }
        }

        @Override
        public void stop() {
            System.out.println("Deteniendo el álbum: " + getTitulo());
            for (Cancion cancion : canciones) {
                cancion.stop();
            }
        }

        @Override
        public void pause() {
            System.out.println("Pausando el álbum: " + getTitulo());
            for (Cancion cancion : canciones) {
                cancion.pause();
            }
        }

        @Override
        public void next() {
            System.out.println("Avanzando al siguiente en el álbum: " + getTitulo());
        }

        @Override
        public void previous() {
            System.out.println("Retrocediendo al anterior en el álbum: " + getTitulo());
        }
    }
~~~






