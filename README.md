## 👋 Estibaliz Etxaburu — Data Engineer

Especializada en pipelines **ETL/ELT**, **modernización legacy** y **calidad del dato**.  
Experiencia real en Accenture/Repsol con Azure, Python y FastAPI en entornos industriales.  
Construyo sistemas donde la **trazabilidad** y la **integridad del dato** no son opcionales.

📍 Alicante · [LinkedIn](https://www.linkedin.com/in/estibaliz-etxaburu-lekube-5011b75b/)

---

## ⚙️ Stack

| Área | Tecnologías |
| :--- | :--- |
| **Data Engineering** | PySpark, ETL/ELT, Parquet, JSONL, Batch Processing |
| **Validación & Calidad** | Pydantic, Schema Enforcement, Data Quality, Hash Chains |
| **Cloud & DevOps** | Azure (Key Vault, Log Analytics, DevOps), Docker, CI/CD |
| **Legacy & Mainframe** | COBOL, JCL, Copybooks, Fixed-Width, Spring Batch |
| **Observabilidad** | Grafana, Azure Log Analytics, RabbitMQ, Kafka |

---

## 📌 Proyectos destacados

| Proyecto | Stack | Qué demuestra |
| :--- | :--- | :--- |
| **[data-engineer-portfolio](https://github.com/eetxlek/data-engineer-portfolio)** | PySpark, Pydantic, Docker, MinIO, Parquet | Pipeline ETL/ELT end-to-end Legacy → Data Lake |
| **[mainframe-migration-spring-batch-cobol](https://github.com/eetxlek/mainframe-migration-spring-batch-cobol)** | Spring Batch, Java 17, COBOL | Migración batch legacy → arquitectura moderna |
| **[COBOL-Fixed-Width-Parser-API](https://github.com/eetxlek/COBOL-Fixed-Width-Parser-API)** | FastAPI, Pydantic | Interoperabilidad COBOL ↔ JSON para pipelines ETL |
| **[industrial-telemetry-api](https://github.com/eetxlek/industrial-telemetry-api)** | FastAPI, RabbitMQ, PostgreSQL, SHA-256 | Data integrity + trazabilidad criptográfica |

---

## 🔍 En detalle

### 🏗️ End-to-End Data Pipeline: Legacy → Data Lake
*Repositorio:* [data-engineer-portfolio](https://github.com/eetxlek/data-engineer-portfolio)

```
┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐
│   Legacy System  │───▶│    Validator     │────▶│      Spark       │───▶│    Data Lake     │
│   (Simulador)    │     │   (Pydantic)     │     │    (PySpark)     │     │    (Parquet)     │
└──────────────────┘     └──────────────────┘     └──────────────────┘     └──────────────────┘
         │                        │                        │                        │
         ▼                        ▼                        ▼                        ▼
 raw_siniestros.jsonl    válidos/inválidos         Transformaciones         Particionado por
                         (separación datos)        (enriquecimiento)        tipo_seguro / año
```

**El problema:** Demostrar un pipeline ETL/ELT completo desde sistemas legacy 
hasta un Data Lake moderno, con validación, calidad del dato y almacenamiento 
optimizado para analítica.

**Mi solución:** Pipeline end-to-end con generación de datos sintéticos legacy, 
validación de reglas de negocio con Pydantic, procesamiento distribuido con PySpark, 
almacenamiento en Parquet particionado por dominio y simulación de cloud con MinIO.

**Resultado:** 95 de 100 registros procesados correctamente, separación automática 
válidos/inválidos, trazabilidad completa por fase y entorno Data Platform 
reproducible en local con Docker Compose.

---

**[Migración Mainframe → Spring Batch](https://github.com/eetxlek/mainframe-migration-spring-batch-cobol)** — Migración de proceso batch crítico COBOL a Java 17 con Spring Batch manteniendo lógica 1:1. Resultado: 10x más rápido, testeable y mantenible.

**[COBOL Fixed-Width Parser API](https://github.com/eetxlek/COBOL-Fixed-Width-Parser-API)** — API REST que parsea archivos fixed-width COBOL (DISPLAY, COMP, COMP-3) a JSON y viceversa para interoperabilidad en pipelines ETL.

**[Data Integrity & Validation Pipeline](https://github.com/eetxlek/industrial-telemetry-api)** — Pipeline con hash chain SHA-256 que garantiza integridad criptográfica de telemetría industrial con endpoint de auditoría completo.

---

## 💡 Lo que me mueve

- La **calidad del dato** no es un extra: es el requisito no negociable.
- La **trazabilidad** convierte un pipeline frágil en uno fiable.
- La **modernización legacy** no es solo migrar código: es preservar lógica 
  de negocio mientras se gana en escalabilidad y mantenibilidad.

---

## 📫 ¿Conectamos?

Si buscas a alguien especializada en **Data Engineering**, **pipelines ETL/ELT** 
o **modernización legacy → cloud**, hablemos.

[LinkedIn](https://www.linkedin.com/in/estibaliz-etxaburu-lekube-5011b75b/)
