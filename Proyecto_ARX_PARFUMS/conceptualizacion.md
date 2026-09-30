
ARX PARFUMS,  SISTEMA WEB MAS ECOMMERCE

1. Presentación del proyecto
Nombre del sistema: ARX STORE — Sistema web de comercio electrónico para ARXPARFUMS.

Integrantes del grupo:

| Nombre | Rol |
|---|---|
| Alan Cabrera | Líder de proyecto / Analista (enlace con el cliente) |
| Alba Lopez |  Diseñadora UX|
| Marcelo Cano | Diseñador de base de datos |
| Sebastian Prieto | Diseñador UI|

Usuario / cliente real: 
ARX Parfums, emprendimiento paraguayo dedicado a la comercialización de perfumes (originales, árabes y de diseñador) al por menor y al por mayor. Actualmente cuenta con un sistema de punto de venta (POS) interno para registrar ventas en local, controlar caja y administrar ventas a cuotas, pero no dispone de un canal de venta en línea propio.
________________________________________
2. Definición del problema
   
Situación actual. ARX Parfums vende sus productos de dos formas:

1.	Venta presencial, registrada en su sistema POS interno (caja, stock, ventas al contado y a cuotas).
2.	Venta por redes sociales y WhatsApp: el cliente ve publicaciones en Instagram/Facebook, consulta precio y disponibilidad por mensaje, y el vendedor responde manualmente, coordina el pago (transferencia o efectivo) y la entrega.
- Problemática concreta.
  
•	Atención 100 % manual: cada consulta ("¿cuánto sale?", "¿hay stock?", "¿qué tamaño tiene?") debe responderse una por una, lo que consume mucho tiempo y genera demoras; muchas consultas fuera de horario se pierden.

•	Catálogo disperso y desactualizado: los productos están repartidos en publicaciones y estados; el cliente no puede ver el catálogo completo, filtrar por marca, familia olfativa o precio, ni saber si un producto sigue disponible.

•	Stock desincronizado: las ventas por WhatsApp no siempre se cargan a tiempo en el POS, por lo que se ofrecen productos sin existencia o se venden dos veces.

•	Pedidos sin trazabilidad: los pedidos quedan en conversaciones de chat; no hay registro ordenado de estado (pendiente, pagado, enviado, entregado), ni historial por cliente.

•	Verificación de pagos lenta: los comprobantes de transferencia llegan como capturas por chat y deben verificarse a mano.

•	Alcance limitado: el negocio depende del horario y de la disponibilidad del vendedor para atender, lo que limita el crecimiento de las ventas en el interior del país.
________________________________________
3. Propósito y objetivos

Objetivo general:

Desarrollar un sistema web de comercio electrónico para ARX Parfums que permita a sus clientes consultar el catálogo y realizar pedidos en línea las 24 horas, integrado con el inventario del negocio, para reducir la atención manual y centralizar la gestión de pedidos.

Objetivos específicos:


1.	Publicar un catálogo en línea con el 100 % de los productos activos, con precio, fotos, descripción y disponibilidad, filtrable por marca, género, familia olfativa y rango de precio.
   
2.	Permitir que el cliente arme un carrito y confirme un pedido en no más de 5 pasos, eligiendo método de pago (transferencia bancaria o pago contra entrega) y método de entrega (retiro o envío).
   
3.	Descontar y reservar el stock automáticamente al confirmar un pedido, compartiendo la misma base de productos que usa el POS, para eliminar la venta de productos sin existencia.
   
4.	Brindar al administrador un panel de gestión de pedidos con estados (pendiente de pago, pagado, en preparación, enviado, entregado, cancelado) y notificación al cliente en cada cambio de estado.
   
5.	Permitir al cliente consultar su historial de pedidos y el estado actual de cada uno sin necesidad de escribir por WhatsApp.
   
6.	Generar reportes básicos de ventas en línea (ventas por período, productos más vendidos, pedidos por estado).
________________________________________
4. Alcance del proyecto
   
Incluye (dentro del alcance) — Versión 1:

•	Catálogo público: listado de productos, búsqueda, filtros, ficha de producto con fotos, notas olfativas y presentaciones (ml).

•	Carrito de compras: agregar, quitar, modificar cantidades y ver el total.

•	Checkout / pedido: datos de entrega, elección de método de pago (transferencia con carga de comprobante, o contra entrega) y método de entrega (retiro en local o envío).

•	Panel de administración: gestión de productos, categorías/marcas, precios, imágenes y stock; gestión de pedidos y cambio de estados; verificación de comprobantes.

•	Gestión de usuarios internos: roles Administrador y Vendedor con permisos diferenciados.

•	Integración de inventario con el POS existente: ambos sistemas trabajan sobre el mismo stock.

•	Reportes básicos de ventas en línea.

•	Diseño adaptable (responsive) para uso desde celulares.

•	Facturación electrónica (SIFEN) ante la SET: la facturación sigue gestionándose por el circuito actual del negocio.

•	Aplicación móvil nativa (Android/iOS): solo se desarrolla la versión web responsive

