# Modelo del Dominio: Menú

## 1. Menú

El **menú** es el elemento central del modelo. Representa la lista organizada de platos que un restaurante ofrece en un momento determinado.

### Relaciones
- **Contiene** → `Sección`: un menú se divide en secciones como Entradas, Principales, Postres.
- **Tiene** → `Disponibilidad`: define cuándo está disponible (ej. almuerzo, fines de semana).
- **Se usa en** → `Turno`: el menú está disponible en ciertos turnos operativos (ej. cena).

---

## 2. Sección

Una **sección** agrupa platos dentro del menú.

### Relaciones
- **Incluye** → `Plato`: cada sección contiene una lista de platos correspondientes a esa categoría.

---

## 3. Plato

Un **plato** es una opción específica del menú que puede ser seleccionada por el cliente.

### Relaciones
- **Incluye** → `Ingrediente`: cada plato está compuesto por uno o varios ingredientes.

---

## 4. Ingrediente

Los **ingredientes** son los componentes que forman un plato.

Esta relación también conecta con la gestión de inventario y preparación en cocina.

---

## 5. Cliente

El **cliente** es quien visualiza el menú y realiza pedidos.

### Relaciones
- **Consulta** → `Menú`: el cliente accede al menú para tomar decisiones.
- **Realiza** → `Pedido`: crea un pedido con uno o más platos seleccionados del menú.

---

## 6. Pedido

El **pedido** representa la acción del cliente al seleccionar platos.

### Relaciones
- **Contiene** → `Plato`: los platos seleccionados forman parte del pedido.
- **Genera** → `Comanda`: a partir del pedido se genera una comanda para cocina.

---

## 7. Comanda

La **comanda** es la versión interna del pedido, utilizada por el personal de cocina.

### Relaciones
- **Tiene** → `Plato`: indica los platos que deben prepararse.
- **Se genera desde** → `Pedido`: deriva directamente del pedido del cliente.

---

## 8. Cocinero

El **cocinero** es responsable de preparar los platos indicados en las comandas.

### Relaciones
- **Consulta** → `Comanda`: utiliza la comanda como guía de preparación.
- **Trabaja en** → `Turno`: cada cocinero opera en uno o varios turnos de cocina.

---

## 9. Turno

El **turno** representa un bloque de tiempo durante el cual operan cocineros y se ofrece un menú específico.

### Relaciones
- **Tiene** → `Cocinero`: define qué cocineros trabajan durante ese turno.
- **Tiene** → `Menú`: define qué menú está activo en ese horario.

---

## 10. Disponibilidad

La **disponibilidad** define los horarios o fechas en los que un menú puede ser accedido o mostrado.

Por ejemplo:
- Menú de almuerzo: lunes a viernes de 12:00 a 16:00
- Menú de desayuno: todos los días de 7:00 a 11:00

---

## Diagrama


![UML](https://github.com/marcosgutierrez6/25-26-IDSW1/blob/eb096666b7ebe03e662ffc234b5cd2b92479096d/entregas/GutierrezMarcos/Reto-001/uml/menu.svg)
