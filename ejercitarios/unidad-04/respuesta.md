# Respuestas — Ejercitario Unidad 04

---

## Tema 1 · El proceso de requerimientos

**1. Define en tus propias palabras qué es la ingeniería de requerimientos.**

La ingeniería de requerimientos es el conjunto de actividades que se hacen para descubrir, entender, documentar y gestionar qué es lo que el software tiene que hacer y qué condiciones debe cumplir, antes y durante su desarrollo.


**2. Explica la diferencia entre "requerimiento", "especificación de requisitos" e "ingeniería de requisitos", con un ejemplo de cada uno.**

_Respuesta:_
1.Requerimiento: Es una necesidad, condición o capacidad individual que el sistema debe cumplir o poseer para satisfacer un problema del cliente.

Ejemplo: "El usuario debe poder iniciar sesión con su correo electrónico y contraseña."

2.Especificación de requisitos: Es el documento formal o conjunto de modelos (como el ERS/SRS) donde se recopilan, estructuran y detallan todos los requerimientos de un proyecto.

Ejemplo: Un documento PDF estructurado bajo el estándar IEEE 830 que incluye la arquitectura conceptual, los casos de uso descritos y la lista de requerimientos del sistema.

3.Ingeniería de requisitos: Es la disciplina/área de la ingeniería de software que agrupa los procesos, técnicas y herramientas utilizadas para elicitar, analizar, especificar, validar y administrar dichos requerimientos a lo largo del ciclo de vida.

Ejemplo: El conjunto de actividades realizadas por el equipo analista durante las primeras 3 semanas del proyecto, que incluyó entrevistas con el cliente, diseño de prototipos y reuniones de negociación.


---

## Tema 2 · Tipos de requerimientos

**3. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Tipo de requerimiento | Descripción |
|---|---|
| A. Funcional | __Describe una función o servicio concreto que el sistema debe realizar.__ |
| B. No funcional | __Restringe cómo debe comportarse el sistema (desempeño, seguridad, usabilidad, etc.)__ |
| C. Del dominio | __Proviene de las reglas o restricciones propias del área o dominio de negocio.__ |

1. Proviene de las reglas o restricciones propias del área o dominio de negocio.
2. Describe una función o servicio concreto que el sistema debe realizar.
3. Restringe cómo debe comportarse el sistema (desempeño, seguridad, usabilidad, etc.).

**4. Completen el siguiente cuadro comparando los requerimientos de usuario y los requerimientos de sistema.**

| Aspecto | Requerimientos de usuario | Requerimientos de sistema |
|---|---|---|
| Audiencia principal | Clientes, usuarios finales, gerentes del negocio y patrocinadores.|Desarrolladores, arquitectos de software, evaluadores (QA) y gestores técnicos. |
| Nivel de detalle | Alto nivel; abstracto, general y enfocado en la necesidad del negocio.	|Detallado; técnico, preciso e indicando el comportamiento explícito del software.| 
| Lenguaje utilizado |Lenguaje natural sencillo, diagramas simples e historias de usuario (sin jerga técnica).	|Lenguaje estructurado, modelos UML, especificaciones técnicas y notación formal. | 

**5. Elegí un sistema que conozcas (una app, una plataforma, un sistema de tu universidad o trabajo) y da un ejemplo propio de un requerimiento funcional y uno no funcional para ese mismo sistema.**

_Respuesta:_
*Sistema seleccionado: Plataforma web de Spotify.

*Requerimiento Funcional (RF): El sistema debe permitir a los usuarios crear y organizar listas de reproducción (playlists) personalizadas agregando o quitando canciones.

*Requerimiento No Funcional (RNF): El reproductor de audio debe iniciar la reproducción de la canción seleccionada en un tiempo menor a 1,5 segundos en conexiones de al menos 10 Mbps.


---

## Tema 3 · Características de los requerimientos

**6. Completen el siguiente cuadro indicando qué pregunta permite verificar cada característica de un buen requerimiento.**