•	Ventas a cuotas en línea: el crédito y las cuotas siguen gestionándose exclusivamente desde el POS.

________________________________________
5. Interesados (stakeholders)
Interesado	Descripción	Interés en el proyecto
Cliente final (comprador)	Persona que compra perfumes al por menor desde cualquier punto del país, principalmente desde el celular.	Ver el catálogo completo con precios y stock reales, comprar a cualquier hora de forma simple y seguir el estado de su pedido.
Cliente (dueño/a de ARX Parfums)	Propietario/a del negocio y quien financia y valida el proyecto.	Aumentar las ventas, reducir el tiempo de atención manual, tener control ordenado de pedidos y stock, y contar con reportes para tomar decisiones.
Administrador del sistema	Persona del negocio (o el equipo de desarrollo durante el soporte) encargada de configurar el sistema, usuarios y catálogo.	Un sistema fácil de mantener, con roles y permisos claros, respaldos y seguridad.
Vendedor / personal de despacho	Empleado que atiende pedidos, verifica pagos y prepara envíos.	Ver en un solo lugar los pedidos pendientes, confirmar pagos rápidamente y actualizar estados sin duplicar carga en el POS.
Revendedor mayorista	Cliente que compra por volumen para revender.	Consultar disponibilidad y precios de forma rápida para hacer sus pedidos.
Equipo de desarrollo (grupo)	Integrantes del grupo de Ingeniería de Software.	Desarrollar un sistema real y bien documentado que cumpla los requisitos de la cátedra.
Cátedra de Ingeniería de Software	Docentes que evalúan el trabajo práctico.	Verificar la aplicación correcta del proceso de análisis y diseño de software.
________________________________________
6. Justificación / viabilidad
Viabilidad técnica: Alta. El grupo tiene experiencia práctica en desarrollo web con PHP y MySQL; uno de los integrantes desarrolló y mantiene el sistema POS actual de ARX Parfums, por lo que conoce su base de datos y sus reglas de negocio. Las tecnologías elegidas son de uso libre, ampliamente documentadas y con gran comunidad. Los conocimientos que faltan (framework Laravel, buenas prácticas de e-commerce) pueden adquirirse durante el cuatrimestre con documentación oficial y cursos gratuitos.
Viabilidad operativa: Alta. El personal del negocio ya utiliza a diario un sistema web (el POS), por lo que está habituado a este tipo de herramientas. El panel de administración se diseñará con una interfaz similar y simple, y se entregará una guía de uso. El cliente tiene interés directo en el proyecto y está disponible para validar requisitos, lo que reduce la resistencia al cambio.
Viabilidad económica (alto nivel): Alta. Todo el software a utilizar es libre y gratuito (PHP, Laravel, MySQL, Bootstrap). El costo operativo principal es un hosting compartido o VPS básico y un dominio, de bajo costo mensual para un comercio. El esfuerzo de desarrollo lo asume el grupo en el marco de la materia. El beneficio esperado (más ventas fuera de horario, menos horas de atención manual, menos errores de stock) justifica ampliamente la inversión.
________________________________________
7. Visión general de la solución
ARX Store será una tienda en línea propia de ARX Parfums a la que el cliente podrá entrar desde el celular o la computadora. Allí verá todos los perfumes disponibles con fotos, precios y descripción, podrá buscarlos y filtrarlos, agregarlos a un carrito y hacer su pedido sin tener que escribir a nadie. Al finalizar elegirá cómo pagar (transferencia, subiendo el comprobante, o contra entrega) y cómo recibir el producto (retiro en local o envío).
Del lado del negocio, el personal tendrá un panel de administración donde verá cada pedido nuevo, confirmará el pago, lo preparará y actualizará su estado. Como la tienda en línea y el sistema de caja del local comparten el mismo inventario, cada venta —en el local o por internet— descuenta el stock en un solo lugar, evitando vender productos que ya no existen.
 Cliente (celular/PC) ──► Tienda en línea ARX PARFUMS ──► Pedido
                                    │
                                    ▼
                         Inventario compartido ◄── POS del local
                                    │
                                    ▼
             Panel de administración (pedidos, stock, reportes)
________________________________________


8. Glosario de términos

