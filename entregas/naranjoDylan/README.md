@startuml
skinparam rectangle {
    BackgroundColor<<class>> White
    BorderColor<<class>> Red
    FontColor<<class>> Red
}

skinparam arrow {
    Color Red
    Thickness 1
}

skinparam class {
    BackgroundColor White
    BorderColor Red
    FontColor Red
}

' --- CLASES ---
class View
class Schema
class Tabla
class Relacion
class ForeignKey
class PrimaryKey
class Usuario
class Role
class Permiso
class Trigger
class Indice
class Campo
class Atributos
class Contrains

' --- RELACIONES ---

' Agregación: Schema contiene Tabla y View
Schema "1" *-- "n" Tabla
Schema "1" *-- "n" View

' Composición: Tabla tiene campos, índices, triggers
Tabla "1" o-- "n" Campo
Tabla "1" o-- "n" Indice
Tabla "1" o-- "n" Trigger

' Campo contiene Atributos y Contrains
Campo "1" o-- "n" Atributos
Campo "1" o-- "n" Contrains

' Relación entre Tabla y Relacion (agregación)
Tabla "1" o-- "n" Relacion

' Relacion tiene Foreign Key y Primary Key
Relacion "1" o-- "n" ForeignKey
Relacion "1" o-- "n" PrimaryKey

' Usuario, Role, Permiso (herencia/relación jerárquica)
Usuario <|-- Role
Role <|-- Permiso

' View compone a Schema y Tabla (según el dibujo, con diamante relleno)
View "1" *-- "n" Schema
View "1" *-- "n" Tabla

' --- ESTILO ESPECIAL PARA LAS FLECHAS DE COMPOSICIÓN ---
note right of View
  Según el diagrama original,
  View está compuesta por Schema y Tabla.
end note

@enduml