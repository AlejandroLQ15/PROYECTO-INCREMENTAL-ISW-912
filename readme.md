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

### Sección 00: Portada e identificación del equipo

## KomoYa – Marketplace Multicomercio

Ciudad Quesada, San Carlos, Alajuela / III Cuatrimestre, 2026
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

</div>

<div style="page-break-after: always;"></div>

### Sección 01: Problema, oportunidad y Product Goal

#### 1. Problema

En Pital y sus alrededores, adquirir productos de distintos comercios representa un desafío para los consumidores, ya que, en muchas ocasiones, deben desplazarse largas distancias para consultar precios, verificar la disponibilidad de productos y realizar sus compras en diferentes establecimientos. Esta situación se agrava debido a la limitada disponibilidad y frecuencia de los servicios de transporte en algunas comunidades, lo que dificulta aún más el acceso a productos de primera necesidad y otros artículos para el hogar, generando mayores gastos de traslado, inversión de tiempo e inconvenientes para los habitantes de la zona.

#### 2. Oportunidad

Con Komo-Ya buscamos reunir los precios, existencias y ofertas de los comercios locales en una plataforma donde los clientes puedan comparar productos, realizar una compra multicomercio y recibir una entrega consolidada.

#### 3. Product Goal

Desarrollar una primera versión web de Komo-Ya que permita consultar productos, reunir ofertas de varios comercios en un carrito, aprobar el total confirmado, realizar un pago unificado y consultar el estado de la entrega.

#### 4. Descripción del proyecto

Desarrollaremos un marketplace para clientes y comercios de Pital y zonas aledañas. Contaremos con tres roles principales: administrador, cliente y comercio. El administrador coordinará las compras y las entregas, y recibirá el pago completo del pedido.

### Sección 02: Contexto organizacional y restricciones

#### 1. Contexto

Los comercios locales atienden principalmente de forma presencial y mediante canales como WhatsApp y redes sociales. Con KomoYa buscamos facilitar su acceso a un canal compartido de ventas y reducir la coordinación que requiere una compra en varios negocios.

Organizaremos los productos en un catálogo central administrado por la plataforma. Cada comercio vinculará sus ofertas con ese catálogo y gestionará sus precios, existencias y disponibilidad.

#### 2. Restricciones

- Utilizaremos Laravel, PHP y PostgreSQL, con Blade, Tailwind CSS y Alpine.js para la interfaz.
- Usaremos Node.js y Vite para compilar los recursos de la interfaz.
- Integraremos SINPE Móvil, Tilopay y PayPal como medios de pago.
- La administración coordinará las entregas; los comercios no tendrán repartidores dentro de esta versión.
- La cobertura inicial será de hasta 50 km desde el punto de operación en Pital.
- El costo de envío considerará distancia, comercios, cantidad de productos y peso.
- Protegeremos los comprobantes y documentos mediante acceso autorizado.
- Necesitaremos alojamiento con HTTPS, almacenamiento, colas y tareas programadas.
- Disponemos de aproximadamente 2 horas semanales por integrante, para un total de 4 horas de equipo por semana.

### Sección 03: Interesados / stakeholders

| Interesado                                     | Interés o responsabilidad                             | Influencia | Comunicación                          |
| :--------------------------------------------- | :---------------------------------------------------- | :--------- | :------------------------------------ |
| Yunior Martínez, Product Owner / Developer     | Priorizar necesidades y revisar el alcance            | Alta       | Revisión del backlog y de cada Sprint |
| Jose Alejandro López, Scrum Master / Developer | Organizar el trabajo y dar seguimiento a impedimentos | Alta       | Seguimiento del equipo                |
| Administrador de KomoYa                        | Coordinar pedidos, pagos y entregas                   | Alta       | Revisión del flujo operativo          |
| Comercios y colaboradores                      | Publicar ofertas y confirmar pedidos                  | Alta       | Demostraciones y consultas            |
| Clientes                                       | Comprar y conocer el estado de sus pedidos            | Media      | Pruebas de uso y comentarios          |
| Docente                                        | Evaluar el expediente del proyecto                    | Alta       | Entregas académicas                   |
| Proveedores de servicios                       | Facilitar pagos, alojamiento y otras integraciones    | Alta       | Consultas técnicas y de contratación  |

Mantendremos una comunicación cercana con los interesados de mayor influencia y recogeremos comentarios de clientes y comercios para ajustar las prioridades.

### Sección 04: Ciclo de vida del proyecto y primer Sprint

#### 1. Ciclo de vida

Trabajaremos de forma incremental con Sprints de dos semanas. Iniciaremos con la definición del alcance y la arquitectura, después construiremos las funcionalidades por prioridad. Al finalizar cada Sprint revisaremos el incremento, las dificultades y los ajustes del backlog.

Organizaremos el proyecto en inicio, planificación, ejecución, seguimiento y cierre.

#### 2. Primer Sprint

