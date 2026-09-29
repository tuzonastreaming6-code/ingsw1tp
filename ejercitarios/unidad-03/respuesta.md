# Respuestas — Ejercitario Unidad 03

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · El significado de proceso

**1. Define en tus propias palabras qué es un proceso de software.**

Un proceso de software es el conjunto ordenado de actividades, pasos y tareas que se siguen para desarrollar un producto de software, desde que surge la idea o la necesidad hasta que el programa está terminado, funcionando y en mantenimiento.


**2. Explica la diferencia entre proceso, metodología y modelo de proceso, con un ejemplo de cada uno.**
2.1- Proceso de software:Es el conjunto de actividades que se realizan para producir software, entender requisitos, diseñar, programar, probar, mantener.
Ejemplo: El proceso general de desarrollar un sistema, que incluye las actividades de análisis, diseño, codificación y pruebas.

2.2- Modelo de proceso: Es una forma de organizar y ordenar las actividades del proceso. Define en qué secuencia y de qué manera se combinan esas etapas, es una representación abstracta del proceso. Ej: El modelo en cascada las etapas van una tras otra, en orden fijo,  el modelo incremental o el modelo espiral. Cada uno propone una estructura distinta para las mismas actividades 

2.3- Metodología: Es un conjunto de reglas, técnicas, roles, herramientas y buenas prácticas específicas que dicen "cómo hacer" el trabajo en el día a día. ej : Scrum (con sus roles como Scrum Master, sus sprints, sus reuniones diarias) o XP (Programación Extrema). Son metodologías ágiles que definen prácticas puntuales de trabajo.


**3. Enumera las cinco actividades genéricas del marco de trabajo de Pressman.**
1- Comunicacion
2- Planeacion
3- Modelado
4- Construccion
5- Despliegue



**4. Menciona dos actividades "de la sombrilla" y explica por qué se dice que "cubren" todo el proceso.**

_Respuesta:_
1.Seguimiento y control del proyecto de software: Permite evaluar el progreso frente al plan y aplicar medidas correctivas si hay desviaciones.

2.Garantía de calidad del software (SQA): Actividades para asegurar que los productos entregados cumplan con los estándares de calidad requeridos.

¿Por qué "cubren" todo el proceso? Se las llama actividades sombrilla (umbrella activities) porque no pertenecen a una fase específica o secuencial, sino que se ejecutan de manera horizontal y continua desde el inicio hasta el final de cualquier proyecto.


---

## Tema 2 · Modelos de proceso

**5. Completen el siguiente cuadro indicando en qué situación conviene usar cada modelo de proceso visto en clase.**

| Modelo | ¿Cuándo conviene usarlo? |
|---|---|
| Cascada | Cuando los requisitos están perfectamente definidos, son estables y no van a cambiar durante el desarrollo; además el dominio de la tecnología es alto.|
| Incremental | Cuando se necesita entregar un producto funcional al cliente en poco tiempo y se planea ir añadiendo funcionalidades en entregas sucesivas.|
| Evolutivo (prototipos) |  Cuando los requisitos son difusos o poco claros y el cliente necesita interactuar con una versión preliminar para entender y definir lo que realmente necesita.|
| Evolutivo (espiral) | En proyectos de gran tamaño, complejos y de alto riesgo donde se requiere un análisis explícito y formal de riesgos en cada iteración.|
| Concurrente | En proyectos donde diferentes equipos trabajan simultáneamente sobre distintas partes del sistema y cada módulo se encuentra en un estado de desarrollo diferente.|

**6. Ejercicio de relación** (completá con el número que corresponda a cada letra):

| Modelo de proceso | Característica principal |
|---|---|
| A. Cascada | ___ |
| B. Incremental | ___ |
| C. Prototipos | ___ |
| D. Espiral | _Combina iteración con análisis explícito de riesgo en cada vuelta.__ |
| E. Concurrente | ___ |

1. Combina iteración con análisis explícito de riesgo en cada vuelta.
2. Enfoque secuencial y lineal, actividad por actividad.
3. Representa actividades ocurriendo en paralelo, no en secuencia estricta.
4. Entrega el producto en porciones funcionales cada vez más completas.
5. Construye una versión parcial y rápida para validar requisitos poco claros.

