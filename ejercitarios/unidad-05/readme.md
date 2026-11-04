# Respuestas — Ejercitario Unidad 05

---

## Tema 1 · El diseño en la ingeniería de software

**1. Explica con tus palabras la diferencia entre diseño conceptual y diseño técnico (detallado). Da un ejemplo de una decisión de cada tipo para un sistema de gestión de una biblioteca.**

_Respuesta:_

El diseño conceptual define qué hará el sistema y cómo funcionará en general, sin entrar en detalles técnicos. En cambio, el diseño técnico o detallado explica cómo se va a construir el sistema, especificando las tecnologías, la base de datos y los procedimientos que se utilizarán.

Ejemplo para un sistema de gestión de una biblioteca:

* Diseño conceptual: decidir que el sistema permitirá registrar libros, gestionar préstamos y devoluciones, y consultar la disponibilidad de los libros.
* Diseño técnico: decidir que se utilizará una base de datos MySQL para guardar los libros, los usuarios y los préstamos, relacionando sus datos mediante identificadores.

En resumen, el diseño conceptual define qué se necesita y el diseño técnico establece cómo se implementará.
| Tipo | Ejemplo de decisión en un sistema de biblioteca |
|---|---|
| Conceptual | "El sistema tendrá tres partes: Catálogo de libros, Socios y Préstamos. Un socio podrá tener como máximo 3 libros prestados a la vez y podrá reservar un libro que está prestado." |
| Técnico | "La clase `ServicioPrestamo` tendrá el método `registrar(idSocio, idEjemplar)`, que valida dentro de una transacción que el socio tenga menos de 3 préstamos activos. La tabla `prestamo` tendrá un índice sobre `fecha_vencimiento` para encontrar rápido los préstamos vencidos." |

**2. Completa el siguiente cuadro sobre los elementos del modelo de diseño.**

| Elemento del diseño | ¿Qué define? | Ejemplo en un sistema de inscripciones |
|---|---|---|
| Diseño de datos | Las estructuras de datos y el modelo de la base de datos (entidades, atributos, relaciones, restricciones) que el sistema necesita. | Tablas `Alumno`, `Materia`, `Seccion` (con su cupo) e `Inscripcion` (alumno, sección, fecha, estado), con una restricción que impide inscribir dos veces al mismo alumno en la misma sección. |
| Diseño arquitectónico | La estructura general del sistema: sus grandes componentes, cómo se relacionan y el estilo arquitectónico. | Aplicación web cliente-servidor en tres capas (presentación, lógica de negocio y datos), con un servidor de aplicaciones y un servidor de base de datos. |
| Diseño de interfaces | Cómo se comunica el sistema con los usuarios, con otros sistemas y cómo se comunican sus módulos internos entre sí. | La pantalla "Inscribirme a materias", con la lista de secciones disponibles y el cupo restante, y la API que consulta al sistema de pagos si el alumno tiene la matrícula al día. |
| Diseño de componentes | El funcionamiento interno de cada módulo: sus clases, algoritmos, estructuras locales y su interfaz. | El componente `ServicioInscripcion`, con el algoritmo que verifica correlatividades, superposición de horarios y cupo antes de confirmar la inscripción. |

---

## Tema 2 · Conceptos fundamentales de diseño

**3. Ejercicio de relación**

| Concepto | Número |
|---|---|
| A. Abstracción | **4** |
| B. Refinamiento progresivo | **6** |
| C. Ocultamiento de información | **2** |
| D. Separación de intereses | **5** |
| E. Patrón | **3** |
| F. Refactorización | **1** |

**4. Aplica refinamiento progresivo a la tarea "Registrar una venta en un comercio": escribí al menos tres niveles de detalle, refinando en el tercer nivel uno de los pasos del segundo.**

_Respuesta:_

**Nivel 1**
- Registrar una venta.