- **Inicio de planificación:** 30/09/2026
- **Duración:** dos semanas, del 30/09/2026 al 13/10/2026.
- **Sprint Goal:** establecer el acceso a la plataforma y los permisos de sus usuarios.
- **Historias:** HU-01a y HU-01b, con un total estimado de 5 puntos.
- **Capacidad:** 8 horas de equipo por Sprint.

### Sección 05: Backlog inicial y Sprint Backlog

#### 1. Backlog inicial

| ID    | Historia de usuario / necesidad                                                                      | Prioridad |
| :---- | :--------------------------------------------------------------------------------------------------- | :-------- |
| HU-01 | Como administrador, quiero gestionar accesos y roles para proteger el sistema.                       | Alta      |
| HU-02 | Como comercio, quiero gestionar mis ofertas e inventario para mantenerlos actualizados.              | Alta      |
| HU-03 | Como cliente, quiero consultar productos y disponibilidad para comparar opciones.                    | Alta      |
| HU-04 | Como cliente, quiero reunir productos de distintos comercios en un carrito para realizar una compra. | Alta      |
| HU-05 | Como cliente, quiero realizar un pago unificado para completar mi pedido.                            | Alta      |
| HU-06 | Como cliente, quiero conocer el costo del envío antes de aprobar mi compra.                          | Alta      |
| HU-07 | Como cliente, quiero recibir avisos y comprobantes de mi pedido.                                     | Media     |
| HU-08 | Como cliente, quiero consultar el historial y estado de mis pedidos.                                 | Media     |

#### 2. Sprint Backlog 1

| Tarea     | Historia       | Actividad                                           | Responsable    | Horas |
| :-------- | :------------- | :-------------------------------------------------- | :------------- | ----: |
| S1-T01    | HU-01a         | Configurar entorno y usuarios de prueba             | Ambos          |     1 |
| S1-T02    | HU-01a         | Implementar acceso, salida y recuperación de cuenta | Yunior         |     2 |
| S1-T03    | HU-01b         | Implementar permisos y navegación por rol           | Jose Alejandro |     2 |
| S1-T04    | HU-01a, HU-01b | Revisar acceso y permisos                           | Ambos          |   1,5 |
| S1-T05    | HU-01a, HU-01b | Planificar, revisar y actualizar documentación      | Ambos          |   1,5 |
| **Total** |                |                                                     |                | **8** |

Seleccionamos estas historias porque el acceso y los permisos son necesarios para desarrollar los módulos de clientes, comercios y administración.

#### 3. Seguimiento

Utilizaremos GitHub Projects para organizar tareas en Backlog, Por hacer, En progreso, En revisión y Terminado. Relacionaremos cada tarea y commit con su historia y revisaremos los avances al finalizar cada Sprint.

### Sección 06: Alcance, Product Backlog priorizado y criterios de aceptación

#### 1. Alcance

Incluiremos acceso y roles, catálogo central, ofertas por comercio, búsqueda, carrito multicomercio, confirmación de existencias, aprobación del pedido, cálculo de envío, pagos, seguimiento y comprobantes.

Dejaremos fuera de esta primera versión las aplicaciones móviles nativas, el seguimiento GPS en tiempo real, la distribución automática de fondos y la gestión de entregas independientes por comercio.

#### 2. Product Backlog priorizado

Dividimos las historias iniciales en funcionalidades más pequeñas. Conservamos su ID principal y utilizamos letras para identificar cada división. Presentamos el orden, los puntos, las prioridades y las dependencias en la matriz de la sección 07.

#### 3. Criterios de aceptación

| ID     | Criterios de aceptación                                                                                                |
| :----- | :--------------------------------------------------------------------------------------------------------------------- |
| HU-01a | El usuario puede ingresar, cerrar sesión y recuperar su cuenta; rechazamos credenciales incorrectas.                   |
| HU-01b | Cada rol accede únicamente a sus funciones; un comercio no modifica información de otro.                               |
| HU-02a | La administración publica los productos centrales y revisa las sugerencias antes de aprobarlas.                        |
| HU-02b | Cada comercio administra sus ofertas, precios y existencias sin alterar el catálogo central ni ofertas ajenas.         |
| HU-03  | La búsqueda muestra productos, comercios y precios disponibles.                                                        |
| HU-04a | El carrito admite varios comercios y actualiza los subtotales al cambiar cantidades.                                   |
| HU-04b | Cada comercio confirma cantidades y precios; reservamos las cantidades confirmadas y excluimos los productos agotados. |
| HU-04c | El cliente aprueba el total antes del pago; al vencer los 15 minutos de aprobación liberamos las reservas.             |
| HU-08a | Registramos quién modifica el estado del pedido, cuándo lo hace y el motivo.                                           |
| HU-06a | Calculamos cobertura y recorrido considerando origen, comercios y cliente.                                             |
| HU-06b | El envío incorpora distancia y recargos; las cargas especiales requieren cotización manual antes de aprobar y pagar.   |
| HU-05a | El comprobante SINPE queda pendiente hasta verificar el movimiento bancario y su monto.                                |
| HU-07a | Cada participante recibe los avisos correspondientes a su pedido.                                                      |
| HU-05b | Confirmamos el pago Tilopay mediante una respuesta validada del proveedor y evitamos registros duplicados.             |
| HU-05d | Guardamos la tasa CRC/USD utilizada y contamos con una tasa de respaldo.                                               |
| HU-05c | PayPal cobra el monto aprobado en USD y confirmamos la captura antes de marcar el pedido como pagado.                  |
| HU-08b | Las compras comienzan después del pago y podemos registrar la programación y el avance de la entrega.                  |
| HU-08c | El cliente consulta únicamente sus pedidos y su historial.                                                             |
| HU-07b | El cliente recibe un resumen y accede de forma autorizada a los comprobantes.                                          |
| HU-07c | El cliente elige factura o tiquete; conservamos sus datos fiscales y el estado de emisión del proveedor.               |