|Término | Definición|
|---|---|
|Producto: |	Perfume u otro artículo que ARX Parfums ofrece a la venta. Tiene marca, nombre, género, familia olfativa, presentaciones, precio e imágenes.|
| Presentación: |	Variante de un producto según su contenido en mililitros (ej. 50 ml, 100 ml). Cada presentación tiene su propio precio y stock.|
|Marca:|	Casa fabricante del perfume (ej. Lattafa, Dior, Carolina Herrera).|
|Familia olfativa:|	Clasificación del aroma de un perfume (amaderado, floral, oriental, cítrico, etc.). Se usa como filtro del catálogo.|
| Notas olfativas:|Ingredientes aromáticos que componen el perfume, divididos en notas de salida, de corazón y de fondo.|
|Perfume original / de diseñador:	|Perfume de marcas internacionales reconocidas, comercializado en su empaque de fábrica.
|Perfume árabe	|Perfume de casas perfumistas de Medio Oriente, de alta concentración y precio accesible; segmento importante del negocio.|
|Decant:	|Porción de un perfume original trasvasada a un frasco pequeño (ej. 5 o 10 ml) para venderla fraccionada.|
| Catálogo:	|Conjunto de productos activos visibles para los clientes en la tienda en línea.|
| Stock:	|Cantidad disponible de una presentación de producto. Es compartido entre la tienda en línea y el POS.|
| Stock reservado:|	Unidades separadas para un pedido confirmado cuyo pago aún no fue verificado.|
| Carrito:|	Lista temporal de productos que el cliente selecciona antes de confirmar el pedido.|
|Pedido:	|Solicitud de compra confirmada por un cliente en la tienda en línea, con productos, montos, método de pago, método de entrega y estado.|
|Estado del pedido:	|Etapa en la que se encuentra un pedido: Pendiente de pago, Pagado, En preparación, Enviado, Entregado o Cancelado.|
| Checkout:	|Proceso de finalización de la compra: datos del cliente, entrega, pago y confirmación.|
| Comprobante de pago:	|Imagen o PDF de la transferencia bancaria que el cliente adjunta al pedido para su verificación.|
| Pago contra entrega:|Modalidad en la que el cliente abona el pedido en efectivo al recibirlo.|
| Cliente registrado:	|Comprador con cuenta en la tienda, que puede ver su historial de pedidos y guardar direcciones.|
| Revendedor / mayorista:|	Cliente que compra en cantidad para revender, generalmente con precios diferenciados.|
| POS (Punto de Venta):|	Sistema interno existente de ARX Parfums con el que se registran las ventas en el local, la caja y las ventas a cuotas.|
|Panel de administración:	|Sección privada del sistema donde el personal gestiona productos, stock, pedidos, usuarios y reportes.|
|Guaraní (PYG / Gs.):|	Moneda en la que se expresan todos los precios del sistema.|

________________________________________

9. Riesgos iniciales

|Riesgo|Impacto |	Estrategia de mitigación|
|---|---|
|- Baja disponibilidad del cliente para reuniones y validaciones.|Alto|Agendar reuniones cortas quincenales fijas; validar avances por WhatsApp con capturas y mockups; un integrante actúa como enlace único con el cliente.|

- Incompatibilidades al integrar el inventario con el POS existente (estructura de base de datos distinta).	Alto,	Analizar en la etapa de Análisis el modelo de datos actual del POS; definir una capa de acceso común al stock; hacer pruebas sobre una copia de la base, nunca sobre producción.

- Crecimiento del alcance (el cliente pide nuevas funciones, ej. pago con tarjeta, cuotas en línea).	Alto,	Documentar el alcance en esta entrega y validarlo con el cliente; toda nueva solicitud se registra como mejora para una versión futura.

- Falta de tiempo del grupo por otras materias y exámenes.	Medio,	Planificación por iteraciones cortas con tareas asignadas por integrante; seguimiento semanal en el tablero del repositorio (GitHub Projects).

- Curva de aprendizaje del framework Laravel.	Medio,	Capacitación temprana con la documentación oficial; prototipo pequeño al inicio; apoyo en el integrante con más experiencia en PHP.

- Seguridad de datos de clientes y de pagos (robo de cuentas, comprobantes falsos).	Alto,	HTTPS obligatorio, contraseñas cifradas, protección CSRF, validación de archivos subidos y verificación manual del comprobante antes de despachar.

- Catálogo incompleto (faltan fotos o descripciones de productos).	Medio,	Acordar con el cliente la carga progresiva del catálogo; plantilla estándar de ficha de producto; imágenes genéricas temporales.

- Rotación o baja de un integrante del grupo.	Medio,	Documentación compartida en el repositorio; cada módulo conocido por al menos dos integrantes.

________________________________________

10. Selección tecnológica preliminar

Componente - Elección - Justificación breve

Lenguaje de programación: PHP 8.2, Es el lenguaje del POS actual de ARX Parfums, lo que facilita la integración y la reutilización de conocimiento; el grupo ya lo domina; está disponible en casi cualquier hosting a bajo costo.

Framework: Laravel 11 (backend, con vistas Blade) + Bootstrap 5 (frontend), Laravel aporta arquitectura MVC, autenticación, protección CSRF, ORM (Eloquent), migraciones y envío de correos ya resueltos, lo que acelera el desarrollo y mejora la seguridad frente a PHP puro. Bootstrap permite un diseño responsive sin esfuerzo adicional.

Base de datos: MySQL 8, Es el motor que ya usa el POS, lo que permite compartir el inventario en la misma base; es relacional (adecuado para pedidos, stock y clientes), gratuito y ampliamente soportado.

Control de versiones y documentación: Git + GitHub / GitHub Pages, Requerido por la cátedra; permite registrar la participación de cada integrante y publicar la documentación.

Herramientas de modelado: draw.io / PlantUML, Gratuitas, soportan notación UML y exportan imágenes para publicar en el sitio.