**Nivel 2**
1. Iniciar la venta (identificar al cajero y la caja abierta).
2. Cargar los productos vendidos.
3. Calcular el total.
4. Cobrar.
5. Emitir el comprobante.
6. Actualizar el stock y la caja.

**Nivel 3** (refinamiento del paso 4 "Cobrar")
- 4.1. Mostrar el total a cobrar.
- 4.2. Elegir el medio de pago (efectivo, tarjeta, transferencia o cuotas).
- 4.3. Si es **efectivo**:
  - 4.3.1. Ingresar el monto recibido.
  - 4.3.2. Si el monto es menor al total, avisar y volver a 4.3.1.
  - 4.3.3. Calcular y mostrar el vuelto.
- 4.4. Si es **tarjeta**:
  - 4.4.1. Enviar el monto a la terminal bancaria (POS).
  - 4.4.2. Esperar la autorización.
  - 4.4.3. Si es rechazada, avisar y volver a 4.2.
- 4.5. Si es **transferencia**, registrar el número de operación.
- 4.6. Si es **en cuotas**, registrar la cantidad de cuotas y generar el plan de pagos del cliente.
- 4.7. Registrar el pago en la caja con fecha, hora, medio y monto.

---

## Tema 3 · Descomposición y modularidad

**5. Explica por qué no conviene dividir un sistema ni en muy pocos ni en demasiados módulos. ¿Qué costos aumentan en cada extremo?**

_Respuesta:_

No conviene dividir un sistema en muy pocos módulos porque se vuelven grandes y difíciles de entender, mantener y modificar. Esto aumenta el costo de mantenimiento y de corrección de errores.

Por otro lado, dividirlo en demasiados módulos genera muchas conexiones y dependencias entre ellos, lo que aumenta el costo de integración, comunicación y coordinación.

En conclusión, lo ideal es encontrar un equilibrio, con módulos bien organizados, que sean fáciles de mantener y que trabajen correctamente entre sí.

**6. Para un sistema de gestión de un consultorio médico, propone dos descomposiciones distintas e indica qué módulos tendría cada una.**

| Estrategia | Módulos propuestos |
|---|---|
| Por capas | **Presentación**: pantallas de recepción, agenda del médico, historia clínica y caja. **Lógica de negocio**: servicios de turnos, consultas, recetas y facturación, con sus reglas (ej. no superponer turnos). **Acceso a datos**: repositorios de Paciente, Médico, Turno, Consulta y Pago. **Infraestructura**: autenticación de usuarios, envío de recordatorios por WhatsApp/correo y respaldos. |
| Por dominio | **Pacientes**: alta y datos personales, seguro médico. **Agenda y turnos**: disponibilidad de médicos, reserva, cancelación y recordatorios. **Historia clínica**: consultas, diagnósticos, recetas y estudios. **Facturación y cobros**: aranceles, cobro de consultas y reportes de caja. **Usuarios y seguridad**: roles (médico, recepcionista, administrador) y permisos. |

---

## Tema 4 · Cohesión y acoplamiento

**7. Indica el tipo de cohesión de cada módulo y justifica brevemente.**

| Módulo | Tipo de cohesión y justificación |
|---|---|
| a) "Utilidades": FormatearFecha, EnviarCorreo y CalcularIVA. | **Coincidental**: las tres funciones no tienen ninguna relación entre sí; están juntas solo porque "no tenían otro lugar". |
| b) "IniciarSistema": abre la conexión a la base, carga la configuración y borra archivos temporales. | **Temporal**: las tareas son distintas y se agrupan solo porque se ejecutan en el mismo momento (al iniciar). |
| c) "CalcularPromedioAlumno": obtiene las notas de un alumno y devuelve su promedio. | **Funcional**: todo el módulo contribuye a una única tarea bien definida: calcular el promedio. |
| d) "ProcesarOperacion": recibe un código y, según su valor, imprime, guarda o elimina un registro. | **Lógica**: agrupa operaciones de una misma categoría ("operar sobre un registro") y elige cuál ejecutar con un parámetro de control. |
| e) Lee un registro, lo valida y, con el registro ya validado, calcula su total. | **Secuencial**: la salida de cada paso es la entrada del siguiente (leer → validar → calcular). |