### Sección 07: Planificación temporal, estimaciones y costos

#### 1. Estimación de historias

Utilizaremos planning poker con la escala **1, 2, 3, 5, 8, 13 y 21**. Compararemos complejidad, esfuerzo e incertidumbre de cada historia y discutiremos las diferencias antes de asignar sus puntos.

Tomamos **HU-05a: pago SINPE verificado**, de **3 puntos**, como historia de referencia. Incluye adjuntar un comprobante, mantener el pago pendiente y permitir su verificación o rechazo.

La siguiente matriz recoge nuestra estimación inicial para revisar mediante planning poker.

#### 2. Matriz de Estimación

| Orden | ID        | Historia resumida                     | Épica      | Puntos | Prioridad | Dependencias   | Sprint |
| ----: | :-------- | :------------------------------------ | :--------- | -----: | :-------- | :------------- | -----: |
|     1 | HU-01a    | Acceso, salida y recuperación         | Seguridad  |      3 | Alta      | —              |      1 |
|     2 | HU-01b    | Roles y permisos                      | Seguridad  |      2 | Alta      | HU-01a         |      1 |
|     3 | HU-02a    | Catálogo central y moderación         | Catálogo   |      5 | Alta      | HU-01b         |      2 |
|     4 | HU-02b    | Ofertas e inventario por comercio     | Catálogo   |      5 | Alta      | HU-02a         |      3 |
|     5 | HU-03     | Búsqueda y consulta de ofertas        | Compra     |      3 | Alta      | HU-02b         |      4 |
|     6 | HU-04a    | Carrito multicomercio                 | Compra     |      2 | Alta      | HU-03          |      4 |
|     7 | HU-04b    | Subórdenes, confirmación y reservas   | Compra     |      5 | Alta      | HU-04a         |      5 |
|     8 | HU-04c    | Aprobación y vencimientos             | Compra     |      3 | Alta      | HU-04b         |      6 |
|     9 | HU-08a    | Auditoría e intervención del operador | Operación  |      2 | Alta      | HU-04b         |      6 |
|    10 | HU-06a    | Cobertura y ruta con paradas          | Logística  |      3 | Alta      | HU-04c         |      7 |
|    11 | HU-06b    | Recargos y cotización manual          | Logística  |      2 | Alta      | HU-06a         |      7 |
|    12 | HU-05a    | Pago SINPE verificado                 | Pagos      |      3 | Alta      | HU-04c, HU-06b |      8 |
|    13 | HU-07a    | Notificaciones                        | Documentos |      2 | Media     | HU-08a         |      8 |
|    14 | HU-05b    | Pago Tilopay en CRC                   | Pagos      |      5 | Alta      | HU-05a         |      9 |
|    15 | HU-05d    | Conversión CRC/USD                    | Pagos      |      2 | Alta      | HU-04c         |     10 |
|    16 | HU-05c    | Pago PayPal en USD                    | Pagos      |      3 | Alta      | HU-05d         |     10 |
|    17 | HU-08b    | Compras, entrega y programación       | Operación  |      3 | Alta      | HU-05a, HU-08a |     11 |
|    18 | HU-08c    | Historial de pedidos del cliente      | Operación  |      2 | Media     | HU-08b         |     11 |
|    19 | HU-07b    | Resumen y comprobantes privados       | Documentos |      3 | Media     | HU-08b         |     12 |
|    20 | HU-07c    | Conexión fiscal configurable          | Documentos |      2 | Media     | HU-07b         |     12 |
|       | **Total** | **20 historias hoja**                 |            | **60** |           |                |        |

| Épica      | Total de puntos |
| :--------- | --------------: |
| Seguridad  |               5 |
| Catálogo   |              10 |
| Compra     |              13 |
| Logística  |               5 |
| Pagos      |              13 |
| Operación  |               7 |
| Documentos |               7 |
| **Total**  |          **60** |

#### 3. Historias que requieren división

