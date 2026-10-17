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

| Nombre Completo              |  Rol Principal en Scrum   |
| :--------------------------- | :-----------------------: |
| Jose Alejandro López Quesada | Scrum Master / Developer  |
| Yunior Martínez Tinoco       | Product Owner / Developer |

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

**3. Product Goal**

Desarrollar y desplegar la primera versión (MVP) de KomoYa, un marketplace web multicomercio que permita a los habitantes de Pital y zonas aledañas comparar ofertas, confirmar disponibilidad y realizar compras unificadas de múltiples comercios locales, integrando pasarelas de pago nacionales y un sistema de envío centralizado operado por el administrador.

**4. Project Charter**

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


### Sección 02: Contexto Organizacional

#### 1. Descripción del Entorno Comercial

El proyecto KomoYa surge como una iniciativa para facilitar la comercialización de productos de los negocios locales de Pital de San Carlos y zonas aledañas.

En esta zona existen diferentes establecimientos comerciales, como supermercados, pulperías, ferreterías, farmacias y otros negocios que ofrecen productos necesarios para la población.

Sin embargo, estos comercios funcionan de manera independiente, lo que obliga a los consumidores a visitar diferentes establecimientos cuando necesitan adquirir productos de distintas categorías.

KomoYa busca integrar estos negocios en una plataforma digital compartida, permitiendo que los consumidores consulten productos, comparen precios y realicen compras en diferentes comercios mediante un único proceso de compra.

#### 2. Situación Actual de los Comercios Locales

Actualmente, gran parte de las actividades comerciales de la zona se realizan mediante la atención presencial en los establecimientos.

Algunos negocios también utilizan herramientas digitales, como WhatsApp y redes sociales, para promocionar sus productos, atender consultas y recibir pedidos.

No obstante, estas herramientas no siempre permiten consultar inventarios actualizados, comparar productos entre establecimientos o gestionar compras en múltiples comercios de manera centralizada.

Esto representa una oportunidad para implementar una solución tecnológica que facilite tanto la comercialización de productos como el acceso de los consumidores a los negocios locales.

#### 3. Necesidades Identificadas

A partir del problema planteado, se identifican las siguientes necesidades:

- Facilitar el acceso a los productos ofrecidos por los comercios locales.
- Permitir que los consumidores consulten precios y disponibilidad sin desplazarse físicamente.
- Centralizar las compras de diferentes establecimientos en un único carrito.
- Reducir los tiempos que los consumidores destinan a realizar sus compras.
- Ofrecer diferentes métodos de pago electrónicos.
- Implementar un sistema de entregas centralizado.
- Brindar a los comercios una herramienta digital para administrar sus productos y pedidos.
- Mejorar la visibilidad de los pequeños y medianos comercios de la zona.

Estas necesidades constituyen una base inicial para definir las funcionalidades del sistema y deberán validarse progresivamente con los usuarios y comercios participantes.

#### 4. Factores que Influyen en el Proyecto

**Factores Tecnológicos:**

El funcionamiento de KomoYa dependerá de la disponibilidad de conexión a Internet, los servicios de alojamiento web y la integración con plataformas externas para procesar pagos y emitir comprobantes electrónicos.

**Factores Económicos:**

El proyecto debe considerar los costos relacionados con el alojamiento del sistema, el mantenimiento de la plataforma, las comisiones de las pasarelas de pago y la operación del servicio de entregas.

**Factores Operativos:**

La administración de KomoYa será responsable de coordinar las entregas de los pedidos. Por esta razón, será necesario considerar las distancias entre comercios, los tiempos de preparación y la disponibilidad del servicio de transporte.

**Factores Sociales:**

La aceptación de la plataforma dependerá de la confianza de los consumidores y comerciantes, así como de su disposición para utilizar herramientas digitales en los procesos de compra y venta.

---

### Sección 03: Mapa de Interesados y Restricciones

#### 1. Identificación de los Interesados