**8. Indica el tipo de acoplamiento en cada caso.**

| Situación | Tipo de acoplamiento |
|---|---|
| a) El módulo A llama a B pasándole solo el idAlumno. | **De datos**: solo se pasa el dato simple que B necesita. |
| b) A le pasa a B una bandera modo = "imprimir" / "guardar" que decide qué hace B. | **De control**: A dirige la lógica interna de B mediante una bandera. |
| c) Varios módulos leen y modifican la variable global TotalVentas. | **Común**: comparten un dato global. |
| d) A modifica directamente un atributo privado de B. | **De contenido**: A accede al interior de B y rompe su encapsulamiento. |
| e) A le pasa a B el objeto Alumno completo, aunque B solo usa la fecha de nacimiento. | **Por estampado**: se pasa una estructura completa de la que B usa solo una parte. |

**9. Explica por qué la alta cohesión y el bajo acoplamiento suelen ir de la mano. Da un ejemplo.**

_Respuesta:_

La alta cohesión significa que un módulo se encarga de tareas relacionadas entre sí, mientras que el bajo acoplamiento significa que los módulos dependen poco unos de otros.

Suelen ir de la mano porque, cuando cada módulo tiene una función clara y específica, necesita menos conexiones y dependencias con otros módulos. Esto facilita el mantenimiento y los cambios en el sistema.

Ejemplo: en un sistema de biblioteca, un módulo se encarga de gestionar los préstamos y otro de registrar los libros. Si cada uno cumple su función sin depender demasiado del otro, existe alta cohesión y bajo acoplamiento.

Así, si se modifica el registro de libros, no será necesario cambiar todo el módulo de préstamos.

---

## Tema 5 · Arquitectura y estilos arquitectónicos clásicos

**10. Ejercicio de relación**

| Estilo arquitectónico | Número |
|---|---|
| A. En capas | **5** |
| B. Cliente-servidor | **4** |
| C. Centrado en datos (repositorio) | **2** |
| D. Tuberías y filtros | **1** |
| E. Modelo-Vista-Controlador | **3** |

**11. Dibujá o describí la arquitectura en capas de un sistema que conozcas, indicando la responsabilidad de cada capa.**

_Respuesta:_

Sistema elegido: **sistema de punto de venta (POS) y gestión de ARX Parfums**, una aplicación web en PHP con MySQL que usa el comercio para registrar ventas en el local, controlar la caja y administrar ventas a cuotas.

```
┌──────────────────────────────────────────────────────────────┐
│ CAPA DE PRESENTACIÓN                                         │
│ Pantallas web (HTML, CSS, JavaScript): caja, nueva venta,    │
│ cobro de cuotas, productos, reportes, inicio de sesión.      │
└───────────────────────────┬──────────────────────────────────┘
                            │ formularios / peticiones HTTP
┌───────────────────────────▼──────────────────────────────────┐
│ CAPA DE LÓGICA DE NEGOCIO                                    │
│ Reglas del comercio: calcular totales y cuotas, apertura y   │
│ cierre de caja, anulación de ventas, validar stock,          │
│ controlar permisos y bloqueo de inicio de sesión.            │
└───────────────────────────┬──────────────────────────────────┘
                            │ llamadas a funciones de acceso
┌───────────────────────────▼──────────────────────────────────┐
│ CAPA DE ACCESO A DATOS                                       │
│ Consultas preparadas con PDO para leer y guardar ventas,     │
│ productos, clientes, cuotas y movimientos de caja.           │
└───────────────────────────┬──────────────────────────────────┘
                            │ SQL
┌───────────────────────────▼──────────────────────────────────┐
│ CAPA DE DATOS                                                │
│ Base de datos MySQL: tablas de productos, ventas, detalle,   │
│ clientes, cuotas, caja y usuarios.                           │
└──────────────────────────────────────────────────────────────┘
```

