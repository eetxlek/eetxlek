## 👋 Sobre mí

Backend developer especializado en **modernización de sistemas legacy** y **arquitecturas de integración**.

Mi enfoque principal es la migración de mainframe (COBOL) a Java moderno con Spring Batch, asegurando la **integridad y trazabilidad del dato** en cada etapa del proceso. No solo traslado lógica: la rediseño para que sea mantenible, testeable y escalable.

Fuera del mundo mainframe, construyo **sistemas de integración** con FastAPI y arquitecturas **event-driven (EDA)** usando RabbitMQ. Me interesa que los sistemas hablen entre sí de forma fiable, asíncrona y con bajo acoplamiento.

## 💼 Experiencia profesional

**Accenture España – Backend Engineer (DataHub Industrial Repsol)** | Prácticas
*Oct 2024 – Ene 2025*

- **Integridad de Flujos Críticos:** Manejo de API Gateway (Python) para la ingesta de datos industriales, garantizando la seguridad y el control centralizado en entornos de alta criticidad.
- **Observabilidad Sistémica:** Implementación de estrategias de debugging y monitorización en Kubernetes (K8s) y Grafana, reduciendo el tiempo de resolución de incidencias en la infraestructura cloud.
- **Seguridad y Gobernanza:** Gestión de secretos mediante Azure Key Vault, asegurando el cumplimiento de normativas de seguridad en el manejo de activos industriales.
- **Autenticación Segura (Managed Identity + APIM):** Implementación de pipelines ADF con Managed Identity para obtención de tokens OAuth2 y consumo de APIs protegidas por Azure APIM, eliminando secretos del código.

## 📚 Proyecto destacado del curso

### [Smart-DieT - Aplicación Web de Gestión Nutricional](https://github.com/eetxlek/Smart-DieT)

**Arquitectura Hexagonal (Ports & Adapters):** Aislé el dominio del negocio de los detalles de infraestructura, facilitando el mantenimiento y la escalabilidad.
**Seguridad:** Implementé Spring Security + JWT para autenticación stateless, generando y validando tokens en cada petición.
**Persistencia:** Usé Spring Data JPA con MySQL para gestionar entidades como usuarios, productos y consumos diarios.
**Frontend:** Integré Thymeleaf y JavaScript para crear una interfaz funcional que permite gestionar despensas, registrar consumos y obtener recomendaciones personalizadas.

**¿Qué demuestra este proyecto?** Que conozco el desarrollo de aplicaciones web completas (backend + frontend), entiendo la importancia de una arquitectura limpia y sé aplicar patrones como hexagonal y DDD en un proyecto real.

## ⚙️ Stack principal

| Área | Tecnologías que uso |
| :--- | :--- |
| **Migración & Batch** | Spring Batch, Java 17, COBOL (lectura/parseo) |
| **APIs & Backend** | FastAPI, Spring Boot, Python, Java |
| **Mensajería (EDA)** | RabbitMQ, event-driven patterns |
| **Persistencia** | PostgreSQL, MongoDB, Redis, MySQL |
| **Data Integrity** | Hash chains (SHA-256), validaciones, trazabilidad con correlation IDs, idempotencia |
| **Infraestructura** | Docker, Kubernetes (K8s), Azure Key Vault, Grafana, GitHub Actions |

## 📌 Proyectos destacados

