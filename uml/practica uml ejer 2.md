practica uml ejer 2
===
``` mermaid


    classDiagram

    Multa "sancion, 0.1" -- "sancionado-->recibe" Socio
    Prestamo .. Copia
    Prestamo .. Socio
    Copia "3.." -- "0.1" Socio
    Copia "1..*" -- "libro" Libro
    Autor "autor" -- "obra, 1..*" Libro

    
        class Libro{
            -titulo: String
            -editorial: String
            -year: Integer
            -tipo: Genero
        }

        class Genero{
            <<enumeration>>
            novela
            teatro
            poesia
            ensayo
        }

         class Multa {
            -inicio: date
            -fin: date
        }

        class Copia{
            -referencia: Integer
            -estado: Estado_copia
        }

        class Autor{
            -nombre: String
            -nacionalidad: String
            -F_nacimiento: date
        }

        class Prestamo{
            -inicio : date
            -fin : date
        }

        class EstadoCopia{
            <<enumeration>>
            prestado
            retraso
            biblioteca
            reparacion
        }

        class Socio{
            -numero: Integer
            -nombre: String
            -direccion: String
            -telefono: Integer
        }
        
end