Cada capa solo usa los servicios de la capa inmediatamente inferior. Así, por ejemplo, se puede rediseñar la pantalla de caja sin tocar las reglas de cálculo de cuotas, o cambiar una consulta SQL sin afectar a la interfaz.

---

## Tema 6 · Estilos actuales y estrategia de selección

**12. Completa el siguiente cuadro comparativo.**

| Aspecto | Monolito modular | Microservicios |
|---|---|---|
| Despliegue | Se despliega como una sola unidad: un único paquete en un servidor. Cualquier cambio implica volver a desplegar toda la aplicación. | Cada servicio se despliega de forma independiente, en su propio proceso o contenedor; se puede actualizar uno sin tocar los demás. |
| Escalado | Se escala la aplicación completa (más instancias o un servidor más potente), aunque solo una parte tenga mucha demanda. | Se escala solo el servicio que lo necesita (ej. más instancias del servicio de pagos en un pico de ventas). |
| Complejidad operativa | Baja: un solo despliegue, una base de datos, llamadas internas, depuración y monitoreo simples. | Alta: muchos despliegues, comunicación por red, consistencia de datos distribuida, monitoreo, trazas, contenedores y orquestación. |
| ¿Cuándo conviene? | En equipos chicos o medianos, productos nuevos o dominios todavía cambiantes, y cuando se busca simplicidad y bajo costo. | En sistemas grandes con varios equipos autónomos, dominios bien conocidos, necesidades de escalado muy distintas por parte y una organización capaz de operar infraestructura compleja. |

**13. Una empresa nueva con tres desarrolladores quiere empezar su producto directamente con quince microservicios. ¿Qué le recomendarías y por qué?**

_Respuesta:_

Les recomendaría **empezar con un monolito modular** y no con quince microservicios, por estas razones:

1. **Tres personas no pueden operar quince servicios.** Cada servicio necesita despliegue, monitoreo, logs, base de datos y manejo de errores de red. El equipo pasaría más tiempo manteniendo infraestructura que construyendo el producto.
2. **El dominio todavía no está claro.** En un producto nuevo los requisitos cambian mucho; si los límites entre servicios se definen mal, corregirlos es muy costoso porque implica cambiar APIs y mover datos entre bases.
3. **Los microservicios resuelven problemas que todavía no tienen**: escalar partes de forma independiente o coordinar muchos equipos. Una empresa nueva todavía no necesita eso.
4. **Costo y velocidad:** un monolito se despliega en un solo servidor barato, se prueba y depura más rápido, y permite llegar antes al mercado.

La clave es diseñar el monolito con **módulos bien separados** (alta cohesión, bajo acoplamiento, cada módulo con sus propios datos). Así, si en el futuro alguna parte necesita escalar o crece el equipo, ese módulo se puede extraer como microservicio con poco esfuerzo.

**14. Para cada escenario, indica el atributo de calidad prioritario y un estilo arquitectónico que lo favorezca.**

| Escenario | Atributo prioritario | Estilo que lo favorece |
|---|---|---|
| Plataforma de venta de entradas con picos enormes de demanda al abrir la venta. | **Escalabilidad** y disponibilidad ante picos de carga. | **Microservicios** con escalado horizontal del servicio de compra, combinados con una arquitectura **orientada a eventos** (cola de espera para procesar los pedidos). |
| Sistema bancario de transferencias entre cuentas. | **Integridad/consistencia de los datos** y **seguridad**. | **Arquitectura en capas** sobre un **repositorio central (centrado en datos)** con transacciones ACID; la capa de negocio controla cada operación y la de seguridad, el acceso. |
| Sistema académico cuyas reglas de inscripción cambian cada semestre. | **Modificabilidad (mantenibilidad).** | **Arquitectura en capas** que concentra las reglas en la capa de negocio (o en un componente de reglas configurable), para cambiarlas sin tocar la interfaz ni los datos. |

