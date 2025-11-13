# 🧩 Correcciones  
**Proyecto:** *Gestor de Bases de Datos – Modelo del Dominio*  

---

## 📘 Resumen General  
El **segundo diagrama** mantiene la estructura general del primero, pero introduce **ajustes en las relaciones entre clases**, mejorando la **semántica de uso y contención** entre entidades del modelo.

---

| Versión | Archivo UML | Vista SVG |
|:--|:--|:--|
| **Diagrama 1** | [diagrama1.uml](./diagramas/diagrama1/diagrama1.uml) | [diagrama1.svg](./diagramas/diagrama1/diagrama1.svg) |
| **Diagrama 2** | [diagrama2.uml](./diagramas/diagrama2/diagrama2.uml) | [diagrama2.svg](./diagramas/diagrama2/diagrama2.svg) |

---

##  Cambios Principales  

### 1. Relación entre `Tabla` y `Trigger`
- **Antes (Diagrama 1):**  
  La relación entre `Tabla` y `Trigger` estaba etiquetada como **“usa”** (unidireccional).  
- **Ahora (Diagrama 2):**  
  Se mantiene la relación, pero se **añade una conexión adicional** desde `Atributo` hacia `Trigger` con la etiqueta **“usa”**, indicando que los atributos también pueden activar o formar parte de un disparador (`Trigger`).


---

### 2. Ajuste Visual del Diagrama
Se realizaron **mejoras en la disposición visual** para facilitar la lectura y comprensión del modelo:

- `Trigger` fue **reubicado en una posición central**.  
- Las líneas de relación **“usa”** y **“contiene”** fueron **redibujadas** para reducir cruces visuales y mejorar la claridad estructural.  