| Proyecto | Tecnologías | ¿Qué demuestra? |
| :--- | :--- | :--- |
| **[mainframe-migration-spring-batch-cobol](https://github.com/eetxlek/mainframe-migration-spring-batch-cobol)** | Spring Batch, Java 17, COBOL | Migración 1:1 de proceso legacy → moderno. Mi proyecto estrella. |
| **[industrial-telemetry-api](https://github.com/eetxlek/industrial-telemetry-api)** | FastAPI, RabbitMQ, PostgreSQL, SHA-256 | Sistema EDA con **hash chain** para integridad criptográfica (blockchain-like). |
| **[COBOL-Fixed-Width-Parser-API](https://github.com/eetxlek/COBOL-Fixed-Width-Parser-API)** | FastAPI, Pydantic | Puente bidireccional COBOL ↔ JSON + validaciones. |
| **[Smart-DieT](https://github.com/eetxlek/Smart-DieT)** | Spring Boot, JWT, MySQL, Thymeleaf | App web completa con arquitectura hexagonal y seguridad. |
| **[microservices-failure-patterns](https://github.com/eetxlek/microservices-failure-patterns)** | Python, simulación | Laboratorio de fallos reales en sistemas distribuidos (cascada, particiones). |

## 🔍 En detalle: Mis proyectos estrella

### 🚀 Migración Mainframe → Spring Batch

**Repositorio:** [mainframe-migration-spring-batch-cobol](https://github.com/eetxlek/mainframe-migration-spring-batch-cobol)

**El problema:** Un banco necesitaba migrar un proceso batch crítico (PB0EC319) escrito en COBOL y orquestado con JCL. El proceso hacía matching 1:1 entre un maestro de empleados y un fichero de subidas salariales, actualizando salarios y generando informes.

**Mi solución:**
- Migración completa a **Java 17 con Spring Batch** manteniendo la lógica original
- Optimización del matching: en lugar de lectura secuencial de ambos ficheros (O(n*m)), cargo el fichero pequeño en un `HashMap` (lookup O(1))
- Implementación de **chunk-oriented processing** (transacciones cada 10 registros) con restart automático
- Replicación exacta del informe de ejecución (contadores, tiempos, detección de inconsistencias)

**Resultado:**
- ✅ **Misma lógica funcional** (1:1 con el COBOL original)
- ✅ **10 veces más rápido** (menos I/O secuencial)
- ✅ **Testeable** (unit tests + integration tests, imposible en mainframe)
- ✅ **Más barato** (infraestructura estándar vs. MIPS)
- ✅ **Mantenible** (Java moderno vs. COBOL legacy)

**Tecnologías clave:** Spring Batch, Java 17, FlatFileItemReader/Writer, Maven, H2 (metadatos batch)

---

### 🔄 COBOL Fixed-Width Parser API

**Repositorio:** [COBOL-Fixed-Width-Parser-API](https://github.com/eetxlek/COBOL-Fixed-Width-Parser-API)

**El problema:** Los sistemas modernos necesitan consumir datos de mainframe, pero los archivos COBOL usan formatos de **longitud fija** y tipos de datos específicos (DISPLAY, COMP, COMP-3) que no son directamente legibles por APIs REST.

**Mi solución:**
- API REST con **FastAPI y Pydantic** que parsea archivos COBOL fixed-width a JSON y viceversa
- Soporte de **copybooks** con definición de layouts (posición, longitud, tipo)
- Validaciones automáticas de dominio (fechas, rangos, valores permitidos)
- Endpoints para: parseo de archivos, validación por línea, generación de muestras, consulta de layouts

**Características destacadas:**
- ✅ Soporte para **COMP (binario)** y **COMP-3 (packed decimal)** – los formatos más complejos
- ✅ Documentación interactiva automática con Swagger UI (`/docs`)
- ✅ Tests unitarios con pytest
- ✅ Extensible: puedes añadir tu propio copybook en minutos

**Caso de uso real:** Un banco necesita exponer datos de clientes desde un mainframe a una app móvil. Esta API actúa como **puente**: recibe el archivo fixed-width, lo valida, lo convierte a JSON y lo sirve vía REST.

**Tecnologías clave:** FastAPI, Pydantic, Python, Uvicorn, Swagger UI

---

### 📡 Industrial Telemetry API

**Repositorio:** [industrial-telemetry-api](https://github.com/eetxlek/industrial-telemetry-api)

**El problema:** En plantas industriales, los datos de sensores pueden ser manipulados (error o malicia), llevando a decisiones peligrosas. Además, los sistemas de monitorización necesitan datos en tiempo real.

**Mi solución:**
- API de telemetría que registra cada dato encadenándolo criptográficamente con el anterior (**hash chain con SHA-256**)
- **Arquitectura hexagonal** (DDD) separando dominio, aplicación e infraestructura
- **Event-driven**: cada nueva lectura publica un evento a RabbitMQ (desacopla consumidores como dashboards o alertas)
- Endpoint de **auditoría** que verifica la integridad de toda la cadena

**Resultado:**
- ✅ Los ingenieros pueden **demostrar matemáticamente** que los datos no han sido alterados
- ✅ Bulk insert optimizado: 10x más rápido para datos IoT
- ✅ Validaciones de dominio: temperaturas < -273°C, humedades > 100%, etc.

**Tecnologías clave:** FastAPI, RabbitMQ, PostgreSQL, SHA-256, SQLAlchemy (async), Docker

---

## 💡 Lo que me mueve

- La **integridad del dato** no es un extra: es el requisito no negociable en cualquier migración o integración.
- La **trazabilidad** (saber qué pasó, cuándo, por qué) es lo que convierte un sistema frágil en uno fiable.
- La **arquitectura limpia** no es una moda: es la diferencia entre un proyecto que se puede mantener y uno que no.

## 📫 ¿Conectamos?

Si tu equipo necesita alguien que entienda de **migración legacy → moderno**, que sepa construir **integraciones robustas con trazabilidad** y que tenga experiencia en entornos cloud (Azure, K8s) y APIs industriales, podemos hablar.