---

## Tema 7 · Características de un buen diseño

**15. Menciona las tres directrices de calidad de Pressman para un buen diseño y explica una de ellas con un ejemplo propio.**

_Respuesta:_

Las tres directrices de calidad de Pressman para un buen diseño son:

* Debe implementar todos los requisitos explícitos: cumplir con lo que el cliente pidió.
* Debe ser legible y comprensible: facilitar que otros desarrolladores puedan entender el diseño.
* Debe proporcionar una visión completa del software: incluir los datos, las funciones y el comportamiento del sistema.

Ejemplo de la segunda directriz: en un sistema de biblioteca, organizar el código en módulos como gestión de libros, usuarios y préstamos permite que los desarrolladores comprendan fácilmente cada función y realicen modificaciones sin afectar todo el sistema.


**16. Ejercicio de relación**

| Síntoma | Número |
|---|---|
| A. Rigidez | **3** |
| B. Fragilidad | **4** |
| C. Inmovilidad | **2** |
| D. Repetición innecesaria | **1** |

---

## Tema 8 · Principios SOLID

**17. Completa el cuadro con el nombre de cada principio y lo que propone, en una oración.**

| Letra | Principio | ¿Qué propone? |
|---|---|---|
| S | Responsabilidad única (*Single Responsibility*) | Una clase debe tener una sola responsabilidad, es decir, un solo motivo para cambiar. |
| O | Abierto/cerrado (*Open/Closed*) | Las clases deben estar abiertas a la extensión pero cerradas a la modificación: se agrega comportamiento nuevo sin cambiar el código existente. |
| L | Sustitución de Liskov (*Liskov Substitution*) | Un objeto de una subclase debe poder reemplazar a uno de su clase base sin que el programa deje de funcionar correctamente. |
| I | Segregación de interfaces (*Interface Segregation*) | Es mejor tener varias interfaces pequeñas y específicas que una grande, para que ninguna clase dependa de métodos que no usa. |
| D | Inversión de dependencias (*Dependency Inversion*) | Los módulos de alto nivel no deben depender de módulos de bajo nivel, sino ambos de abstracciones (interfaces). |

**18. Analiza la siguiente clase: "ReporteVentas obtiene las ventas desde SQL Server, calcula los totales, arma un PDF y lo envía por correo". ¿Qué principio SOLID viola principalmente? Propone una mejor distribución de responsabilidades.**

_Respuesta:_

Viola principalmente el **Principio de Responsabilidad Única (S)**. La clase tiene cuatro motivos distintos para cambiar: si cambia la base de datos, si cambia la forma de calcular los totales, si cambia el formato del reporte (por ejemplo, Excel en vez de PDF) o si cambia el medio de envío (por ejemplo, WhatsApp en vez de correo). Además depende directamente de SQL Server, por lo que también incumple la **Inversión de dependencias (D)**.

Distribución propuesta:

| Clase / interfaz | Responsabilidad |
|---|---|
| `IVentaRepositorio` | Interfaz con el método `obtenerVentas(desde, hasta)`. |
| `VentaRepositorioSqlServer` | Implementa `IVentaRepositorio`: consulta las ventas en SQL Server. |
| `CalculadoraTotales` | Recibe la lista de ventas y calcula los totales (por día, por producto, total general). |
| `IGeneradorReporte` | Interfaz con el método `generar(datos)` que devuelve el archivo del reporte. |
| `GeneradorReportePdf` | Implementa `IGeneradorReporte`: arma el PDF. |
| `INotificador` | Interfaz con el método `enviar(destinatario, archivo)`. |
| `NotificadorCorreo` | Implementa `INotificador`: envía el archivo por correo electrónico. |
| `ServicioReporteVentas` | Coordina el proceso: pide las ventas al repositorio, calcula los totales, genera el reporte y lo envía. Depende solo de las interfaces, que recibe por constructor. |