| Historia inicial              | Puntos de sus divisiones | Tratamiento                                           |
| :---------------------------- | -----------------------: | :---------------------------------------------------- |
| HU-02: productos y ofertas    |                       10 | Dividimos en catálogo central y ofertas por comercio. |
| HU-04: carrito y confirmación |                       10 | Dividimos en carrito, confirmación y aprobación.      |
| HU-05: pagos                  |                       13 | Dividimos en SINPE, Tilopay, conversión y PayPal.     |

Las historias de más de 8 puntos quedan divididas en la matriz. Contabilizamos únicamente sus divisiones para obtener los 60 puntos del backlog.

#### 4. Supuestos y riesgos de la estimación

- Estimamos con una disponibilidad de 2 horas semanales por integrante.
- Consideramos el uso de librerías y componentes estándar para autenticación, pagos y documentos.
- Las integraciones dependen de contar con acceso a los servicios y ambientes de prueba.
- La facturación, la confirmación de inventario y los pagos pueden requerir más trabajo del previsto.
- Revisaremos las estimaciones cuando cambien los requisitos o identifiquemos nuevas dificultades.

#### 5. Velocidad inicial

Para nuestra planificación utilizamos una velocidad inicial de **5 puntos por Sprint**, con un rango de **3 a 8 puntos**. Cada Sprint durará dos semanas y contará con 8 horas de equipo.

Actualizaremos la velocidad con los puntos de historias terminadas y aceptadas. Después de tres Sprints utilizaremos el promedio de los últimos tres para ajustar las fechas y la distribución del trabajo.

#### 6. Sprints necesarios

| Escenario       | Velocidad | Sprints necesarios | Duración   | Final estimado |
| :-------------- | --------: | -----------------: | :--------- | :------------- |
| Mayor velocidad |  8 puntos |                  8 | 16 semanas | 19/01/2027     |
| Base            |  5 puntos |                 12 | 24 semanas | 16/03/2027     |
| Menor velocidad |  3 puntos |                 20 | 40 semanas | 06/07/2027     |

Proyectamos entre **8 y 20 Sprints**, con un escenario base de **12 Sprints** para completar los 60 puntos. Ajustaremos la distribución de las historias según la velocidad y sus dependencias.

#### 7. Cronograma de Entregas / Release Plan

| Sprint | Inicio     | Fin / demo | Historias      | Puntos | Incremento                                  |
| -----: | :--------- | :--------- | :------------- | -----: | :------------------------------------------ |
|      1 | 30/09/2026 | 13/10/2026 | HU-01a, HU-01b |      5 | Acceso y permisos por rol                   |
|      2 | 14/10/2026 | 27/10/2026 | HU-02a         |      5 | Catálogo central moderado                   |
|      3 | 28/10/2026 | 10/11/2026 | HU-02b         |      5 | Ofertas e inventario por comercio           |
|      4 | 11/11/2026 | 24/11/2026 | HU-03, HU-04a  |      5 | Consulta pública y carrito multicomercio    |
|      5 | 25/11/2026 | 08/12/2026 | HU-04b         |      5 | Subórdenes, confirmación parcial y reservas |
|      6 | 09/12/2026 | 22/12/2026 | HU-04c, HU-08a |      5 | Aprobación, plazos y auditoría              |
|      7 | 23/12/2026 | 05/01/2027 | HU-06a, HU-06b |      5 | Ruta, cobertura y tarifa logística          |
|      8 | 06/01/2027 | 19/01/2027 | HU-05a, HU-07a |      5 | SINPE y notificaciones                      |
|      9 | 20/01/2027 | 02/02/2027 | HU-05b         |      5 | Pago en CRC con Tilopay                     |
|     10 | 03/02/2027 | 16/02/2027 | HU-05d, HU-05c |      5 | Conversión y pago PayPal                    |
|     11 | 17/02/2027 | 02/03/2027 | HU-08b, HU-08c |      5 | Compra, entrega programada e historial      |
|     12 | 03/03/2027 | 16/03/2027 | HU-07b, HU-07c |      5 | Resumen, comprobantes y conexión fiscal     |

Al finalizar cada Sprint realizaremos una revisión con el Product Owner. Consideramos trabajo continuo desde el 30 de septiembre; cualquier pausa modificará las fechas del cronograma.

| Hito                           | Fecha      | Entrega a revisar                    |
| :----------------------------- | :--------- | :----------------------------------- |
| Revisión con comercios         | 10/11/2026 | Catálogo y ofertas                   |
| Demostración del carrito       | 24/11/2026 | Compra multicomercio                 |
| Revisión del pedido confirmado | 22/12/2026 | Confirmación, aprobación y auditoría |
| Demostración de pago local     | 19/01/2027 | SINPE y notificaciones               |
| Revisión del release           | 16/03/2027 | Flujo completo y comprobantes        |

#### 8. Costos estimados

