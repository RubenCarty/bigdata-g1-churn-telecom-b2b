# Proceso ETL (Extract, Transform and Load)

## Objetivo

Diseñar e implementar el proceso ETL para consolidar la información proveniente de múltiples fuentes de datos y generar un conjunto de datos confiable para el análisis de churn de clientes B2B.

---

# Arquitectura ETL

```text
Fuentes CSV
│
├── empresas.csv
├── servicios.csv
├── consumo.csv
├── facturacion.csv
├── tickets.csv
├── eventos_red.csv
└── churn.csv
      │
      ▼
Extracción
      │
      ▼
Transformación
      │
      ▼
Validación
      │
      ▼
Dataset Integrado
      │
      ▼
Data/Processed
```

---

# Fase 1: Extracción

## Objetivo

Obtener la información desde los archivos fuente ubicados en el directorio:

```text
data/raw/
```

## Archivos procesados

* empresas.csv
* servicios.csv
* consumo.csv
* facturacion.csv
* tickets.csv
* eventos_red.csv
* churn.csv

## Herramientas utilizadas

* Python
* Pandas

---

# Fase 2: Transformación

## Actividades realizadas

### Estandarización de nombres

Se normalizaron los nombres de columnas utilizando formato snake_case.

Ejemplo:

```text
Fecha Alta → fecha_alta
Monto Facturado → monto_facturado
```

### Conversión de tipos de datos

Se transformaron columnas a tipos adecuados:

| Campo         | Tipo     |
| ------------- | -------- |
| fecha_alta    | datetime |
| fecha_consumo | datetime |
| fecha_ticket  | datetime |
| monto         | float    |
| churn         | integer  |

### Eliminación de duplicados

Se identificaron registros duplicados utilizando:

```text
id_empresa
fecha
```

### Tratamiento de valores nulos

Se aplicaron reglas de imputación según el tipo de dato.

Ejemplos:

* Promedio para variables numéricas.
* Valor "Desconocido" para variables categóricas.

---

# Fase 3: Integración

## Clave de integración

```text
id_empresa
```

Todas las tablas fueron relacionadas utilizando el identificador único de empresa.

## Resultado

Se obtuvo un dataset consolidado que integra:

* Información comercial
* Información financiera
* Información operativa
* Información de soporte
* Información técnica
* Variable objetivo de churn

---

# Fase 4: Carga

El resultado final fue almacenado en:

```text
data/processed/
```

Formato utilizado:

```text
Parquet
```

Beneficios:

* Menor tamaño.
* Mayor velocidad de lectura.
* Compatibilidad con Big Data.

---

# Resultado Esperado

Generar una base consolidada y confiable que permita realizar análisis exploratorios y desarrollar modelos predictivos de Machine Learning.
