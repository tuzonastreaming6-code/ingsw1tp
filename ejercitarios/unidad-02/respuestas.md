# Respuestas — Ejercitario Unidad 02

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · Propiedades de los sistemas

**1. Define en tus propias palabras qué es un sistema y da un ejemplo distinto al utilizado en clase.**

_Respuesta:_ 

Un sistema es un conjunto de partes que trabajan juntos y se relacionan entre si para cumplir un objetivo común.


**2. Enumera los seis elementos de un sistema basado en computadora.**

1- Software
2- Hardware
3- Personas
4- Base de datos
5- Documentacion
6- Procedimientos


**3. Piensa en un sistema cotidiano (por ejemplo, una biblioteca, un supermercado o un club deportivo) y completa la tabla con un ejemplo propio para cada propiedad.**

| Propiedad | Ejemplo en el sistema elegido | Ejemplo en el supermercado

| Jerarquía: El supermercado se organiza en niveles: gerencia general → jefes de sección (cajas, depósito, reposición, atención al cliente) → empleados de cada sección. Además, él mismo puede ser parte de un sistema mayor (una cadena de supermercados)
| Límites (fronteras): Lo que está dentro: el local, los empleados, la mercadería y los sistemas de venta e inventario. Lo que queda fuera (el entorno): los proveedores, los clientes, la competencia y las regulaciones. La frontera separa lo que el supermercado controla de lo que no.
| Interrelación de elementos: Las cajas dependen del sistema de inventario para descontar el stock; la reposición depende de lo que informa el depósito; el depósito depende de los pedidos a proveedores. Si falla uno, afecta a los demás (ej.: si el depósito no repone, las góndolas quedan vacías).
| Propiedades emergentes: La "experiencia de compra" (poder atender a cientos de clientes a la vez, encontrar todo en un solo lugar, cobrar rápido) no la produce ninguna caja, góndola o empleado por separado: surge de la interacción de todos los elementos funcionando juntos

**4. Dentro del mismo sistema, identifica un posible subsistema y justifica por qué lo consideras tal.**

Lo considero un subsistema porque es un sistema completo en sí mismo tiene sus propios elementos (cajeros, terminales de cobro, lectores de código de barras, software de facturación y medios de pago) que se organizan para cumplir un objetivo propio: procesar el pago de cada cliente de forma rápida y correcta— pero a la vez es solo una parte del sistema mayor que es el supermercado.
Además, se interrelaciona con los demás subsistemas: descuenta productos del inventario, le informa a la gerencia cuánto se vendió y depende de la reposición para que haya mercadería que cobrar. Por eso cumple la definición de subsistema: un sistema que, a su vez, es un componente de un sistema más grande.


---

## Tema 2 · Los sistemas y su entorno

**5. Elige un sistema de software que uses habitualmente e identifica: una entrada, una salida y un elemento de su entorno.**

| Elemento | Descripción en el sistema elegido |
|---|---|
| Sistema elegido: WhatsApp — aplicación de mensajería que uso para comunicarme con clientes y contactos todos los días.
| Una entrada: El mensaje de texto que escribo y los datos que ingreso (el contacto al que le envío, una foto o un archivo adjunto). Es lo que le doy al sistema para que procese.
| Una salida: El mensaje ya entregado que aparece en la pantalla del destinatario con su tilde de "enviado, leído", y la notificación que recibe, es el resultado que el sistema produce.
| Un elemento del entorno: La conexión a internet o la red del proveedor de telefonía. Está fuera del sistema WhatsApp, no la controla la app, pero WhatsApp depende de ella para funcionar. 

**6. ¿El sistema que elegiste es abierto o cerrado? Justifica tu respuesta.**

_Respuesta:_


**7. Explica con tus palabras qué es la retroalimentación (feedback) en un sistema y da un ejemplo.**

_Respuesta:_


**8. Para el mismo sistema, menciona una restricción externa real que podría afectarlo, indicando si es organizacional, regulatoria o tecnológica.**

_Respuesta:_


---

## Tema 3 · Modelado de sistemas

**9. Menciona dos razones por las cuales es útil modelar un sistema antes de construirlo.**

_Respuesta:_

