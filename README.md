## 👋 Sobre mí

Data Engineer especializada en **pipelines ETL/ELT**, **modernización de sistemas 
legacy** y **calidad del dato** en entornos industriales.

Experiencia real en Accenture/Repsol trabajando con Azure, Python y FastAPI en 
pipelines de ingesta de datos industriales. Construyo proyectos orientados a 
trazabilidad, data quality y arquitecturas lakehouse modernas.

Mi enfoque: llevar datos desde sistemas legacy (COBOL/mainframe) hasta plataformas 
cloud modernas, garantizando integridad y observabilidad en cada paso.

---

## ⚙️ Stack principal

| Área | Tecnologías |
| :--- | :--- |
| **Data Engineering** | PySpark, ETL/ELT, Parquet, JSONL, Batch Processing |
| **Validación & Calidad** | Pydantic, Schema Enforcement, Data Quality, Hash Chains |
| **APIs & Backend** | FastAPI, Python, Spring Batch, Java 17 |
| **Cloud & DevOps** | Azure (Key Vault, Log Analytics, DevOps), Docker, CI/CD |
| **Legacy & Mainframe** | COBOL, JCL, Copybooks, Fixed-Width, Mainframe Integration |
| **Observabilidad** | Grafana, Azure Log Analytics, métricas, alertas |
| **Mensajería** | Kafka, RabbitMQ |
| **Persistencia** | PostgreSQL, MySQL, Redis |

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

**El problema:** Demostrar un pipeline ETL/ELT completo desde sistemas legacy 
hasta un Data Lake moderno, con validación, calidad del dato y almacenamiento 
optimizado para analítica.

**Mi solución:** Pipeline end-to-end con generación de datos sintéticos legacy, 
validación de reglas de negocio con Pydantic, procesamiento distribuido con PySpark, 
almacenamiento en Parquet particionado por dominio y simulación de cloud con MinIO.

**Resultado:** Arquitectura reproducible con Docker Compose, separación automática 
de registros válidos/inválidos y data quality garantizada en cada fase del pipeline.

---

### 🚀 Migración Mainframe → Spring Batch
*Repositorio:* [mainframe-migration-spring-batch-cobol](https://github.com/eetxlek/mainframe-migration-spring-batch-cobol)

**El problema:** Migrar un proceso batch crítico de mainframe a una arquitectura 
moderna preservando lógica e integridad del procesamiento.

**Mi solución:** Migración a Java 17 con Spring Batch manteniendo lógica 1:1, 
lookup O(1) con HashMap y chunk-oriented processing con restart automático.

**Resultado:** Misma lógica, 10x más rápido, testeable y mantenible.

---

### 🔄 COBOL Fixed-Width Parser API
*Repositorio:* [COBOL-Fixed-Width-Parser-API](https://github.com/eetxlek/COBOL-Fixed-Width-Parser-API)

**El problema:** Los pipelines ETL modernos necesitan consumir datos de mainframe 
en formatos COBOL de longitud fija (DISPLAY, COMP, COMP-3).

**Mi solución:** API REST con FastAPI y Pydantic que parsea fixed-width a JSON 
y viceversa, con validaciones automáticas para interoperabilidad en pipelines ETL.

---

### 📡 Data Integrity & Validation Pipeline
*Repositorio:* [industrial-telemetry-api](https://github.com/eetxlek/industrial-telemetry-api)

**El problema:** Garantizar que los datos de sensores industriales no sean 
manipulados antes de llegar al sistema analítico.

**Mi solución:** Pipeline con hash chain (SHA-256) que encadena cada registro 
con el anterior, arquitectura hexagonal y endpoint de auditoría para trazabilidad 
completa.

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