Para estimar el costo utilizamos un valor de **₡5.000 por hora de trabajo** y un presupuesto de **₡10.000 por Sprint** para alojamiento, almacenamiento, correo y dominio. Reservamos un 10% para imprevistos.

| Concepto                    |  Por Sprint |
| :-------------------------- | ----------: |
| Trabajo del equipo: 8 horas |     ₡40.000 |
| Infraestructura y servicios |     ₡10.000 |
| Subtotal                    |     ₡50.000 |
| Reserva para imprevistos    |      ₡5.000 |
| **Total**                   | **₡55.000** |

| Escenario                      | Costo estimado total |
| :----------------------------- | -------------------: |
| 8 Sprints                      |             ₡440.000 |
| **12 Sprints, escenario base** |         **₡660.000** |
| 20 Sprints                     |           ₡1.100.000 |

#### 9. Seguimiento del release

Utilizaremos un burndown para revisar los puntos pendientes al finalizar cada Sprint. Compararemos el avance con los 60 puntos iniciales y actualizaremos el cronograma cuando cambie el alcance o la velocidad.

### Sección 08: Riesgos y adquisiciones

#### 1. Matriz de riesgos

| ID  | Riesgo                                              | Probabilidad | Impacto | Acción                                                                        | Responsable    |
| :-- | :-------------------------------------------------- | :----------- | :------ | :---------------------------------------------------------------------------- | :------------- |
| R01 | Retrasos al integrar las pasarelas de pago          | Alta         | Alto    | Solicitar accesos con anticipación y realizar pruebas por separado.           | Yunior         |
| R02 | Interrupciones de servicios externos                | Media        | Alto    | Contar con respaldo para el tipo de cambio y revisión manual de cotizaciones. | Jose Alejandro |
| R03 | Diferencias entre inventario publicado y disponible | Alta         | Alto    | Confirmar cantidades con el comercio y reservar existencias.                  | Ambos          |
| R04 | Trabajo mayor a la capacidad disponible             | Alta         | Alto    | Dividir historias y ajustar alcance y fechas.                                 | Jose Alejandro |
| R05 | Poca participación de comercios o clientes          | Media        | Medio   | Coordinar revisiones y recoger observaciones durante las demostraciones.      | Yunior         |
| R06 | Errores en la tarifa de entrega                     | Media        | Alto    | Probar límites y recargos; revisar cargas especiales antes del pago.          | Jose Alejandro |
| R07 | Acceso no autorizado a información                  | Media        | Alto    | Proteger rutas y archivos y comprobar permisos por rol.                       | Ambos          |
| R08 | Dificultades en facturación electrónica             | Alta         | Alto    | Validar datos e integración con el proveedor antes de habilitar la emisión.   | Yunior         |
| R09 | Fallos en procesos programados                      | Media        | Alto    | Revisar colas, vencimientos y reintentos.                                     | Jose Alejandro |
| R10 | Registros duplicados de pagos                       | Media        | Alto    | Validar referencias y probar notificaciones repetidas.                        | Ambos          |

Revisaremos los riesgos al finalizar cada Sprint y registraremos las acciones necesarias para reducir su efecto en el proyecto.

#### 2. Adquisiciones y servicios

| Recurso                                  | Necesidad                         | Criterio de selección                                         | Momento de gestión          | Responsable    |
| :--------------------------------------- | :-------------------------------- | :------------------------------------------------------------ | :-------------------------- | :------------- |
| Alojamiento, PostgreSQL y almacenamiento | Publicar y mantener la plataforma | Compatibilidad con Laravel, HTTPS, respaldo y costo           | Sprint 1                    | Jose Alejandro |
| Dominio y correo                         | Acceso público y notificaciones   | Disponibilidad, entrega de mensajes y costo                   | Sprint 1                    | Yunior         |
| Rutas y geocodificación                  | Calcular cobertura y recorrido    | Cobertura de la zona, disponibilidad y límites de uso         | Antes del Sprint 7          | Jose Alejandro |
| SINPE Móvil                              | Recibir y verificar pagos locales | Cuenta operativa y procedimiento de verificación              | Antes del Sprint 8          | Yunior         |
| Tilopay y PayPal                         | Procesar pagos electrónicos       | Compatibilidad, ambiente de pruebas y condiciones comerciales | Antes de los Sprints 9 y 10 | Yunior         |
| FacturaEnCR                              | Emitir comprobantes electrónicos  | Integración, datos fiscales y costo del servicio              | Antes del Sprint 12         | Yunior         |

Compararemos las opciones antes de contratar. Incluimos los servicios de apoyo en el presupuesto de infraestructura y revisaremos cualquier cargo adicional de las integraciones antes de adquirirlas.

### Sección 09: Calidad y Definition of Done

#### 1. Criterios de calidad

Para asegurar el correcto funcionamiento de KomoYa, establecemos los siguientes estándares técnicos durante el desarrollo:

