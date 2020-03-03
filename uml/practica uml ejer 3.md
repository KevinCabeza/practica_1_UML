practica uml ejer 3
===


``` mermaid
    classDiagram
    Vuelo "0..*" -- "0..*" Persona
    Avion "1..*" -- "0..*" Vuelo
    Billete .. Vuelo
    Billete .. Persona
    


        class Vuelo{
            -plazas : Integer
            -fecha : Date
            }
        class Billete{
            -asiento : Integer
            }
        class Persona{ 
            -nombre : String
            -fechaNacimiento : Date
            -apellidos : String
            -sexo : Genero
            }
        class Avion{
            -modelo : String
            -capacidad : Integer
            }
        class Genero{
            <<enumeration>>
            -hombre
            -mujer
            }
end