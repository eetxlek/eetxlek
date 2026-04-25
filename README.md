## 👋 Sobre mí

Backend developer especializado en **modernización de sistemas legacy** y **arquitecturas de integración**.

Mi enfoque principal es la migración de mainframe (COBOL) a Java moderno con Spring Batch, asegurando la **integridad y trazabilidad del dato** en cada etapa del proceso. No solo traslado lógica: la rediseño para que sea mantenible, testeable y escalable.

Fuera del mundo mainframe, construyo **sistemas de integración** con FastAPI y arquitecturas **event-driven (EDA)** usando RabbitMQ. Me interesa que los sistemas hablen entre sí de forma fiable, asíncrona y con bajo acoplamiento.

> 📄 Más sobre mi experiencia profesional en [LinkedIn](https://www.linkedin.com/in/estibaliz-etxaburu-lekube-5011b75b/)

## ⚙️ Stack principal

| Área | Tecnologías |
| :--- | :--- |
| **Migración & Batch** | Spring Batch, Java 17, COBOL |
| **APIs & Backend** | FastAPI, Spring Boot, Python, Java |
| **Mensajería (EDA)** | RabbitMQ, event-driven patterns |
| **Persistencia** | PostgreSQL, MySQL, Redis |
| **Data Integrity** | Hash chains (SHA-256), validaciones, trazabilidad |
| **Infraestructura** | Docker, Kubernetes, Azure, Grafana, GitHub Actions |

## 📌 Proyectos destacados

| Proyecto | Stack | Qué demuestra |
| :--- | :--- | :--- |
| **[mainframe-migration-spring-batch-cobol](https://github.com/eetxlek/mainframe-migration-spring-batch-cobol)** | Spring Batch, Java 17, COBOL | Migración 1:1 de proceso legacy → moderno |
| **[industrial-telemetry-api](https://github.com/eetxlek/industrial-telemetry-api)** | FastAPI, RabbitMQ, PostgreSQL, SHA-256 | EDA + hash chain para integridad criptográfica |
| **[COBOL-Fixed-Width-Parser-API](https://github.com/eetxlek/COBOL-Fixed-Width-Parser-API)** | FastAPI, Pydantic | Puente bidireccional COBOL ↔ JSON |
| **[microservices-failure-patterns](https://github.com/eetxlek/microservices-failure-patterns)** | Python | Laboratorio de fallos en sistemas distribuidos |

## 🔍 Proyecto estrella: Migración COBOL → Spring Batch

**El problema:** Migrar un proceso batch crítico (PB0EC319) de mainframe a Java.

**Mi solución:**
- Migración a Java 17 con Spring Batch manteniendo lógica 1:1
- Optimización: lookup O(1) con HashMap vs lectura secuencial
- Chunk-oriented processing con restart automático

**Resultado:** Misma lógica, 10x más rápido, testeable, mantenible.

## 💡 Lo que me mueve

- La **integridad del dato** no es un extra: es el requisito no negociable.
- La **trazabilidad** convierte un sistema frágil en uno fiable.
- La **arquitectura limpia** es la diferencia entre un proyecto mantenible y uno que no.

## 📫 ¿Conectamos?

Si buscas a alguien que entienda de **migración legacy → moderno** o **integraciones robustas con trazabilidad**, hablemos.
