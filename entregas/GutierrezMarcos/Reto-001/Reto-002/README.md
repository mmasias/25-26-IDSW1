# ☕ Modelo del Dominio: Cafetería

Este documento describe el **modelo del dominio** para un sistema de gestión de una **cafetería**.  
El objetivo del modelo es representar las entidades principales y las relaciones que intervienen en los procesos operativos, desde la atención al cliente hasta la gestión de inventario y pedidos.

---

## 🧩 Descripción general

El sistema de la cafetería permite administrar:
- Los **pedidos** realizados por los clientes.  
- La **preparación de comandas** por parte de los empleados.  
- El **inventario** y los movimientos de stock.  
- La **gestión de productos**, menús y categorías.  
- Los **pagos** y asignación de mesas.  
- La **relación con proveedores** y los **turnos de trabajo** del personal.

---

## 🏗️ Entidades principales

### ☕ Cliente
Representa a la persona que realiza pedidos en la cafetería.  
**Atributos:**
- nombre  
- teléfono  
- email  

**Relaciones:**
- Realiza uno o varios **Pedidos**.

---

### 🧾 Pedido
Representa una orden solicitada por un cliente.  
**Atributos:**
- número  
- fecha  
- estado  
- total  

**Relaciones:**
- Es **realizado por** un **Cliente**.  
- **Genera** una o varias **Comandas**.  
- **Se paga con** un **Pago**.  
- Puede estar **asignado a** una **Mesa**.

---

### 🍽️ Comanda
Documento interno que indica qué productos deben prepararse.  
**Atributos:**
- número  
- hora  
- estado  

**Relaciones:**
- **Incluye** varios **Productos**.  
- Es **atendida por** un **Empleado**.  
- Se **genera desde** un **Pedido**.

---

### 🥐 Producto
Elemento que se ofrece en la cafetería (bebidas, comidas, postres).  
**Atributos:**
- nombre  
- precio  
- descripción  
- tipo  

**Relaciones:**
- **Clasificado por** una **Categoría**.  
- **Incluido en** un **Menú**.  
- **Registrado en** el **Inventario**.

---

### 🗂️ Categoría
Permite agrupar los productos (por ejemplo: “Bebidas calientes”, “Postres”).  
**Atributos:**
- nombre  
- descripción  

**Relaciones:**
- **Clasifica** varios **Productos**.

---

### 📋 Menú
Agrupación de productos disponibles en un periodo determinado.  
**Atributos:**
- nombre  
- fechaVigencia  

**Relaciones:**
- **Contiene** varios **Productos**.

---

### 👨‍🍳 Empleado
Trabajador de la cafetería (barista, camarero, cocinero, etc.).  
**Atributos:**
- nombre  
- puesto  

**Relaciones:**
- **Atiende** **Comandas**.  
- **Asignado a** un **Turno**.

---

### 🕐 Turno
Bloque horario asignado a empleados.  
**Atributos:**
- horaInicio  
- horaFin  

**Relaciones:**
- **Asigna** uno o varios **Empleados**.

---

### 📦 Inventario
Controla los productos y materiales en existencia.  
**Atributos:**
- código  
- fechaActualización  

**Relaciones:**
- **Contiene** **Stock**.  
- **Afectado por** **Movimientos de Inventario**.  
- **Registra** los **Productos**.

---

### 📊 Stock
Cantidad disponible de cada producto o insumo.  
**Atributos:**
- cantidadDisponible  
- umbralMinimo  

**Relaciones:**
- **Abastecido por** **Proveedores**.  
- **Controlado por** el **Inventario**.

---

### 🚚 Proveedor
Fuente de abastecimiento de productos o materias primas.  
**Atributos:**
- nombre  
- teléfono  
- email  

**Relaciones:**
- **Abastece** el **Stock**.

---

### 🔄 Movimiento de Inventario
Registro de entradas y salidas de inventario.  
**Atributos:**
- tipo (entrada/salida)  
- cantidad  
- fecha  

**Relaciones:**
- **Afecta** el **Inventario**.

---

### 🍴 Mesa
Ubicación física donde el cliente realiza su pedido.  
**Atributos:**
- número  
- capacidad  

**Relaciones:**
- **Asignada a** uno o varios **Pedidos**.

---

### 💳 Pago
Transacción asociada a un pedido.  
**Atributos:**
- monto  
- fecha  
- método (efectivo, tarjeta, etc.)  

**Relaciones:**
- **Asociado a** un **Pedido**.

---

## 🧠 Resumen de Relaciones

| Entidad Origen | Relación | Entidad Destino |
|----------------|-----------|----------------|
| Cliente | realiza | Pedido |
| Pedido | genera | Comanda |
| Comanda | incluye | Producto |
| Producto | clasificado por | Categoría |
| Menú | contiene | Producto |
| Empleado | atiende | Comanda |
| Empleado | asignado a | Turno |
| Producto | registrado en | Inventario |
| Inventario | controla | Stock |
| Stock | abastecido por | Proveedor |
| MovimientoInventario | afecta | Inventario |
| Pedido | se paga con | Pago |
| Pedido | asignado a | Mesa |

---

![UML](marcosgutierrez6/25-26-IDSW1/entregas/GutierrezMarcos/Reto-001/Reto-002/uml/diagrama-cafeteria.svg)