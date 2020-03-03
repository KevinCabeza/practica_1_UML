practica uml ejer 1
===


``` mermaid

    classDiagram
      Persona <|-- Empleado
      Persona <|-- Cliente
      Cliente "1..*" --o "0..*" Empresa
      Empleado <|-- Directivo
      Directivo "0..*" -- "0..*" Empleado : subordinados
      Empresa "1..*" *-- "1--*" Empleado : empleados

      class Empleado{
          -SueldoBruto : integer
          +Calcular_salario_neto()
          +mostrar() void
      }
      class Cliente{
          -nombre : String
          -edad : integer
          -telefono : String
          +mostrar()
      }
      class Empresa{
          -Nombre
          +Mostrar()
      }
       class Directivo{
          -nombre : String
          -edad : integer
          +mostrar() void
       }
       class Persona{
          -nombre : String
          -edad : integer
          +mostrar() void
      }
end