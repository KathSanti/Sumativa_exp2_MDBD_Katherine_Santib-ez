# Sistema de Gestión de Base de Datos: Retail Solari S.A.

Este proyecto consiste en el diseño e implementación de la base de datos para Solari S.A., una empresa dedicada a la comercialización 
de productos esenciales. El diseño abarca desde el análisis de requerimientosde negocio hasta la generación del script DDL para un entorno Oracle Database 11g.

## Arquitectura del Modelo

### 1. Modelo Lógico (MER-E)
Se aplicó la notación de **Barker** para representar la lógica del negocio:
- **Jerarquías de Herencia:** Se implementó la especialización en la entidad `PRODUCTO`  y `PROVEEDOR` (Empresa vs. Persona Natural) para cumplir con el **Criterio 4** de la evaluación.
- **Normalización Geográfica:** Se estructuró la cadena  `COMUNA` -> `DIRECCION` -> `SUCURSAL` para evitar redundancia y cumplir con la **Tercera Forma Normal (3NF)**.

### 2. Modelo Relacional
Transformación técnica del MER-E donde se destaca:
- **Entidades Asociativas:** Uso de `DETALLE_BOLETA` para resolver la relación N:M entre `BOLETA` y `PRODUCTO`, permitiendo el registro de precios históricos y cantidades.

---

## Herramientas Utilizadas
- **Software CASE:** Oracle SQL Developer Data Modeler 24.3.
- **Motor de Base de Datos:** Oracle Database 11g.
