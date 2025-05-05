# 🚇 spark-movilidad-cdmx

Análisis de movilidad del metro en la Ciudad de México usando PySpark sobre la plataforma Databricks.

---

## 📘 Descripción general

Este proyecto realiza un análisis distribuido de datos reales de afluencia del metro en CDMX. Utiliza Apache Spark a través del entorno Databricks para explorar patrones de movilidad, identificar líneas más congestionadas, horarios pico y otros aspectos clave del transporte público.

**Fuente de datos**: [Portal de Datos Abiertos CDMX](https://datos.cdmx.gob.mx/dataset/?organization=secretaria-de-movilidad)

**Archivo utilizado**: `AfluenciaMetro.csv`  
**Tamaño**: ~51 MB  
**Formato**: CSV, con columnas como `fecha`, `línea`, `estación`, `tipo de pago`, `afluencia`.

---

## 📓 Notebook: `Practica Spark PPC.ipynb`

Este notebook contiene el código desarrollado en PySpark y ejecutado en Databricks. Fue exportado en formato `.ipynb` para facilitar su visualización en GitHub y otras plataformas compatibles con Jupyter Notebooks.

### 🔍 Contenido:
- **Carga del dataset** desde CSV.
- **Transformaciones** con Spark DataFrames:
  - Conversión de tipos de datos.
  - Filtrado por columnas específicas.
  - Agregaciones (`groupBy`, `sum`).
  - Ordenamientos (`orderBy`) para encontrar valores máximos y mínimos.
- **Visualización** con `matplotlib`:
  - Gráficas de barras de afluencia por línea, estación, tipo de pago y mes.

---

## 🧠 Análisis de resultados

El análisis permitió identificar:

- Las **líneas con mayor afluencia** (Línea 2 y Línea 3).
- Las **estaciones más concurridas**, especialmente en zonas de correspondencia o conectoras como Pantitlan y Constitucion de 1917.
- El **tipo de pago predominante** en distintas líneas en su mayoria es prepago (uso de tarjeta).
- La **distribución mensual** del flujo de pasajeros a lo largo del año.

---

## 🧵 Uso de IA (documentación requerida)

Se consultó IA (ChatGPT) para resolver dudas  durante el desarrollo en Databricks. Estas consultas incluyeron:

- ✔ Corrección de sintaxis inválida en comentarios (`//` reemplazado por `#`).
- ✔ Ayuda para corregir sintaxis en funciones como `groupBy().agg()` y `orderBy()` en Spark DataFrames.
- ✔ Orientación para crear gráficas usando `matplotlib.pyplot.bar()` s.


---


🗂 Archivo Databricks (.dbc)
Este repositorio incluye un archivo .dbc que contiene el notebook original exportado desde la plataforma Databricks.

Nombre del archivo: Practica Spark PPC.dbc

Uso: Este archivo permite reimportar el notebook completo dentro de otro entorno Databricks, manteniendo la estructura, celdas y metadatos.

Limitación: No es legible directamente desde GitHub ni compatible con editores como Jupyter o Colab.

Instrucciones: Para abrirlo, ve a tu espacio de trabajo en Databricks, selecciona Import > File y carga el archivo .dbc.

📝 Este archivo se incluye como respaldo del trabajo completo realizado en Databricks, ideal para reutilización o migración del notebook.