Con esta distribución, cambiar de SQL Server a MySQL o de PDF a Excel solo implica crear una nueva implementación de la interfaz correspondiente, sin modificar el resto (también se cumple **Abierto/cerrado**).

---

## Tema 9 · Evaluación y validación del diseño

**19. Explica la diferencia entre una revisión técnica del diseño y una prueba del software. ¿Por qué conviene revisar el diseño antes de programar?**

_Respuesta:_

La revisión técnica del diseño consiste en analizar los planos y la estructura del sistema antes de programarlo, para detectar errores o problemas de organización. En cambio, una prueba del software consiste en ejecutar el programa para comprobar si funciona correctamente y cumple con los requisitos.

Conviene revisar el diseño antes de programar porque permite detectar errores desde el principio, evitar cambios costosos y ahorrar tiempo durante el desarrollo.

Ejemplo: en un sistema de biblioteca, revisar el diseño permite detectar que el módulo de préstamos no contempla las devoluciones. Si se descubre antes de programar, corregirlo será más sencillo y económico que modificar todo el sistema después.

**20. Completa la matriz de trazabilidad para un sistema de biblioteca.**

| Req. | Descripción | Elementos de diseño que lo satisfacen |
|---|---|---|
| RF-01 | Registrar el préstamo de un libro a un socio. | Pantalla **"Registrar préstamo"**; `PrestamoController`; `ServicioPrestamo.registrar(idSocio, idEjemplar)`, que valida la disponibilidad del ejemplar y el máximo de préstamos del socio; clases `Prestamo`, `Socio`, `Ejemplar`; `PrestamoRepositorio`; tabla `prestamo`. |
| RF-02 | Avisar por correo al socio cuando vence un préstamo. | Tarea programada **`VerificadorVencimientos`** (se ejecuta una vez al día); `PrestamoRepositorio.buscarVencidos(fecha)`; interfaz `INotificador` y su implementación `NotificadorCorreo`; plantilla de correo "Préstamo vencido". |
| RF-03 | Buscar libros por título, autor o tema. | Pantalla **"Buscar libros"** con campo de búsqueda y filtros; `CatalogoController`; `ServicioCatalogo.buscar(criterio)`; `LibroRepositorio.buscar(texto, tipo)`; índice de texto completo sobre título, autor y tema en la tabla `libro`. |
| RNF-01 | Solo el personal de la biblioteca puede registrar préstamos. | Módulo de **autenticación** (inicio de sesión); clases `Usuario` y `Rol`; **middleware de autorización** que exige el rol "Bibliotecario" en las rutas de `PrestamoController`; la pantalla "Registrar préstamo" se muestra solo a ese rol. |

---

## Tema 10 · Diseño de la interfaz de usuario

**21. Para cada regla de oro, da un ejemplo de una aplicación o sitio que la cumpla y otro que la viole.**

| Regla de oro | Ejemplo que la cumple | Ejemplo que la viola |
|---|---|---|
| Dar el control al usuario | **Gmail**: después de enviar un correo muestra "Deshacer" durante unos segundos, y permite cancelar el envío. | Sitios de noticias que reproducen videos con sonido automáticamente y sin un botón visible para pausarlos o cerrarlos. |
| Reducir la carga de memoria | **Buscador de Google**: autocompleta la búsqueda y recuerda búsquedas anteriores; **Mercado Libre** guarda la dirección de envío para no tener que escribirla de nuevo. | Formularios de trámites que en un paso piden escribir un número (de expediente o de pedido) que solo se mostró en una pantalla anterior, obligando al usuario a anotarlo. |
| Lograr una interfaz consistente | **Microsoft Word, Excel y PowerPoint**: comparten la misma cinta de opciones, los mismos íconos y atajos (Ctrl+S, Ctrl+Z), por lo que lo aprendido en uno sirve en los otros. | Sistemas en los que el botón "Guardar" cambia de lugar, de color o de nombre ("Aceptar", "Confirmar", "OK") según la pantalla. |