**7. Elegí un proyecto de software (hipotético o real) y justificá qué modelo de proceso usarías para desarrollarlo y por qué.**

_Respuesta:_
Proyecto: Desarrollo de una aplicación móvil para la gestión y reserva de turnos en una cadena de barberías.

Modelo elegido: Modelo Incremental.

Justificación: Permite lanzar rápidamente una primera versión operativa (Incr. 1: registro de usuarios y agenda básica de turnos) para que el negocio empiece a operarla de inmediato. Luego, mediante nuevos incrementos, se pueden sumar funciones más complejas (Incr. 2: pagos en línea, Incr. 3: programa de fidelización y notificaciones), reduciendo el tiempo de salida al mercado (Time-to-Market) y absorbiendo retroalimentación real del usuario sin detener la operación.

---

## Tema 3 · Iteración de procesos

**8. Explica con tus palabras por qué la mayoría de los procesos modernos son iterativos.**

_Respuesta:_
Porque en la práctica los requisitos rara vez son fijos o totalmente claros desde el principio. La tecnología evoluciona rápido y las necesidades del cliente o del negocio cambian con frecuencia. Un proceso iterativo permite validar entregas parciales constantemente con los usuarios, aprender del feedback y corregir el rumbo a bajo costo antes de que sea demasiado tarde.


**9. Menciona una ventaja y una desventaja de trabajar con iteraciones cortas.**

_Respuesta:_
Ventaja: Permite obtener retroalimentación rápida del usuario final y detectar errores o desviaciones de diseño tempranamente, disminuyendo el costo del cambio.

Desventaja: Puede generar sobrecarga administrativa (overhead) por la alta frecuencia de reuniones, planificación, pruebas e integraciones constantes si el equipo no cuenta con automatización adecuada.


---

## Tema 4 · Especificación, diseño, implementación, validación y evolución

**10. Describan brevemente qué implica cada una de las cuatro actividades fundamentales del proceso de software, según Sommerville.**

| Actividad | Qué implica |
|---|---|
| Especificación | |
| Diseño e implementación | |
| Validación | |
| Evolución | |

**11. Relaciona estas cuatro actividades con las cinco fases del ciclo del software vistas en la Unidad 1 (análisis, diseño, implementación, pruebas, mantenimiento). ¿En qué se parecen y en qué se diferencian?**

_Respuesta:_


---

## Tema 5 · Herramientas y técnicas para modelado de procesos

**12. Menciona dos formas de representar un proceso (no un sistema) y explica brevemente cada una.**

_Respuesta:_
1.Diagramas de Flujo de Datos / Diagramas de Actividad (UML): Representación gráfica que utiliza símbolos normalizados para ilustrar la secuencia lógica de pasos, decisiones, entradas, salidas y el flujo de trabajo dentro del proceso.

2.Representación en Lenguaje Natural Estructurado (o PSDL - Process Software Description Language): Uso de plantillas textuales con palabras clave estructuradas (ej. Premisas, Entradas, Pasos, Salidas, Roles involucrados) que describen de forma precisa cada paso sin margen a interpretaciones ambiguas.


**13. ¿Qué es un patrón de proceso? Da un ejemplo hipotético de un problema recurrente en un proyecto y su solución.**

_Respuesta:_


---

## Tema 6 · Ayuda automatizada al proceso

**14. Explica la diferencia entre herramientas Upper-CASE y Lower-CASE.**

_Respuesta:_


**15. Menciona tres herramientas que consideren CASE (de su propia experiencia o investigación) y clasifíquenlas según la categoría a la que pertenecen.**

| Herramienta | Categoría (Upper / Lower / I-CASE) |
|---|---|
| | |
| | |
| | |

**16. Reflexión final:** de los modelos de proceso vistos en esta unidad, ¿cuál elegirían para un proyecto personal? Justifiquen su elección considerando el tamaño del proyecto, el tiempo disponible y el nivel de certeza sobre los requisitos.

_Respuesta:_

