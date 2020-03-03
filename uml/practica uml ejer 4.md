practica uml ejer 4
===


``` mermaid

 classDiagram
      Proyecto *-- "1..*" Ciclo : (ordered)
      Ciclo *-- "4..*" Fase : (ordered)
      Iteracion "1..*" --* Fase : (ordered)
      Actividad "1..*" --* Iteracion
      Ejecutable -- Ciclo
      Iteracion -- "1..*" Artefacto : produce
      Documento --|> Artefacto
      Software --|> Artefacto
      Recurso "0..*" --* "0..*" Actividad
      Humano --|> Recurso
      Material --|> Recurso

        class Proyecto {
          -nombre : String
          -avance : Float
    }

      class Ciclo{
      }

      class Fase{
          -tipo : TipoFase
      }

      class Ejecutable{
          -bytes
      }

      class Iteracion{
          -comienzo : Date
      }

      class Artefacto{
      }

      class Documento{
          -nombre : String
          -ubicacion : String
      }

      class Software{
          -bytes
      }

      class Actividad{
          -duracion : Integer
          -avance : Float
      }

      class Recurso{
      }

      class Humano{
          -nombre : String
      }

      class Material{
          -inventario : String
      }

      class TipoFase{
          inicio
          elaboracion
          construccion
          transicion
     }