Los interesados son las personas, grupos u organizaciones que participan en el desarrollo del proyecto o que pueden verse afectados por sus resultados.

En el caso de KomoYa, se identifican los siguientes interesados:

| Interesado | Función o interés dentro del proyecto | Nivel de influencia |
| :--- | :--- | :---: |
| Product Owner | Definir las necesidades del producto y establecer las prioridades del Product Backlog. | Alta |
| Scrum Master / Developer | Facilitar la aplicación de Scrum y participar en el desarrollo del sistema. | Alta |
| Comercios locales | Ofrecer sus productos mediante la plataforma y gestionar los pedidos recibidos. | Alta |
| Clientes | Consultar productos, comparar precios y realizar compras mediante KomoYa. | Media |
| Administrador de KomoYa | Administrar la plataforma, supervisar los pedidos y coordinar las entregas. | Alta |
| Tilopay y PayPal | Proporcionar los servicios necesarios para procesar pagos electrónicos. | Media |
| FacturaEnCR | Proporcionar los servicios de emisión de comprobantes electrónicos. | Media |
| Proveedores de infraestructura | Proporcionar los servicios tecnológicos necesarios para el funcionamiento del sistema. | Media |

Los niveles de influencia representan una clasificación inicial y podrán ajustarse conforme avance el proyecto.

#### 2. Matriz de Poder e Interés

Para identificar la importancia de cada interesado y determinar la manera adecuada de gestionar su participación, se utilizará una matriz de poder e interés.

Esta herramienta clasifica a los interesados según su capacidad para influir en el proyecto y su nivel de interés en los resultados.

| Clasificación | Interesados | Estrategia |
| :--- | :--- | :--- |
| Alto poder / Alto interés | Product Owner, Scrum Master, administrador y comercios participantes clave. | Gestionar de cerca, involucrándolos en las decisiones y revisiones del proyecto. |
| Alto poder / Bajo interés | Proveedores externos con capacidad de afectar servicios esenciales. | Mantener satisfechos y verificar las condiciones de los servicios contratados. |
| Bajo poder / Alto interés | Clientes y usuarios potenciales. | Mantener informados y recopilar sus necesidades y opiniones. |
| Bajo poder / Bajo interés | Actores indirectos que no participan activamente en el proyecto. | Monitorear y mantener una comunicación cuando sea necesario. |

Esta clasificación permitirá establecer estrategias de comunicación y participación de acuerdo con las necesidades de cada grupo.

#### 3. Estrategia de Comunicación con los Interesados

Para mantener una comunicación adecuada durante el desarrollo de KomoYa, se establecen los siguientes mecanismos:

- **Equipo de desarrollo:** reuniones periódicas para revisar avances, identificar dificultades y organizar las actividades del Sprint.
- **Product Owner:** revisión continua del Product Backlog y definición de prioridades según las necesidades del producto.
- **Comercios participantes:** comunicación directa para recopilar requisitos, validar funcionalidades y atender observaciones.
- **Clientes:** recopilación de opiniones mediante pruebas del sistema, encuestas y comentarios sobre la experiencia de compra.
- **Proveedores externos:** consultas técnicas y seguimiento de las integraciones necesarias para el funcionamiento de la plataforma.

El equipo utilizará GitHub y GitHub Projects para registrar tareas, asignar responsables y dar seguimiento a las actividades de desarrollo.

#### 4. Restricciones del Proyecto

Durante el desarrollo de KomoYa se deberán considerar diferentes restricciones que pueden influir en su alcance, planificación y ejecución.

**Restricciones Técnicas:**

- El sistema será desarrollado utilizando tecnologías como Laravel, PHP, JavaScript y PostgreSQL.
- La plataforma dependerá de servicios externos para procesar pagos y emitir comprobantes electrónicos.
- Será necesario contar con una infraestructura web segura y compatible con HTTPS.
- El sistema deberá contar con mecanismos de autenticación y autorización para proteger la información de los usuarios.

**Restricciones Económicas:**

