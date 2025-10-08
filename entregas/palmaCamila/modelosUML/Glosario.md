# Modelo de Dominio: Presupuesto

Este modelo de dominio representa la estructura lógica de un sistema de **gestión de presupuestos** para proyectos de software. Se enfoca en planificar, controlar y estimar elementos como costos, tiempos, ingresos, egresos y recursos humanos a lo largo de las fases del proyecto.

---

##  Componentes Principales del Modelo

### 1. `Presupuesto`
Entidad principal que representa la estimación económica de un proyecto. Está compuesto por:
- Un `Proyecto`
- Un bloque de `Dinero` (finanzas generales)
- Fases y costos

### 2. `Proyecto`
Representa el proyecto de software al que está asignado el presupuesto. Puede tener múltiples fases.

### 3. `Fase`
Etapas del ciclo de vida del proyecto. Cada fase:
- Pertenece a un proyecto
- Tiene un presupuesto (`Dinero`) asignado
- Contiene múltiples `Actividades`

### 4. `Actividad`
Unidad de trabajo específica dentro de una fase. Consume tiempo (`Horas`) y requiere personal (`RRHH`).

### 5. `RRHH` (Recursos Humanos)
Personas asignadas a las actividades. Se asume que tienen un costo asociado por hora.

### 6. `Horas`
Tiempo estimado o trabajado sobre una actividad. Se relaciona con `Dinero` porque permite calcular costos en base a tarifas.

### 7. `Dinero`
Entidad que agrupa la parte financiera. Puede representar:
- El total del presupuesto
- Lo asignado a una fase
- El resultado de las horas trabajadas

Incluye dos entidades financieras:
- `Ingreso`: Aportes, ventas, inversión
- `Egreso`: Pagos, sueldos, herramientas
