# Análisis de Calidad de Datos

## Objetivo

Evaluar la calidad de la información utilizada en el proyecto para garantizar la confiabilidad de los resultados obtenidos durante el análisis y modelado predictivo.

---

# Dimensiones Evaluadas

## Completitud

Mide la presencia de información en cada atributo.

### Validación

```text
Porcentaje de valores nulos
Porcentaje de registros incompletos
```

### Resultado

Los conjuntos de datos presentan niveles aceptables de completitud para el desarrollo del proyecto.

---

## Consistencia

Mide la uniformidad de los datos entre diferentes fuentes.

### Validaciones realizadas

* Formatos de fecha.
* Tipos de datos.
* Integridad de identificadores.
* Correspondencia de claves entre tablas.

### Resultado

No se encontraron inconsistencias críticas que afecten la integración de datos.

---

## Unicidad

Mide la existencia de registros duplicados.

### Validación

Se verificó la unicidad de:

```text
id_empresa
id_ticket
id_factura
id_evento
```

### Resultado

Los registros duplicados fueron identificados y eliminados durante el proceso ETL.

---

## Validez

Mide si los valores cumplen reglas de negocio.

### Ejemplos

Facturación:

```text
monto >= 0
```

Consumo:

```text
consumo_gb >= 0
```

Churn:

```text
0 = Cliente activo
1 = Cliente abandonó
```

### Resultado

Los datos cumplen las reglas definidas para el proyecto.

---

## Integridad Referencial

Se verificó que todas las tablas secundarias posean una relación válida con la tabla principal.

### Relación validada

```text
empresas.id_empresa
```

Tablas relacionadas:

* servicios
* consumo
* facturacion
* tickets
* eventos_red
* churn

### Resultado

No se identificaron registros huérfanos significativos.

---

# Indicadores de Calidad

| Indicador              | Resultado |
| ---------------------- | --------- |
| Completitud            | > 95%     |
| Consistencia           | Alta      |
| Unicidad               | Validada  |
| Integridad Referencial | Validada  |
| Calidad General        | Aprobada  |

---

# Riesgos Identificados

* Posibles inconsistencias históricas en fechas.
* Registros con información faltante en atributos secundarios.
* Variaciones en formatos provenientes de distintas fuentes.

---

# Acciones Correctivas

* Limpieza automática de datos.
* Normalización de formatos.
* Validaciones de negocio.
* Eliminación de duplicados.
* Imputación controlada de valores nulos.

---

# Conclusión

La calidad de los datos es adecuada para continuar con las siguientes fases del proyecto, incluyendo el análisis exploratorio, la construcción de variables predictivas y el entrenamiento de modelos de Machine Learning para la predicción de churn de clientes B2B.