| Característica | Pregunta que permite verificarla |
|---|---|
| Correcto | ¿El requerimiento refleja exactamente una necesidad real expresada por el cliente sin errores ni distorsiones?|
| No ambiguo |¿Tiene una sola y única interpretación posible para cualquier persona que lo lea (desarrollador, usuario, QA)? |
| Completo | ¿Contiene toda la información necesaria para implementarlo, incluyendo condiciones, entradas y salidas, sin dejar cabos sueltos?|
| Verificable | ¿Existe una prueba cuantitativa o un caso de prueba concreto que permita comprobar de manera objetiva si se cumplió o no?|

**7. Tomá el requerimiento "El sistema debe ser rápido" y reescribilo de forma que cumpla con las características de un buen requerimiento vistas en clase.**

_Respuesta:_
Versión corregida (Verificable e Inambigua): "El tiempo de respuesta del sistema para procesar y mostrar el resultado de una búsqueda en el catálogo debe ser inferior a 2 segundos bajo una carga simultánea de hasta 500 usuarios concurrentes."


---

## Tema 4 · Obtención y análisis de requerimientos

**8. Enumera las cuatro etapas del ciclo de obtención y análisis de requerimientos vistas en clase.**

1- Descubrimiento de requerimiento
2- Clasificacion y organizacion de requerimientos
3- Priorizacion y negociacion de requerimientos
4- Especificacion


**9. Ejercicio de relación** (completen con el número que corresponda a cada letra):

| Técnica de obtención | Situación en que conviene usarla |
|---|---|
| A. Entrevistas | _3__ |
| B. Observación | __1_ |
| C. Talleres / workshops | _2__ |

1. Cuando el usuario no puede verbalizar fácilmente lo que necesita.
2. Cuando hay varios interesados con visiones distintas que negociar.
3. Cuando se quiere profundizar con un interesado en particular.

---

## Tema 5 · Técnicas de especificación de requerimientos

**10. Completen el siguiente cuadro indicando una ventaja y una limitación de cada técnica de especificación de requerimientos.**

| Técnica | Ventaja | Limitación |
|---|---|---|
| Lenguaje natural estructurado |Fácil de leer para cualquiera y más ordenado que el texto libre | Aún puede ser ambiguo y se vuelve extenso |
| Casos de uso |Muestran la interacción usuario-sistema paso a paso | Poco útiles para requerimientos no funcionales |
| Historias de usuario | Breves, centradas en el valor y fáciles de priorizar | Poco detalle; requieren conversación y criterios de aceptación |
| Diagramas (UML) | Dan una visión clara y compacta de estructura y comportamiento | Requieren conocer la notación; el cliente puede no entenderlos |

---

## Tema 6 · Especificaciones formales

**11. ¿Qué es una especificación formal y en qué tipo de sistemas se justifica su uso? Da un ejemplo hipotético de un sistema donde la usarías.**

_Respuesta:_
¿Qué es?: Es una descripción matemática y rigurosa del comportamiento del software utilizando notación lógica formal (como Notación Z o VDM) para eliminar cualquier tipo de ambigüedad.

¿En qué sistemas se justifica su uso?: En sistemas críticos (safety-critical o mission-critical) donde un error de especificación puede causar pérdidas humanas, catástrofes ambientales o grandes pérdidas financieras.

Ejemplo hipotético: El sistema de control de piloto automático y navegación de un avión comercial de pasajeros.


---

## Tema 7 · Prototipado de los requerimientos

**12. Explica la diferencia entre un prototipo desechable y un prototipo evolutivo, con un ejemplo de un proyecto donde usarías cada uno.**

_Respuesta:_
1.Prototipo desechable (Throwaway): Se construye de forma rápida y económica para explorar o aclarar requisitos ambiguos con el usuario, y luego se descarta totalmente (no se usa para el sistema final).

Ejemplo: Maquetas en papel o mockups interactivos creados en Figma para validar con un grupo de médicos cómo prefieren ver los datos en la pantalla de una clínica.

2.Prototipo evolutivo: Se desarrolla una versión inicial limpia y funcional del software que cumple con los requisitos mejor comprendidos; este prototipo no se desecha, sino que se refina y amplía progresivamente hasta convertirse en el producto final.

