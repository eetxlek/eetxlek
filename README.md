## 👋 Sobre mí

Backend developer con experiencia en **integración de datos industriales** (Repsol/Accenture) y **modernización de sistemas legacy** (migración COBOL → Java).

Mi enfoque transversal es garantizar la **integridad y trazabilidad del dato**, ya sea en flujos críticos de IoT, en migraciones de mainframe o en APIs event-driven.

Tengo experiencia real en entornos cloud (Azure, Kubernetes, Grafana) y también construyo sistemas desde cero con arquitectura hexagonal y EDA.

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

## 🔍 En detalle

### 🚀 Migración Mainframe → Spring Batch
*Repositorio:* [mainframe-migration-spring-batch-cobol](https://github.com/eetxlek/mainframe-migration-spring-batch-cobol)

**El problema:** Migrar un proceso batch crítico (PB0EC319) de mainframe a Java.

**Mi solución:** Migración a Java 17 con Spring Batch manteniendo lógica 1:1, lookup O(1) con HashMap, chunk-oriented processing con restart automático.

**Resultado:** Misma lógica, 10x más rápido, testeable, mantenible.

### 🔄 COBOL Fixed-Width Parser API
*Repositorio:* [COBOL-Fixed-Width-Parser-API](https://github.com/eetxlek/COBOL-Fixed-Width-Parser-API)

**El problema:** Los sistemas modernos necesitan consumir datos de mainframe, pero los archivos COBOL usan formatos de longitud fija y tipos específicos (DISPLAY, COMP, COMP-3).

**Mi solución:** API REST con FastAPI y Pydantic que parsea archivos fixed-width a JSON y viceversa, con soporte para COMP/COMP-3 y validaciones automáticas.

### 📡 Industrial Telemetry API
*Repositorio:* [industrial-telemetry-api](https://github.com/eetxlek/industrial-telemetry-api)

**El problema:** En plantas industriales, los datos de sensores pueden ser manipulados, llevando a decisiones peligrosas.

**Mi solución:** API con hash chain (SHA-256) que encadena cada lectura con la anterior, arquitectura hexagonal, event-driven con RabbitMQ y endpoint de auditoría.

## 💡 Lo que me mueve

- La **integridad del dato** no es un extra: es el requisito no negociable.
- La **trazabilidad** convierte un sistema frágil en uno fiable.
- La **arquitectura limpia** es la diferencia entre un proyecto mantenible y uno que no.

## 📫 ¿Conectamos?

Si buscas a alguien que entienda de **migración legacy → moderno** o **integraciones robustas con trazabilidad**, hablemos.

[LinkedIn](https://www.linkedin.com/in/estibaliz-etxaburu-lekube-5011b75b/)