- **Validación y control de acceso:** Validaremos todos los formularios en el servidor y verificaremos los permisos por rol (administrador, cliente y comercio) en cada ruta y acción para evitar accesos no autorizados.
- **Prevención de pagos duplicados:** Validaremos las referencias de transacción y las respuestas de los proveedores de pago antes de confirmar una orden, evitando cobros o registros repetidos.
- **Manejo de errores en integraciones:** Implementaremos registros de errores, reintentos en cola y mecanismos de respaldo (como la tasa manual CRC/USD y la cotización manual de envíos) ante fallos de servicios externos.
- **Rendimiento y estándar de código:** Mantendremos el código limpio bajo las convenciones de Laravel, ejecutaremos notificaciones y documentos en segundo plano mediante colas y verificaremos tiempos de respuesta fluidos en las consultas principales.

#### 2. Definition of Done (DoD)

Para considerar una historia de usuario como terminada al finalizar un Sprint, deberá cumplir con los siguientes puntos:

- [ ] Cumple con todos los criterios de aceptación definidos en la sección 06.
- [ ] El código fue probado localmente sin errores de ejecución ni de compilación (`npm run build`).
- [ ] Las pruebas automatizadas (`php artisan test`) y la revisión de formato (`pint --test`) pasan correctamente.
- [ ] Los cambios fueron subidos a GitHub vinculados al ID de la historia y revisados entre ambos integrantes del equipo.
- [ ] La historia fue revisada con el Product Owner, movida a _Terminado_ en GitHub Projects y documentada en el expediente si aplica.

#### 3. Estrategia de validación

Antes de cerrar cada módulo, comprobaremos su funcionamiento mediante las siguientes pruebas:

| Módulo / Flujo               | Método de validación                                                                                                                                              |
| :--------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Seguridad y roles**        | Pruebas funcionales intentando acceder o alterar datos entre cuentas de administrador, comercio y cliente.                                                        |
| **Inventario y reservas**    | Pruebas de compra simultánea y ejecución del _scheduler_ para confirmar que las reservas vencidas a los 15 minutos liberan las existencias.                       |
| **Cálculo de rutas y envío** | Verificación de distancias con OSRM, cálculo de tarifas y recargos, bloqueo fuera del radio de 50 km y flujo de cotización manual.                                |
| **Pagos y moneda**           | Simulación en ambiente de pruebas de _webhooks_ de Tilopay y PayPal (incluyendo envíos duplicados), verificación de comprobantes SINPE y uso de tasa de respaldo. |
| **Avisos y comprobantes**    | Ejecución del _queue worker_ para confirmar el envío de notificaciones por correo, acceso privado a documentos y respuesta del proveedor fiscal.                  |

### Sección 10: Comunicación y responsabilidades del equipo

#### 1. Matriz de responsabilidades

Para distribuir el trabajo de forma clara entre los dos integrantes del equipo, aplicamos una matriz RACI (_R: Responsable de ejecutar, **A: Aprueba / rinde cuentas, **C_: Consultado / apoya en revisión):

| Área / Actividad del proyecto                               | Jose Alejandro (Scrum Master / Dev) | Yunior (Product Owner / Dev) |
| :---------------------------------------------------------- | :---------------------------------: | :--------------------------: |
| Gestión y priorización del Product Backlog                  |                  C                  |            R / A             |
| Facilitación Scrum, tablero y control de impedimentos       |                R / A                |              C               |
| Infraestructura, roles, seguridad, rutas y colas            |                  R                  |              A               |
| Catálogo central, ofertas y carrito multicomercio           |                  R                  |              R               |
| Integración de pagos (SINPE, Tilopay, PayPal) y facturación |                  C                  |            R / A             |
| Validación con comercios y usuarios piloto                  |                  C                  |              R               |
| Pruebas de calidad, revisión de código y expediente         |                  R                  |              R               |

#### 2. Plan de comunicación

Definimos los siguientes canales y frecuencias para mantener la alineación durante el desarrollo:

| Participantes                         | Canal                             | Frecuencia                     | Propósito                                                                         |
| :------------------------------------ | :-------------------------------- | :----------------------------- | :-------------------------------------------------------------------------------- |
| Equipo de desarrollo                  | WhatsApp / GitHub                 | Continua (2 veces por semana)  | Sincronizar avances, reportar bloqueos y revisar Pull Requests.                   |
| Scrum Team (Sprint Review / Planning) | Reunión virtual                   | Cada 2 semanas (fin de Sprint) | Demostrar el incremento, actualizar el Burndown y planificar el siguiente Sprint. |
| Docente (Rudy Barboza)                | Sesión de clase / Entorno virtual | Semanal / Por entrega          | Presentar avances del expediente y aplicar retroalimentación.                     |
| Comercios y clientes piloto           | Contacto directo / Pruebas de uso | Según hitos del cronograma     | Validar flujos de catálogo, carrito y entrega, y recopilar mejoras.               |

#### 3. Working Agreements (Acuerdos de trabajo)

