1. Presentación del proyecto
Nombre del sistema: ARX STORE — Sistema web de comercio electrónico para ARXPARFUMS.

Integrantes del grupo:

Nombre	-    Rol

Alan Cabrera	     Líder de proyecto / Analista funcional (enlace con el cliente).

Alba Lopez	     Diseñador UX.

Marcelo Cano	     Diseñador de base de datos.

Sebastian Prieto   Diseñador UI.

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

