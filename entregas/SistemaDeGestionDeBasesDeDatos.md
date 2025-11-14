# Modelos del Sistema de Gestión de Bases de Datos

## 1. Diagrama de estados (BDD)
El primer modelo es un diagrama de estados que muestra de forma general cómo se comportan los elementos principales dentro de un sistema de gestión de bases de datos. No entra en detalles de implementación, sino que enseña el funcionamiento lógico del sistema: qué componentes intervienen, cómo se relacionan entre ellos y qué papel tiene cada uno.

Se representan estados como la base de datos organizada en esquemas, usuarios que ejecutan consultas y tienen roles asignados, tablas con sus campos e índices, y las validaciones que se activan mediante restricciones. También aparece la relación entre claves primarias y foráneas, que es esencial en cualquier diseño de bases de datos.

En conjunto, este modelo sirve para entender cómo funciona de manera global un sistema de gestión de BDD.

## 2. Diagrama de objetos – Gestión académica
El segundo modelo es un ejemplo práctico basado en el diagrama anterior, pero con objetos concretos. Representa un caso académico sencillo en el que se usa una base de datos llamada BD_GESTION, un usuario administrador con su rol, un esquema principal y una tabla Usuario con sus campos, índice, clave primaria y una restricción básica. Además, se incluye una consulta típica para obtener información de usuarios.

Este diagrama permite ver cómo se aplica el modelo conceptual en un caso real y más fácil de entender.

## 3. Diagrama de objetos – Gestión de copias
El tercer modelo es otro caso práctico, pero aplicado al ámbito de las copias de seguridad y los registros del sistema. En este caso aparece una base de datos llamada BD_COPIAS, un usuario encargado de gestionar las copias, su rol, el esquema del sistema y la tabla LogCopias con su campo principal, clave primaria, índice, restricciones y la clave foránea relacionada con el usuario. También se añade una consulta centrada en recuperar los errores recientes.

Este diagrama ayuda a ver cómo el mismo modelo se puede aplicar a situaciones distintas sin modificar su estructura.

## Resumen
El diagrama de estados muestra la lógica general del sistema de bases de datos y los dos diagramas de objetos ofrecen ejemplos concretos basados en ese modelo, cada uno aplicado a un contexto diferente.
