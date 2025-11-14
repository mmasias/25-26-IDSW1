# Modelos del Sistema de Gestión de Bases de Datos

## 1. Diagrama de estados (BDD)
El primer modelo es un diagrama de estados que muestra de forma general cómo se comportan los componentes principales de un sistema de gestión de bases de datos. Refleja la lógica del sistema y cómo interactúan elementos como la base de datos, los usuarios, los roles, las consultas, los esquemas, las tablas, los campos, los índices y las claves. También se representan aspectos como las restricciones y la relación entre claves primarias y foráneas. Este modelo sirve para entender el funcionamiento global del sistema sin entrar todavía en ejemplos concretos.

## 2. Diagrama de objetos – Gestión académica
El segundo modelo es un ejemplo práctico basado en el diagrama de estados. Representa una base de datos académica sencilla donde aparece una BD llamada BD_GESTION, un usuario administrador con su rol, un esquema principal y una tabla Usuario con su campo principal, su índice, su clave primaria y una restricción básica. También se incluye una consulta típica relacionada con esta tabla. Este diagrama muestra cómo se aplica el modelo conceptual en un caso real dentro de un entorno académico.

## 3. Diagrama de objetos – Gestión de ventas
El tercer modelo es otro ejemplo práctico, pero aplicado a un sistema de ventas. En este caso aparece la base de datos BD_VENTAS, un usuario con un rol de lectura, el esquema del sistema y dos tablas principales: Cliente y Pedido. En el modelo se representan los campos más importantes, la clave primaria de cada tabla, la clave foránea que relaciona los pedidos con los clientes, además de un índice y una restricción. También se incluye una consulta enfocada en obtener los pedidos realizados por un cliente. Este diagrama muestra cómo el mismo modelo se puede aplicar a un contexto distinto sin cambiar la estructura general.

## Resumen
El diagrama de estados recoge la estructura lógica del sistema de bases de datos, mientras que los dos diagramas de objetos muestran ejemplos concretos basados en ese modelo, cada uno en un contexto diferente.