**22. Realiza el análisis previo al diseño de la interfaz para la aplicación de autogestión de alumnos de la universidad.**

| Aspecto | Descripción |
|---|---|
| Usuarios | **Alumnos de grado** de distintas carreras, de aproximadamente 18 a 35 años. La mayoría usa el celular a diario y tiene un manejo de tecnología de medio a alto. Muchos trabajan y estudian, por lo que usan el sistema en ratos cortos. Hay alumnos de primer año que no conocen los términos administrativos (correlatividad, regularidad, mesa de examen). Usuarios secundarios: personal de **secretaría académica**, que consulta y corrige datos de los alumnos. |
| Tareas principales | Inscribirse a materias y a exámenes finales; consultar notas, asistencias e historial académico; ver horarios y aulas; consultar el estado de cuenta y pagar aranceles; descargar constancias (alumno regular, certificado de notas); recibir avisos de la facultad. Las más frecuentes y críticas son **inscribirse** y **consultar notas**. |
| Entorno de uso | Mayormente desde el **celular**, con datos móviles o el wifi de la facultad, en pasillos, en el colectivo o en el trabajo, a veces con luz solar directa y conexión inestable. También desde computadoras en casa o en la biblioteca. Hay **picos de uso** al abrir las inscripciones y al publicar notas, en los que muchos alumnos entran a la vez y bajo presión de tiempo (cupos limitados). |

---

## Tema 11 · Usabilidad, accesibilidad y prototipos

**23. Evaluación heurística: elijan una pantalla real, agreguen una captura al repositorio e identifiquen al menos tres problemas de usabilidad o accesibilidad.**

Pantalla evaluada: **inicio de sesión e inscripción a exámenes del sistema de autogestión de alumnos de la facultad**.

![Captura de la pantalla evaluada](captura-evaluacion-heuristica.png)