1. Permite detectar errores y problemas antes de construir el sistema, evitando costos y retrabajos.
2. Facilita la planificación y comprensión del sistema, ya que permite visualizar cómo funcionará y cómo interactuarán sus diferentes componentes.


**10. Ejercicio de relación** (completá con el número que corresponda a cada letra):

| Nivel de visión | Descripción |
|---|---|
| A. Visión del mundo (worldview) | _3_ |
| B. Visión del dominio | _4_ |
| C. Visión del elemento | _1_ |
| D. Visión detallada | _2_ |

1. El sistema particular que se va a construir, dentro del dominio.
2. Los componentes internos del sistema: software, hardware, datos, etc.
3. El contexto global: todos los sistemas y organizaciones que interactúan.
4. El sector o área específica del negocio dentro de ese contexto.

**11. Explica la diferencia entre vista estructural y vista de comportamiento, y da un ejemplo de notación para cada una.**

_Respuesta:_

* Vista estructural: muestra cómo está compuesto el sistema, sus elementos y las relaciones entre ellos.
    Ejemplo de notación: diagrama de clases UML.
* Vista de comportamiento: muestra cómo funciona el sistema, las acciones, eventos y cambios que ocurren a lo largo del tiempo.
    Ejemplo de notación: diagrama de secuencia UML.


**12. Diagrama de contexto:** elige un sistema simple (por ejemplo, un cajero automático, una app de delivery) y dibujá un diagrama de contexto que muestre el sistema y al menos dos entidades externas con las que interactúa. Adjuntá la imagen acá abajo.

_(Arrastrá la imagen a este archivo desde el editor de GitHub para insertarla)_


**13. ¿En qué situación elegirías usar simulación en lugar de un modelo estático? Da un ejemplo concreto.**

_Respuesta:_


---

## Tema 4 · El proceso de Ingeniería de Sistemas

**14. Explica la diferencia entre Ingeniería de procesos de negocio e Ingeniería de producto, dando un ejemplo de cada una.**

_Respuesta:_ 

Ingeniería de procesos de negocio: optimiza el funcionamiento interno de una empresa (flujos de trabajo, eficiencia, costos).
Ejemplo: automatizar el proceso de aprobación de préstamos en un banco para reducirlo de 5 días a 1.

Ingeniería de producto: diseña y desarrolla un producto para el mercado.

Ejemplo: crear una app móvil de pagos, desde su diseño hasta su lanzamiento.

Diferencia clave: una mejora procesos internos; la otra crea algo para vender o usar externamente.


**15. Ordena numéricamente (1 a 4) los siguientes pasos genéricos del proceso de Ingeniería de Sistemas, según la secuencia vista en clase.**

| N.º | Paso |
|---|---|
|3 | Especificación del sistema |
|1 | Definición de necesidades |
|4 | Asignación de requisitos entre elementos |
|2 | Análisis de factibilidad |

**16. Reflexión final:** ¿por qué crees que es importante que un ingeniero de software comprenda el sistema completo (Ingeniería de Sistemas) antes de comenzar a programar? Relaciona tu respuesta con algún ejemplo visto en la Unidad 01 o en esta unidad.

_Respuesta:_

Es importante porque el software que un ingeniero construye no funciona en el vacío: forma parte de un sistema más grande, y si no se entiende ese sistema completo, se corre el riesgo de programar algo que técnicamente funciona pero que no resuelve el problema real.

Un ejemplo claro es el del **hospital** visto en la Unidad 02: ahí el sistema no es solo el software, sino también los médicos y enfermeras que lo usan, el hardware, los datos de los pacientes y los procedimientos del hospital, todos trabajando juntos. Si un ingeniero solo se enfoca en programar sin conocer cómo trabaja el personal médico o qué reglas de privacidad hay que cumplir con los datos de los pacientes, puede terminar creando un sistema difícil de usar o que ni siquiera se pueda implementar por no respetar esas normas.

Por eso, antes de programar, hay que tener una visión global del sistema: quiénes lo van a usar, con qué otras partes se relaciona y qué reglas del entorno debe respetar. Así el software que se construye realmente encaja con la necesidad real, en vez de resolver bien un problema que no era el correcto.