Para sostener el ritmo de trabajo con una capacidad de 2 horas semanales por integrante, acordamos las siguientes reglas internas:

- _Gestión del tiempo:_ Cada integrante organizará sus 2 horas semanales comprometidas; si surge un imprevisto, avisará con al menos 24 horas de anticipación para reajustar las tareas del Sprint.
- _Uso de GitHub y trazabilidad:_ Todo avance se registrará en GitHub Projects y cada commit o Pull Request llevará el ID de su historia correspondiente antes de integrarse a la rama principal.
- _Revisión cruzada:_ Ningún módulo se dará por terminado sin que el otro integrante valide su funcionamiento y cumplimiento con el Definition of Done.
- _Comunicación ante bloqueos:_ Si una tarea o integración externa presenta fallos que superan lo estimado, se notificará en menos de 12 horas para buscar una solución conjunta o activar un respaldo.
- _Actualización del expediente:_ Al cierre de cada semana de clase, ambos revisaremos y completaremos la sección correspondiente del documento antes de su entrega.

### Sección 11: Decisiones, cambios y evidencias de integración final

#### 1. Bitácora de decisiones y cambios

Durante el avance de los Sprints y las revisiones con el Product Owner, registramos los siguientes ajustes para mantener la viabilidad técnica y operativa del proyecto:

|    ID     | Decisión o cambio aplicado                                                                        | Motivo                                                                                | Impacto en el proyecto                                                                          |
| :-------: | :------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------------------- |
| **DC-01** | División de historias complejas (`HU-02`, `HU-04`, `HU-05`) en historias hoja de máximo 5 puntos. | Adecuar las entregas a la capacidad real del equipo (8 horas por Sprint).             | Permitió cerrar incrementos funcionales cada dos semanas sin arrastrar tareas incompletas.      |
| **DC-02** | Priorización de SINPE Móvil verificado (`HU-05a`) antes de Tilopay y PayPal.                      | Validar el flujo completo de compra y entrega con un medio de pago local inmediato.   | Adelantó las pruebas integrales del ciclo de pedido sin depender de credenciales externas.      |
| **DC-03** | Incorporación de tasa de cambio manual CRC/USD de respaldo (`HU-05d`).                            | Mitigar posibles interrupciones o demoras en la consulta del indicador 318 del BCCR.  | Garantizó la continuidad del _checkout_ en dólares con PayPal ante fallos del servicio externo. |
| **DC-04** | Cotización manual de envío para cargas especiales (`HU-06b`).                                     | Cubrir pedidos con volumen o peso fuera de la tarifa estándar calculada por OSRM.     | Evitó pérdidas operativas en entregas complejas sin frenar la automatización de rutas normales. |
| **DC-05** | Ejecución de pruebas automatizadas con SQLite en memoria y colas en segundo plano.                | Agilizar la validación continua (`php artisan test`) y desacoplar correos y facturas. | Redujo errores de regresión y mejoró los tiempos de respuesta al confirmar un pedido.           |

#### 2. Evidencias de gestión e integración

La trazabilidad entre la planificación del expediente y el producto construido se respalda mediante los siguientes artefactos:

- **Repositorio y control de versiones (GitHub):** Historial de _commits_ asociados a los identificadores de historias (`HU-01a` a `HU-08c`), organización por ramas y _Pull Requests_ revisados entre ambos integrantes.
- **Seguimiento ágil (GitHub Projects):** Tablero Kanban actualizado con el flujo de tarjetas (_Backlog_, _Por hacer_, _En progreso_, _En revisión_, _Terminado_) y control del gráfico _Burndown_ sobre el total de 60 puntos.
- **Pruebas y calidad de código:** Ejecución satisfactoria de la suite de pruebas (`php artisan test`), verificación de formato (`php vendor/bin/pint --test`) y compilación de activos (`npm run build`), junto con los procesos `queue:work` y `schedule:work` activos.
- **Documentación técnica del sistema:** Especificaciones y guías integradas en el repositorio (`docs/requisitos-marketplace-mvp.md`, `docs/manual-tecnico.md`, `docs/electronic-invoicing.md` y `docs/deployment-railway.md`).

#### 3. Guion de preparación de la demostración (Demo)

Para la presentación oficial en la Semana 13, ejecutaremos el siguiente recorrido funcional en vivo utilizando los usuarios de demostración configurados en el sistema:

1. **Acceso y control de roles:** Ingreso con `admin@komoya.test`, `supermercado@komoya.test` y `cliente@komoya.test` para evidenciar la separación de vistas y permisos protegidos.
2. **Gestión de ofertas e inventario:** Actualización de precios y existencias de productos desde el panel del comercio (`ferreteria@komoya.test` y `farmacia@komoya.test`).
3. **Compra multicomercio y reservas:** Búsqueda de artículos en el catálogo público, armado de un carrito con productos de distintos comercios, confirmación de existencias y visualización del plazo de reserva de 15 minutos.
4. **Cálculo de envío y pago unificado:** Validación de dirección dentro del radio de 50 km, cálculo automático de tarifa logística, aprobación del total y procesamiento de pago en ambiente de pruebas.
5. **Seguimiento operativo y comprobantes:** Gestión del estado del pedido desde el panel del administrador, verificación de notificaciones en cola y consulta del resumen y comprobante del pedido desde la cuenta del cliente.