| Problema detectado | Heurística de Nielsen violada | Mejora propuesta |
|---|---|---|
| Al ingresar una contraseña incorrecta, la página se recarga y aparece un mensaje genérico ("Error") sin indicar qué falló, y el campo de usuario se borra. | **Ayudar a reconocer, diagnosticar y recuperarse de errores** (#9). | Mostrar un mensaje claro junto al campo ("Usuario o contraseña incorrectos") y conservar el usuario ya escrito. |
| Después de presionar "Inscribirme" no hay ninguna confirmación visible ni indicador de carga; el alumno no sabe si quedó inscripto y vuelve a presionar el botón. | **Visibilidad del estado del sistema** (#1). | Mostrar un indicador de "Procesando…", desactivar el botón mientras tanto y luego un mensaje "Inscripción confirmada" con la materia, la fecha y un número de comprobante. |
| No hay forma de cancelar una inscripción desde la misma pantalla; hay que ir a otro menú. | **Control y libertad del usuario** (#3). | Agregar un botón "Anular inscripción" en cada examen inscripto, con confirmación. |
| Los textos son grises claros sobre fondo blanco y la tabla no se adapta al celular (hay que hacer zoom y desplazarse de costado). | **Accesibilidad**: contraste y diseño adaptable; también **diseño estético y minimalista** (#8). | Aumentar el contraste (mínimo 4,5:1 según WCAG) y mostrar los exámenes como tarjetas en pantallas pequeñas. |

> ⚠️ **Antes de entregar:** reemplacen la captura `captura-evaluacion-heuristica.png` por una imagen real de la pantalla que elijan y ajusten los problemas de la tabla a lo que efectivamente se ve en esa captura.

**24. Elijan una pantalla clave del sistema de su Trabajo Práctico y dibujen su wireframe. Indiquen qué regla de oro o heurística tuvieron en cuenta en al menos dos decisiones.**

_Respuesta:_

Pantalla elegida: **P-04 · Confirmar pedido (checkout)** de **ARX Store**, el sistema web de comercio electrónico de ARX Parfums. Corresponde al caso de uso CU-08 "Realizar pedido" y la usa el actor Cliente registrado.

![Wireframe de la pantalla Confirmar pedido de ARX Store](wireframe-checkout.png)

Decisiones de diseño y la regla o heurística aplicada:

1. **Indicador de pasos "① Carrito → ② Entrega → ③ Pago → ④ Confirmación"** en la parte superior. Heurística **Visibilidad del estado del sistema**: el cliente sabe en qué paso está y cuántos faltan para terminar la compra.
2. **Resumen del pedido siempre visible a la derecha** (productos, cantidades y total en guaraníes) mientras el cliente elige la entrega y el pago. Regla de oro **Reducir la carga de memoria** (y heurística *reconocer antes que recordar*): no tiene que volver al carrito para recordar qué está comprando ni cuánto va a pagar.
3. **Opciones de entrega y pago como botones de opción con un valor ya seleccionado** (la dirección guardada y la transferencia). Heurística **Prevención de errores**: el cliente no puede confirmar un pedido sin método de entrega o de pago, y no necesita volver a escribir la dirección.
4. **El comprobante de pago es opcional en esta pantalla**, porque también se puede subir después desde "Mis pedidos". Regla de oro **Dar el control al usuario**: si en ese momento no tiene el comprobante a mano, igual puede confirmar el pedido.
5. **Un único botón principal "Confirmar pedido"**, con el mismo estilo que los botones principales del resto del sitio ("Agregar al carrito", "Continuar con el pedido"). Regla de oro **Lograr una interfaz consistente**.

**25. Reflexión final: ¿qué estilo arquitectónico proponen para el sistema de su Trabajo Práctico y por qué? Justifiquen la elección con al menos dos atributos de calidad del sistema.**

_Respuesta:_

Para **ARX Store** proponemos un **monolito modular con arquitectura en capas**, organizado internamente con el patrón **Modelo-Vista-Controlador (MVC)** que ofrece Laravel. Funciona como una aplicación **cliente-servidor web**: el navegador del cliente se conecta al servidor de la aplicación, que a su vez usa la misma base de datos MySQL del POS del local.

- **Capa de presentación:** vistas Blade de la tienda y del panel de administración.
- **Capa de negocio:** controladores y servicios (pedidos, stock, pagos, notificaciones), donde se aplican las reglas del negocio como RN-01 (stock disponible) y RN-04 (estados del pedido).
- **Capa de acceso a datos:** modelos Eloquent y repositorios sobre MySQL.

Justificación con atributos de calidad:

1. **Integridad y consistencia de los datos.** El problema principal del cliente es vender productos sin stock. Al tener una sola aplicación y una sola base de datos compartida con el POS, la reserva y el descuento de stock se hacen dentro de una **transacción**, sin datos duplicados ni sincronizaciones entre servicios. Así se cumple RNF-12 (la venta del POS se refleja en la tienda en 5 segundos o menos).
2. **Mantenibilidad (modificabilidad).** La separación en capas y en MVC permite cambiar una parte sin afectar a las otras. Por ejemplo, se puede rediseñar la pantalla del catálogo sin tocar las reglas de stock, o agregar más adelante una pasarela de pago con tarjeta como un nuevo módulo de pagos.
3. **Costo y simplicidad de operación.** Somos un equipo de cuatro estudiantes y el cliente es un comercio pequeño. Un monolito se despliega en un único hosting compartido o VPS de bajo costo, es fácil de probar y de mantener, y cumple sin problemas el volumen previsto (RNF-13: 200 pedidos diarios). Descartamos los microservicios porque agregarían complejidad operativa que ni el equipo ni el cliente necesitan.
4. **Rendimiento suficiente.** Con consultas indexadas y caché de las páginas del catálogo, una sola aplicación alcanza los tiempos pedidos (RNF-01: catálogo en 3 segundos o menos). Si en el futuro el tráfico creciera, se pueden agregar más instancias del mismo monolito detrás de un balanceador.
