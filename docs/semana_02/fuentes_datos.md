# Fuentes de Datos

## Objetivo

Identificar y documentar las fuentes de información que serán utilizadas para la construcción del modelo predictivo de churn para clientes B2B de telecomunicaciones.

---

# Descripción General

El proyecto utiliza siete conjuntos de datos que representan diferentes dimensiones del comportamiento de los clientes empresariales.

Estas fuentes permiten analizar variables comerciales, financieras, operativas y de experiencia del cliente para identificar patrones asociados al abandono del servicio.

---

# empresas.csv

## Descripción

Contiene la información maestra de los clientes corporativos.

## Propósito

Permite caracterizar a cada empresa y segmentarla según sus atributos de negocio.

## Información esperada

* ID Empresa
* RUC
* Razón Social
* Sector Económico
* Región
* Tamaño Empresa
* Fecha Alta

## Uso en el Modelo

Generación de variables demográficas y de segmentación.

---

# servicios.csv

## Descripción

Contiene los servicios contratados por cada empresa.

## Propósito

Analizar el nivel de vinculación comercial del cliente.

## Información esperada

* Internet
* Telefonía
* VPN
* Datacenter
* Cloud
* Seguridad

## Uso en el Modelo

Construcción de indicadores de cantidad y tipo de servicios contratados.

---

# consumo.csv

## Descripción

Registra el consumo histórico de los servicios.

## Propósito

Analizar cambios de comportamiento y patrones de uso.

## Uso en el Modelo

* Consumo promedio
* Variación de consumo
* Tendencias de disminución

---

# facturacion.csv

## Descripción

Información financiera y de pagos.

## Propósito

Analizar comportamiento económico del cliente.

## Uso en el Modelo

* Facturación promedio
* Morosidad
* Variación de ingresos

---

# tickets.csv

## Descripción

Registra incidencias y solicitudes de soporte.

## Propósito

Medir satisfacción y experiencia del cliente.

## Uso en el Modelo

* Cantidad de tickets
* Tickets críticos
* Tiempo de resolución

---

# eventos_red.csv

## Descripción

Incidentes técnicos relacionados con la infraestructura de red.

## Propósito

Medir calidad del servicio entregado.

## Uso en el Modelo

* Cantidad de incidentes
* Tiempo de indisponibilidad
* Frecuencia de fallas

---

# churn.csv

## Descripción

Tabla objetivo utilizada para el entrenamiento del modelo.

## Propósito

Identificar qué clientes abandonaron los servicios.

## Variable Objetivo

* 0 = Cliente Activo
* 1 = Cliente con Churn

---

# Conclusión

La integración de estas siete fuentes permitirá construir una visión 360° del cliente corporativo y desarrollar modelos predictivos capaces de anticipar el abandono con 90 días de anticipación.
