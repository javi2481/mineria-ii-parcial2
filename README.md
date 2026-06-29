# Segundo Parcial — Minería de Datos II

Pipeline PySpark con arquitectura medallion: landing → bronze → silver → gold → AstraDB.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/javi2481/mineria-ii-parcial2/blob/main/parcial2_colab.ipynb)

## Carpetas

- **`parcial2_colab.ipynb`** — el pipeline completo
- **`datalake/landing/`** — datos crudos (CSV + JSONL)
- **`cql/`** — scripts para la consola CQL de Astra
- **`docs/decision_log.md`** — apuntes de decisiones

## Qué pide el examen (sección del notebook)

1. Bronze batch — 3 CSV con esquema manual
2. Bronze streaming — watermark + checkpoint
3. Silver — 3 reglas + quarantine
4. Gold — resumen diario por org/día/servicio
5. Astra — `foreachBatch` + 2 consultas
6. Idempotencia
7. CQL + README + decision log

## Cómo correr

1. Abrir en Colab (badge de arriba)
2. **Entorno de ejecución → Ejecutar todo**
3. La primera vez clona el repo en `/content/mineria-ii-parcial2`
4. En Colab, crear Secret `ASTRA_TOKEN` con tu token de Astra (o pegarlo en la celda 15)

## Consultas Astra

Tabla: `default_keyspace.examen_mineria_II`  
Scripts: [`cql/02_queries.cql`](cql/02_queries.cql)

- Consulta 1: `org_pbhsahxt`, día `2025-08-01`
- Consulta 2: misma org, `compute`, jul–ago 2025

## Equipo

- Lucas Dugo
- Cristian Lo Giudice
- Rodolfo Berrone
- Santiago Ham Saguier
- Andrea Romeo