Ejemplo: El desarrollo del producto mínimo viable (MVP) de una tienda e-commerce donde la base del código inicial se conserva y sobre ella se agregan pasarelas de pago y módulos de inventario en entregas sucesivas.


---

## Tema 8 · Técnicas de construcción rápida

**13. Menciona dos técnicas de construcción rápida de prototipos vistas en clase y explica brevemente en qué consiste cada una.**

_Respuesta:_
1.Modelado visual mediante maquetadores UI / Herramientas de prototipado (Mockups/Wireframing): Uso de herramientas de diseño interactivo (ej. Figma, Balsamiq) que permiten crear interfaces de usuario navegables a partir de componentes preconstruidos, sin escribir código de backend.

2.Desarrollo impulsado por bases de datos / Plataformas Low-Code: Uso de frameworks o plataformas que generan automáticamente formularios web, tablas de datos e interfaces CRUD a partir del diseño básico del esquema de datos.

---

## Tema 9 · Validación de requerimientos

**14. Completen el siguiente cuadro relacionando cada técnica de validación con el tipo de problema que detecta mejor.**

| Técnica de validación | Qué tipo de problema detecta mejor |
|---|---|
| Revisiones de requisitos | Qué tipo de problema detecta mejor|
| Prototipado |Malos entendidos en la experiencia de usuario (UX), flujos de trabajo ilógicos y requisitos no funcionales de usabilidad. |
| Generación de casos de prueba |Requerimientos imposibles de verificar, inconsistencias lógicas en reglas de negocio y falta de detalle en escenarios límite (edge cases). |

---

## Tema 10 · Administración de requerimientos

**15. Explica con tus palabras qué es la trazabilidad de requerimientos y por qué es importante en un proyecto real.**

La trazabilidad de requerimientos es la capacidad de seguirle el rastro a cada requerimiento a lo largo de todo el proyecto: saber de dónde salió (quién lo pidió y por qué), en qué parte del diseño y del código se convirtió, y con qué pruebas se verifica que se cumplió.


---

## Tema 11 · Medición de requerimientos

**16. Menciona dos métricas que se pueden aplicar a los requerimientos de un proyecto y qué información le aporta cada una al equipo.**

_Respuesta:_
Es una descripción del comportamiento del sistema escrita en un lenguaje con sintaxis y semántica matemáticas precisas (por ejemplo Z, B o VDM). Al no tener ambigüedades, permite razonar sobre los requerimientos y demostrar que el diseño y el código los cumplen.

Se justifica en sistemas críticos, donde un error puede costar vidas o mucho dinero: aviación, equipos médicos, control ferroviario, sistemas nucleares o financieros. Es costosa y requiere personal especializado, así que no conviene en sistemas comunes.

Ejemplo: el software de control de una bomba de infusión de medicamentos. Formalmente se puede especificar que la dosis nunca supere el máximo configurado y que la bomba se detenga ante una falla, y verificar esas propiedades antes de programar.

**17. Reflexión final:** pensá en un proyecto de software (hipotético o real). Describí qué técnica de obtención, qué técnica de especificación y qué técnica de validación usarías para sus requerimientos, y justificá tu elección considerando el tipo de proyecto y de usuarios.

_Respuesta:_
Supongamos una app móvil de turnos para una clínica, usada por pacientes de todas las edades y por personal administrativo.
Obtención: entrevistas y observación. Con el personal administrativo hago entrevistas. Con los pacientes, muchos poco familiarizados con la tecnología, observo cómo sacan turnos hoy, porque suelen no saber explicar lo que necesitan.
Especificación: historias de usuario con criterios de aceptación. Son simples, comprensibles para usuarios no técnicos y se adaptan bien a cambios, algo esperable en una app con muchos tipos de usuarios. Para flujos críticos, como la cancelación de turnos, sumaría algún caso de uso.
Validación: prototipos y revisiones con usuarios reales. Un prototipo navegable permite que los pacientes prueben el flujo antes de programar. Así se detectan errores de comprensión temprano, cuando corregirlos es barato.


