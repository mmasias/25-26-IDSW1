# Diagramas de entidades y de objetos de un sistema de gestión de bases de datos relacional

[Ir a diagramas de objetos](#Diagramas-de-objetos)

## Changelog del diagrama de entidades

### 1º Iteración

Este es el diagrama original que se entregó el dia de la primera parte

| ![1º DiagramaEntidades](images/diagramaEntidadesIteracion1.svg) |
| :--- |
| [Ver código](modelosUML/diagramaEntidadesIteracion1.puml) |

### 2º Iteración

Cambios:
- Implementación de la corrección que expliqué en la segunda parte del examen: "Trigger" también actúa sobre "Vista" y "Tabla" tiene "Trigger"
- Adición de los atributos "evento activacion" y "momento activación" y sus respectivos tipos a la entidad "Trigger"
- Modificación de la fortaleza de la relación "Indice"-"Campo"
- Modificación del texto de la relación "Campo"-"Llave" para mostrar que un campo puede ser una llave

| ![2º DiagramaEntidades](images/diagramaEntidadesIteracion2.svg) |
| :--- |
| [Ver código](modelosUML/diagramaEntidadesIteracion2.puml) |

### 3º Iteración 

Cambios:
- Adición del atributo "enunciado" a la entidad "Consulta"
- Adición del atributo "nombre" a la entidad "Rol"
- Adición del atributo "capacidad" y sus tipos a la entidad "Permiso"

| ![3º DiagramaEntidades](images/diagramaEntidadesIteracion3.svg) |
| :--- |
| [Ver código](modelosUML/diagramaEntidadesIteracion3.puml) |

### 4º Iteración

Cambios:
- Implementación de jerarquía entre las entidades

| ![4º DiagramaEntidades](images/diagramaEntidadesIteracion4.svg) |
| :--- |
| [Ver código](modelosUML/diagramaEntidadesIteracion4.puml) |

### 5º Iteración 

Cambios:
- Adición de los atributos "nombre" y "tipo" a la entidad "Campo"
- Adición del atributo "tipo" a la entidad "Llave"
- Adición del atributo "tipo" y sus respectivos tipos a la entidad "Restriccion"

| ![5º DiagramaEntidades](images/diagramaEntidadesIteracion5.svg) |
| :--- |
| [Ver código](modelosUML/diagramaEntidadesIteracion5.puml) |

## Diagramas de objetos

### Diagrama de objetos de un sistema de gestión academica

| ![1º Diagrama de objetos](images/diagramaObjetos1.svg) |
| :--- |
| [Ver código](modelosUML/diagramaObjetos1.puml) |

### Diagrama de objetos de un sistema de inventario

| ![2º Diagrama de objetos](images/diagramaObjetos2.svg) |
| :--- |
| [Ver código](modelosUML/diagramaObjetos2.puml) |