# ELT End-to-End en Azure con ADF y Databricks

## 📌 Descripción
Pipeline ELT automatizado que ingesta datos crudos en ADLS Gen2,
los transforma usando Azure Databricks y los organiza en una
arquitectura Lakehouse (RAW → SILVER → GOLD).

## 🏗️ Arquitectura
- Azure Data Factory (orquestación)
- Azure Data Lake Gen2 (storage)
- Azure Databricks (transformaciones)
- Delta Lake (formato)


## 🔄 Flujo del pipeline
1. Trigger diario inicia la ingesta
2. ADF copia datos a capa RAW
3. ADF ejecuta Job de Databricks
4. Databricks transforma:
   - RAW → SILVER (limpieza, tipado)
   - SILVER → GOLD (modelo analítico)
5. Datos listos para BI o analítica

## 🧠 Decisiones técnicas
- Delta Lake para ACID y versionado
- Jobs de Databricks para ejecución automática
- Separación clara de responsabilidades (ADF vs Databricks)

## 🚀 Resultado
Pipeline completamente automatizado sin intervención manual.
