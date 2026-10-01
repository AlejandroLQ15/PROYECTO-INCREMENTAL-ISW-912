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
