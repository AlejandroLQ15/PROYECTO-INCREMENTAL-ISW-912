<div align="center">

# UNIVERSIDAD TÉCNICA NACIONAL

### Sede Regional San Carlos

**Bachillerato en Ingeniería en Software**

<br><br>

**Curso:**
ISW-912 Proyecto Incremental

**Docente:**
Rudy Barboza

<br><br><br>

# EXPEDIENTE DEL PROYECTO

## KomoYa – Marketplace Multicomercio

<br><br>

**Organización / Cliente:**
Comunidad y Comercios Locales de Pital y zonas aledañas

<br><br><br>

**Scrum Team:**

| Nombre Completo              | Identificación / Carné |  Rol Principal en Scrum   |
| :--------------------------- | :--------------------: | :-----------------------: |
| Jose Alejandro López Quesada |       208360921        | Scrum Master / Developer  |
| Yunior Martínez Tinoco       |       208550120        | Product Owner / Developer |

<br><br><br>

**Ciudad Quesada, San Carlos, Alajuela**
**III Cuatrimestre, 2026**

</div>

<div style="page-break-after: always;"></div>

### Sección 01: Problema, oportunidad y Product Goal

**1. Definición del Problema Real**

En la zona de Pital y sus alrededores, los consumidores se enfrentan a un proceso de compra fragmentado cuando necesitan adquirir productos de diferentes rubros (como abarrotes, ferretería o farmacia). Actualmente, para comparar precios y verificar existencias, el cliente debe visitar físicamente múltiples comercios o contactarlos uno por uno. Además, si decide comprar en varios lugares, debe coordinar y pagar múltiples servicios de entrega (express), lo que incrementa los costos logísticos y el tiempo de espera, desincentivando la compra en los comercios locales.

**2. La Oportunidad**

Existe la oportunidad de digitalizar y unificar el ecosistema comercial de la zona mediante una plataforma centralizada (KomoYa). Esto permitirá a los comercios locales exponer su inventario en un canal digital compartido, y a los usuarios consolidar sus compras de diferentes tiendas en un único carrito, gestionando un solo pago y recibiendo todos sus productos mediante una entrega unificada operada por la administración.

**3. Product Goal (Objetivo del Producto)**

Desarrollar y desplegar la primera versión (MVP) de KomoYa, un marketplace web multicomercio que permita a los habitantes de Pital y zonas aledañas comparar ofertas, confirmar disponibilidad y realizar compras unificadas de múltiples comercios locales, integrando pasarelas de pago nacionales y un sistema de envío centralizado operado por el administrador.

**4. Project Charter (Borrador Inicial)**

- **Descripción del Proyecto:** Construcción de una plataforma web bajo arquitectura MVC (Laravel/PHP, Node.js, PostgreSQL) que operará como un marketplace para comercios locales. En esta primera versión, la administración del sistema absorberá el rol de operador logístico exclusivo.
- **Alcance Inicial (MVP):**
  - Módulo de roles diferenciados: Administrador (operador), Cliente y Comercios (supermercado, ferretería, farmacia).
  - Gestión de carrito multicomercio con validación de existencias previas al pago.
  - Integración de pagos en colones (Tilopay) y alternativa internacional (PayPal).
  - Integración con FacturaEnCR para la emisión de tiquetes/facturas electrónicas de los servicios de envío.
  - Cálculo automatizado de distancias y tarifas de envío usando OSRM y geocodificación (Tarifa base: ₡350/km, mínimo ₡1.000, radio máximo 50 km).
  - Sincronización automatizada del tipo de cambio del BCCR (indicador 318).
- **Restricciones de Alto Nivel:**
  - El sistema de envíos en esta versión es centralizado; los comercios no gestionarán sus propias entregas.
  - Se requiere conexión constante a servicios de fondo (colas y _scheduler_) para procesar vencimientos de reservas (15 min), notificaciones transaccionales y comprobantes fiscales.
  - La plataforma debe estar desplegada en un entorno con soporte HTTPS estricto para el correcto funcionamiento de los webhooks de pago (Tilopay/PayPal).

### Sección 04: Ciclo de vida del proyecto y primer Sprint

#### 1. Mapa del Ciclo de Vida del Proyecto

- **Enfoque del Ciclo de Vida (Híbrido):** Se utilizará un enfoque híbrido. Emplearemos una **fase predictiva** al inicio para definir la arquitectura base del sistema (bases de datos y seguridad), ya que son elementos predecibles. Paralelamente, utilizaremos un **enfoque adaptativo (ágil con Scrum)** durante la ejecución para integrar módulos que requieren validación constante (pasarelas de pago y logística de envíos).
- **Fases del Proyecto:**
  1.  **Inicio:** Definición del problema, conceptualización del MVP, selección de comercios locales e inicio del _Project Charter_.
  2.  **Planificación:** Diseño de la arquitectura, estructuración de la base de datos y creación del _Product Backlog_ inicial.
  3.  **Ejecución (Iterativa):** Desarrollo del software mediante Sprints. Construcción del entorno, seguridad, catálogo, carrito de compras y pasarela de pago.
  4.  **Monitoreo y Control:** Pruebas de integración, validación de dependencias externas y ajustes continuos en las _Sprint Reviews_.
  5.  **Cierre:** Despliegue en producción, demostración (Demo) y entrega del Expediente del Proyecto.

---

#### 2. Planificación del Primer Sprint

- **Duración del Sprint:** 2 semanas.
- **Sprint Goal (Objetivo del Sprint):** Establecer los cimientos técnicos de la plataforma configurando el entorno de desarrollo y construyendo los módulos fundamentales de autenticación (Login), seguridad de rutas y navegación básica (Dashboard).

**Sprint Backlog (Historias y tareas que se atacarán primero):**

|   ID   | Tarea / Historia a desarrollar                          | Prioridad |
| :----: | :------------------------------------------------------ | :-------: |
| **1**  | Configurar el entorno de desarrollo del proyecto.       |   Alta    |
| **3**  | Crear la interfaz gráfica del Login.                    |   Alta    |
| **4**  | Implementar la validación de credenciales.              |   Alta    |
| **5**  | Implementar el manejo de sesiones.                      |   Alta    |
| **6**  | Desarrollar la funcionalidad de cerrar sesión (Logout). |   Alta    |
| **7**  | Diseñar la interfaz gráfica del Dashboard.              |   Alta    |
| **9**  | Proteger las rutas para usuarios autenticados.          |   Alta    |
| **8**  | Implementar la navegación principal del Dashboard.      |   Media   |
| **10** | Mostrar información básica del usuario en el Dashboard. |   Media   |

- **Justificación de selección:** Se eligió atacar estas historias primero porque representan la base técnica indispensable del sistema. No se puede avanzar a la programación de módulos de ventas o perfiles de comercio sin antes tener un entorno funcional y un sistema de autenticación seguro y probado que controle los accesos al Dashboard.