- El proyecto deberá desarrollarse considerando un presupuesto limitado.
- Se deberán evaluar los costos de alojamiento, dominio, servicios externos y mantenimiento.
- Las comisiones de las pasarelas de pago pueden influir en la rentabilidad de las operaciones.

**Restricciones Operativas:**

- Durante la primera versión, el servicio de entregas será administrado exclusivamente por KomoYa.
- La disponibilidad de los productos dependerá de la información proporcionada por cada comercio.
- La cobertura del servicio estará limitada a las zonas establecidas por la administración.
- Los tiempos de entrega dependerán de la ubicación de los establecimientos y de la disponibilidad del servicio logístico.

**Restricciones de Tiempo:**

- El desarrollo académico se realizará durante el III Cuatrimestre de 2026.
- Las funcionalidades serán organizadas y desarrolladas mediante Sprints.
- Se dará prioridad a las funcionalidades necesarias para disponer de una primera versión funcional del sistema.

#### 5. Riesgos Iniciales del Proyecto

Se identifican los siguientes riesgos que podrían afectar el desarrollo o funcionamiento de KomoYa:

| ID | Riesgo | Impacto estimado | Medida preventiva |
| :---: | :--- | :---: | :--- |
| R01 | Dificultades en la integración con las pasarelas de pago. | Alto | Realizar pruebas de integración en entornos de prueba antes de habilitar pagos reales. |
| R02 | Fallos o interrupciones de los servicios externos. | Alto | Implementar registros de errores y mecanismos de recuperación. |
| R03 | Información desactualizada del inventario de los comercios. | Alto | Validar la disponibilidad de los productos antes de confirmar las compras. |
| R04 | Retrasos en el desarrollo de funcionalidades. | Medio | Priorizar las funcionalidades esenciales y realizar seguimiento mediante Sprints. |
| R05 | Baja participación de comercios locales. | Alto | Establecer comunicación con comercios interesados y validar sus necesidades. |
| R06 | Dificultades en la coordinación de entregas. | Medio | Definir zonas de cobertura, tarifas y procedimientos de entrega. |
| R07 | Problemas de seguridad o acceso no autorizado. | Alto | Implementar autenticación, autorización y validaciones de seguridad. |

Los riesgos identificados serán revisados durante el desarrollo del proyecto para determinar si requieren nuevas acciones preventivas o correctivas.

### Sección 04: Ciclo de vida del proyecto y primer Sprint

#### 1. Mapa del Ciclo de Vida del Proyecto

- **Enfoque del Ciclo de Vida (Híbrido):** Se utilizará un enfoque híbrido. Emplearemos una **fase predictiva** al inicio para definir la arquitectura base del sistema (bases de datos y seguridad), ya que son elementos predecibles. Paralelamente, utilizaremos un **enfoque adaptativo** durante la ejecución para integrar módulos que requieren validación constante (pasarelas de pago y logística de envíos).
- **Fases del Proyecto:**
  1.  **Inicio:** Definición del problema, conceptualización del MVP, selección de comercios locales e inicio del _Project Charter_.
  2.  **Planificación:** Diseño de la arquitectura, estructuración de la base de datos y creación del _Product Backlog_ inicial.
  3.  **Ejecución (Iterativa):** Desarrollo del software mediante Sprints. Construcción del entorno, seguridad, catálogo, carrito de compras y pasarela de pago.
  4.  **Monitoreo y Control:** Pruebas de integración, validación de dependencias externas y ajustes continuos en las _Sprint Reviews_.
  5.  **Cierre:** Despliegue en producción, demostración (Demo) y entrega del Expediente del Proyecto.

---

#### 2. Planificación del Primer Sprint

- **Duración del Sprint:** 2 semanas.
- **Sprint Goal:** Establecer los cimientos técnicos de la plataforma configurando el entorno de desarrollo y construyendo los módulos fundamentales de autenticación (Login), seguridad de rutas y navegación básica (Dashboard).

**Sprint Backlog:**

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