### Sección 12: Producto / Incremento final y cierre del proyecto

#### 1. Resumen del incremento final entregado

Al cierre del proyecto, cumplimos con el **Product Goal** establecido mediante el desarrollo e integración de la primera versión funcional (MVP) de **KomoYa**. La plataforma web permite a los habitantes de Pital y zonas aledañas comparar precios entre comercios locales, consolidar productos de distintos establecimientos en un carrito único, confirmar existencias, calcular el envío centralizado y completar el pago de forma segura.

El incremento final cubre las 7 épicas planificadas en el _Product Backlog_:

| Épica          |           Historias            |   Estado   | Funcionalidad entregada en el producto                                                                                                                                                 |
| :------------- | :----------------------------: | :--------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Seguridad**  |         HU-01a, HU-01b         | Completado | Autenticación, recuperación de cuenta, protección de rutas y navegación diferenciada para administrador, comercio y cliente.                                                           |
| **Catálogo**   |         HU-02a, HU-02b         | Completado | Catálogo central administrado y gestión independiente de ofertas, precios y existencias por cada comercio.                                                                             |
| **Compra**     | HU-03, HU-04a, HU-04b, HU-04c  | Completado | Búsqueda pública, carrito multicomercio, subórdenes por tienda, confirmación de inventario y reservas con vencimiento automático a los 15 minutos.                                     |
| **Logística**  |         HU-06a, HU-06b         | Completado | Validación de cobertura en radio de 50 km, cálculo de recorridos y tarifas con OSRM, recargos y flujo de cotización manual.                                                            |
| **Pagos**      | HU-05a, HU-05b, HU-05c, HU-05d | Completado | Pago unificado con verificación de comprobantes SINPE Móvil, _checkout_ en colones con Tilopay y cobro en dólares con PayPal usando tipo de cambio BCCR (con tasa manual de respaldo). |
| **Operación**  |     HU-08a, HU-08b, HU-08c     | Completado | Bitácora de auditoría, programación de compras y entregas consolidadas por el operador e historial de pedidos para el cliente.                                                         |
| **Documentos** |     HU-07a, HU-07b, HU-07c     | Completado | Notificaciones transaccionales en cola, acceso autorizado a comprobantes y conexión fiscal configurable con FacturaEnCR.                                                               |

#### 2. Entregables de cierre y artefactos del producto

Como respaldo de la entrega oficial y la demostración en vivo, consolidamos los siguientes artefactos:

- **Repositorio y código fuente:** Aplicación desarrollada en Laravel, PHP, PostgreSQL, Tailwind CSS y Alpine.js, organizada en GitHub con trazabilidad de _commits_ y pruebas automatizadas (`php artisan test`) sobre SQLite en memoria.
- **Entorno operativo y despliegue:** Configuración lista para producción con soporte HTTPS (guías para Railway con Neon PostgreSQL y Laravel Cloud), datos de demostración (`SEED_DEMO_DATA=true`) y ejecución de procesos en segundo plano (`queue:work` y `schedule:work`).
- **Documentación técnica:** Especificaciones del MVP, manual técnico, guía de facturación electrónica y manual de despliegue integrados en la carpeta `docs/` del proyecto.
- **Expediente del Proyecto:** Documento integral actualizado desde la Sección 00 hasta la Sección 12, alineado con el tablero en GitHub Projects y el incremento demostrado.

#### 3. Lecciones aprendidas y cierre del proyecto

El desarrollo incremental de KomoYa dejó aprendizajes clave para la gestión y construcción de soluciones de software:

- **División de historias y ritmo sostenible:** Fragmentar requerimientos amplios (como el flujo de carrito multicomercio y las pasarelas de pago) en historias pequeñas de máximo 5 puntos permitió mantener un avance constante y verificable acorde con la disponibilidad del equipo.
- **Resiliencia ante integraciones externas:** Incorporar mecanismos de respaldo operativo —como la tasa de cambio manual CRC/USD frente al BCCR, la verificación manual de SINPE Móvil y la cotización manual de cargas especiales— evitó bloqueos y aseguró la continuidad del servicio.
- **Automatización para la integridad de datos:** Delegar los vencimientos de reservas de 15 minutos, el envío de correos y los reintentos fiscales a colas y tareas programadas garantizó estabilidad y evitó inconsistencias de inventario o cobros duplicados.
- **Evolución futura (Post-MVP):** Como siguientes pasos fuera del alcance de esta primera versión, se proyecta incorporar seguimiento en tiempo real de entregas, métricas avanzadas de ventas para los comercios afiliados y aplicaciones móviles nativas.
