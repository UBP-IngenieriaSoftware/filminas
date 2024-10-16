---
title: Diseño e Implementación
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Diseño e Implementación
Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

---
<!-- .slide: style="font-size: 0.60em" -->
<style>
.grid-container2 {
    display: grid;
    grid-template-columns: auto auto;
    font-size: 0.8em;
    text-align: left !important;
}

.grid-item {
    border: 3px solid rgba(121, 177, 217, 0.8);
    padding: 20px;
    text-align: left !important;
}
</style>
## Temario
<div class="grid-container2">
<div class="grid-item">

### Diseño e implementación
* Definición
* Construir o Comprar
* Proceso de Diseño
* Estapas del Proceso
* Contexto del Sistema
* Modelo de Contexto
* Diseño Arquitetcónico
* Identificación de las clases
* Aproximacione spara la Identificación
* Patrones de Diseño
</div>
<div class="grid-item">

* Elementos del Patrón
* Patrón Observador
* Implementación del Software
* Reutilización
* Niveles de Reutilización
* Costos de Reutilización
* Gestión de la Configuración
* Actividades de Gestión de Configuración
* Desarrollo Huesped - Objetivo
* Herramientas de Desarrollo
* Entorno de Desarrollo Integrado
* Desarrollo de Código Abierto
</div>
</div>

---
### Diseño e implementación
<!-- .slide: style="font-size: 0.90em" -->
* El diseño de software y la implementación es la etapa en el proceso de ingeniería de software en el que se
desarrolla un sistema de software ejecutable.
* Las actividades de diseño e implementación de software son invariablemente entrelazadas.
* El diseño de software es una actividad creativa en la que se identifica los componentes de software y sus relaciones,
sobre la base de los requisitos del cliente.
* La implementación es el proceso de realización del diseño como un programa.

---
### Construir o comprar
<!-- .slide: style="font-size: 0.80em" -->
* En una amplia gama de dominios, ahora es posible comprar sistemas **Comerciales off-the-shelf** (COTS) que pueden ser
adaptados y orientados a los deseos de los usuarios.
* Por ejemplo, si desea implementar un sistema de registros médicos, es posible comprar un paquete que ya se utiliza
en los hospitales. Puede ser más barato y más rápido para utilizar este enfoque en lugar de desarrollar un sistema en
un lenguaje de programación convencional.
* Cuando se desarrolla una aplicación de esta forma, el proceso de diseño se preocupa con el uso de las funciones
de configuración de ese sistema para entregar los requisitos del sistema.

----

### COTS: Ventajas
* Gran comunidad de soporte técnico proporciona ayuda y resuelve dudas.
* Fácil de obtener
* Tiene un costo único
* El sistema es flexible y puede ser reemplazado si falla.
* Fácil de implementar.
* Tiene actualizaciones regulares.
* Es confiable
* Suele tener pruebas gratuitas
<!--https://dazzet.co/que-es/commercial-off-the-shelf-software/-->

----

### COTS: Desventajas
- El vendedor puede dejar de brindar soporte
- El software no es tan personalizable.
- Alto costo a largo plazo si requiere de licencia periódica.
- Hay mayor riesgo de seguridad.

---
### Un proceso de diseño orientado a objetos
* Procesos de diseño orientados a objetos suponen el desarrollo de una serie de diferentes modelos de sistemas.
* Ellos requieren un gran esfuerzo para el desarrollo y el mantenimiento de estos modelos y, para sistemas
pequeños, esto puede no ser rentable.
* Sin embargo, para los grandes sistemas desarrollados por diferentes modelos de diseño de grupos son un
mecanismo de comunicación importante.

---
### Etapas del proceso
Hay una variedad de diferentes procesos de diseño orientados a objetos que dependen de la organización que
utilice el proceso.

Las actividades comunes en estos procesos incluyen:
* Definir el contexto y los modos de uso del sistema;
* Diseñar la arquitectura del sistema;
* Identificar los principales objetos del sistema;
* Desarrollar modelos de diseño;
* Especificar las interfaces de objetos.

---
### Contexto del sistema y las interacciones
<!-- .slide: style="font-size: 0.90em" -->
* La comprensión de las relaciones entre el software que se está diseñando y su entorno externo es esencial para
decidir la manera de proporcionar la funcionalidad requerida del sistema y cómo estructurar el sistema para
comunicarse con su entorno.
* La comprensión del contexto también permite establecer los límites del sistema. El ajuste de los límites del sistema
ayuda a decidir qué características se implementan en el sistema que está siendo diseñado y qué características se
encuentran en otros sistemas asociados.

---
### Los modelos de contexto e interacción
* Un **modelo de contexto** del sistema es un modelo estructural que demuestra los otros sistemas en el entorno
del sistema en desarrollo.
* Un **modelo de interacción** es un modelo dinámico que muestra cómo el sistema interactúa con su entorno
mientras es utilizado.

---
### Contexto del sistema para la estación meteorológica

![Estacion Metereológica](images/unidad7/estacion-metereologica.jpg)

---
### Casos de uso de la Estación meteorológica

![Casos de Uso de Estación Metereológica](images/unidad7/caso-uso-estacion-metereologica.jpg)

---
### Descripción de caso de uso-Informe meteorológico
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Caso de uso  | Reportar clima                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actores      | Sistema de información meteorológica, Estación meteorológica                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Descripción  | La estación meteorológica envía un resumen de los datos meteorológicos que se ha recogido de los instrumentos en el período de recolección para el sistema de información sobre el clima. Los datos enviados son el máximo, el mínimo, y una temperatura media de tierra y aire; máximo, mínimo y promedio de las presiones de aire; el máximo, el mínimo, y la velocidad media del viento; la precipitación total; y la dirección del viento como un muestreo a intervalos de cinco minutos. |
| Estimulo     | El sistema de información del clima establece un enlace de comunicación por satélite con la estación meteorológica y solicita la transmisión de datos.                                                                                                                                                                                                                                                                                                                                        |
| Respuesta    | El resumen de datos se envía al sistema de información sobre el clima.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Comentarios  | Las estaciones meteorológicas por lo general se les pide reportar una vez por hora, pero esta frecuencia puede variar de una estación a otra y pueden ser modificados en el futuro.                                                                                                                                                                                                                                                                                                           |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Caso de uso</th>
<th style="text-align:left">Reportar clima</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Actores</td>
<td style="text-align:left">Sistema de información meteorológica, Estación meteorológica</td>
</tr>
<tr>
<td style="text-align:left">Descripción</td>
<td style="text-align:left">La estación meteorológica envía un resumen de los datos meteorológicos que se ha recogido de los instrumentos en el período de recolección para el sistema de información sobre el clima. Los datos enviados son el máximo, el mínimo, y una temperatura media de tierra y aire; máximo, mínimo y promedio de las presiones de aire; el máximo, el mínimo, y la velocidad media del viento; la precipitación total; y la dirección del viento como un muestreo a intervalos de cinco minutos.</td>
</tr>
<tr>
<td style="text-align:left">Estimulo</td>
<td style="text-align:left">El sistema de información del clima establece un enlace de comunicación por satélite con la estación meteorológica y solicita la transmisión de datos.</td>
</tr>
<tr>
<td style="text-align:left">Respuesta</td>
<td style="text-align:left">El resumen de datos se envía al sistema de información sobre el clima.</td>
</tr>
<tr>
<td style="text-align:left">Comentarios</td>
<td style="text-align:left">Las estaciones meteorológicas por lo general se les pide reportar una vez por hora, pero esta frecuencia puede variar de una estación a otra y pueden ser modificados en el futuro.</td>
</tr>
</tbody>
</table>


---
### Diseño arquitectónico
<!-- .slide: style="font-size: 0.90em" -->
* Una vez que se han entendido las interacciones entre el  sistema y su entorno, se utiliza esta información para el
diseño de la arquitectura del sistema.
* Se identifican los principales componentes que conforman el sistema y sus interacciones, y luego puede organizar los
componentes utilizando un patrón arquitectónico, como un modelo en capas o cliente-servidor.
* La estación meteorológica se compone de subsistemas independientes que se comunican mediante la difusión de
mensajes sobre una infraestructura común.

---
### Arquitectura de alto nivel de la estación meteorológica

![Arquitetcura de Alto Nicel](images/unidad7/arquitectura-de-alto-nivel.jpg)

---
### Arquitectura del sistema de recolección de datos

![Arquitectura del sistema de recolección de datos](images/unidad7/sistema-recoleccion-de-datos.jpg)

---
### Identificación de las clases Objeto
* Identificar las clases de objetos se vuelve a menudo una parte difícil del diseño orientado a objetos.
* No existe una "fórmula mágica" para la identificación de objetos. Se basa en la habilidad, la experiencia y el
conocimiento del dominio de los diseñadores de sistemas
* La Identificación de objetos es un proceso iterativo. Es poco probable hacerlo bien la primera vez.

---
### Aproximaciones para la identificación
* Utilizar un enfoque gramatical basado en una descripción en lenguaje natural del sistema
* Basar la identificación en las cosas tangibles en el dominio de aplicación.
* Utilizar un enfoque conductual e identificar objetos en función de su participación y su comportamiento.
* Utilizar un análisis basado en escenarios. Se identifican los objetos, atributos y métodos en cada escenario.

---
### Descripción de la estación meteorológica
<!-- .slide: style="font-size: 0.90em" -->
* Una estación meteorológica es un paquete de instrumentos controlados por software que recoge los
datos, lleva a cabo algún tipo de procesamiento de datos y transmite estos datos para su posterior procesamiento. Los
instrumentos incluyen el aire y los termómetros de tierra, un anemómetro, una veleta, un barómetro y un
pluviómetro. Los datos se recogen periódicamente.
* Cuando se emite un comando para transmitir los datos del clima se resumen los datos recopilados. Los datos
resumidos se transmiten control central.

---
### Clases de objeto de la estación meteorológica
<!-- .slide: style="font-size: 0.80em" -->
La identificación de clase de objetos en el sistema de estación meteorológica puede estar basada en el hardware
y los datos tangibles en el sistema:
* Termómetro de tierra, anemómetro, barómetro, (objetos de dominio de aplicación que son objetos
'hardware' relacionados con los instrumentos en el sistema)
* Estación meteorológica
* La interfaz básica de la estación meteorológica a su entorno. Por lo tanto, refleja las interacciones
identificadas en el modelo de casos de uso.
* Los datos del clima
* Los datos resumidos de los instrumentos.

---
### Clases de objeto de la Estación meteorológica

![Clase Objeto](images/unidad7/clases-objeto.png)

---
### Patrones de diseño
* Son soluciones habituales a problemas comunes en el diseño de software. 
* Cada patrón es como un plano que se puede personalizar para resolver un problema de diseño particular de tu código.
* Los patrones de diseño varían en su complejidad, nivel de detalle y escala de aplicabilidad.

---
### Patrones de diseño
* Un patrón de diseño es una forma de reutilizar el conocimiento abstracto sobre un problema y su solución.
* Un patrón es una descripción del problema y la esencia de su solución.
* Debe ser lo suficientemente abstracto para ser reutilizados en diferentes entornos.
* Descripciones de patrón suelen hacer uso de las características orientadas a objetos como la herencia y el
polimorfismo.

---
### Patrones de diseño: Desventaja

![Desventaja](images/unidad7/design-patterns-everywhere.jpg)

----

### Patrones de diseño: Desventaja
- Si se emplea un lenguaje "incorrecto", aplicar el patron de diseño puede ser complicado
- A veces se toma al patrón como "dogma" sin adaptarlo correctamente al proyecto.
- Uso injustificado. Quizás no era necesario emplearlo, y la solución podía ser menos compleja.  

---
### Patrones de diseño: Clasificación
* **Patrones creacionales:** Proporcionan mecanismos de creación de objetos que incrementan la flexibilidad y la 
reutilización de código existente.
* **Patrones estructurales:** Explican cómo ensamblar objetos y clases en estructuras más grandes a la vez que se 
mantiene la flexibilidad y eficiencia de la estructura.
* **Patrones de comportamiento:** Se encargan de una comunicación efectiva y la asignación de responsabilidades entre objetos.

----

### Patrones Creacionales
* Factory Method
* Abstract Factory
* Builder
* Prototype
* Singleton

----

### Patrones Estructurales
* Adapter
* Bridge
* Composite
* Decorator
* Facade
* Flyweight
* Proxy
* Page Object

----

## Patrones de Comportamiento
* Chain of Responsibility
* Command 
* Iterator 
* Mediator 
* Memento 
* Observer 
* State
* Strategy 
* Template Method
* Visitor 

----

![Clasificación](images/unidad7/patrones-clasificacion.png)

---
### Elementos del patrón
* Nombre
* Un identificador de patrón significativo.
* Descripción del problema.
* Descripción de la solución.
* No es un diseño concreto, pero es una plantilla para una solución de diseño que pueden ser instanciado de
diferentes maneras.
* Consecuencias
* Los resultados y las ventajas y desventajas de aplicar el patrón.

---

### Creacional: 1. Abstract Factory
Permite producir familias de objetos relacionados sin especificar sus clases concretas.

![Abstract Factory](images/unidad7/1-abstract-factory-mini.png)

----

### Creacional: 2. Builder
Permite construir objetos complejos paso a paso. Permite producir distintos tipos y representaciones de un objeto
empleando el mismo código de construcción.

![Builder](images/unidad7/2-builder-mini.png)

----

### Creacional: 3. Factory Method
Proporciona una interfaz para crear objetos en una superclase, mientras permite a las subclases alterar el tipo de 
objetos que se crearán.

![Factory Method](images/unidad7/3-factory-method-mini.png)

----

### Creacional: 4. Prototype
Permite copiar objetos existentes sin que el códugo dependa de sus clases.

![Prototype](images/unidad7/4-prototype-mini.png)

----

### Creacional: 5. Singleton
Permite asegurarnos de que una clase tenga una única instancia, a la vez que proporciona un punto de acceso global a
dicha instancia.

![Singleton](images/unidad7/5-singleton-mini.png )

---
### Estructural: 6. Bridge
Permite dividir una clase grande o un grupo de clases estrechamente relacionadas, en dos jerarquías separadas (abstracción
e implementación) que pueden desarrollarse independientemente la una de la otra.

![Bridge](images/unidad7/6-bridge-mini.png)

----

### Estructural: 7. Composite
Permite componer objetos en estructuras de árbol y trabajar con esas estructuras como si fueran objetos individuales.

![Composite](images/unidad7/7-composite-mini.png)

----

### Estructural: 8. Decorator
Permite añadir fucnionalidades a objetos colocando estos objetos dentro de objetos encapsuladores especiales que contienen
estas funcionalidades.

![Decorator](images/unidad7/8-decorator-mini.png)

----

### Estructural: 9. Facade
Proporciona una interfaz simplificada a una biblioteca, un framework o cualquier otro grupo complejo de clases.

![Facade](images/unidad7/9-facade-mini.png)

----

### Estructural: 10. Flyweight
Permite mantener más objetos dentro de la cantidad disponible de memoria RAM compartiendo las partes comunes del estado
entre varios objetos en lugar de mantener toda la información en cada objeto.

![Flyweight](images/unidad7/10-flyweight-mini.png)

----

### Estructural: 11. Proxy
Permite proporcionar un sustituto o marcador de posición para otro objeto. Un proxy controla el acceso al objeto original,
permitiéndte hacer algo antes o después de que la solicitud llegue al objeto original.

![Proxy](images/unidad7/11-proxy-mini.png)

----

### Estructural: 12. Adapter
Permite la colaboración entre objetos con interfaces incompatibles.

![Adapter](images/unidad7/12-adapter-mini.png)

----

### Estructural: 24. PageObject
Se emplea para pruebas automatizadas, facilitando el mantenimiento y reduciendo la duplicación de código.
Cada elemento de la página (botón, texto, campo de formulario) se coloca en una "página" que permite su re-utilización.

---

### Comportamiento: 13. Chain of Responsability
Permite pasar solicitudes a lo largo de una cadena de manejadores. Al recibir una solicitud, cada manejador decide si
la procesa o su la pasa al siguiente manejador de la cadena.

![Chain of Responsability](images/unidad7/13chain-of-responsibility-mini.png)

----

### Comportamiento: 14. Command
Convierte una solicitud en un objeto independiente que contiene toda la información sobre la solicitud. Esta 
transformación permite parametrizar los métodos con diferentes solicitudes, retrasar o poner en cola la ejecución de una
solicitud y soportar operaciones que no se pueden realizar.

![Command](images/unidad7/14-command-mini.png)

----

### Comportamiento: 15. Interpreter
Define una forma de evaluar o interpretar sentencias en un lenguaje específico. Se utiliza cuando se tiene una gramática 
simple y se quiere representar cada regla como una clase. 
Cada expresión de la gramática es interpretada recursivamente mediante objetos, permitiendo que el sistema analice y 
ejecute el lenguaje en cuestión. Es común en motores de reglas, lenguajes de programación o expresiones matemáticas.

----

### Comportamiento: 16. Iterator
Permite recorrer elementos de una colección sin exponer su representaciín subyacente (lista, pila, árbol, etc).

![Iterator](images/unidad7/16-iterator-mini.png)

----

### Comportamiento: 17. Mediator
Permite reducir las dependencias caóticas entre objetos. El patrón restringe las comunicaciones directas entre los
objetos, forzándolos a colaborar únicamente a través de un objeto mediador.

![Mediator](images/unidad7/17-mediator-mini.png)

----

### Comportamiento: 18. Memento
Permite guardar y restaurar el estado previo de un objeto sin revelar los detalles de su implementación.

![Memento](images/unidad7/18-memento-mini.png)

----

### Comportamiento: 19. Observer
Permite definir un mecanismo de suscripción para notificar a varios objetos sobre cualquier evento que le suceda al
objeto que están observando.

![Observer](images/unidad7/19-observer-mini.png)

----

### Comportamiento: 20. State
Permite a un objeto alterar su comportamiento cuando su estado interno cambia. Parece como su el objeto cambiara su clase.

![State](images/unidad7/20-state-mini.png)

----

### Comportamiento: 21. Strategy
Permite definir una familia de algoritmos, colocara cada uno de ellos en una clase separada y hacer sus objetos
intercambiables.

![Strategy](images/unidad7/21-strategy-mini.png)

----

### Comportamiento: 22. Template method
Define el esqueleto de un algoritmo en la superclase pero permite que las subclases sobre-escriban pasos del algoritmo
sin cambiar su estructura.

![Template method](images/unidad7/23-template-method-mini.png)

----

### Comportamiento: 23. Visitor
Permite separar los algoritmos de los objetos sobre los que operan.

![Visitor](images/unidad7/23-visitor-mini.png)

---
### El patrón observador
* **Nombre:** Observador.
* **Descripción:** Separa la vista del estado del objeto, del objeto en sí.
* **Descripción del problema:** Se utiliza cuando se necesitan varias vistas de estado.
* **Descripción de la solución:** Genera distintas vistas
* **Consecuencias:** Las optimizaciones para mejorar el rendimiento de la vistas no son prácticos.

----

### El patrón Observador

<!-- .slide: style="font-size: 0.60em" -->
<!--
|                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción              | Separa la vista del estado de un objeto del objeto en sí mismo y permite que se proporcionen vistas alternativas. Cuando el estado del objeto cambia, todas las vistas son automáticamente notificadas y actualizadas para reflejar el cambio.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Descripción del problema | En muchas situaciones se debe proporcionar varias vistas de información de estado, como por ejemplo una pantalla gráfica y una pantalla tabular. No todos ellos pueden ser conocidos cuando se especifica la información. Todas las presentaciones alternativas deben apoyar la interacción y, cuando se cambia el estado, todas las pantallas deben ser actualizados. Este patrón se puede utilizar en todas las situaciones en que se requiere más de un formato de visualización de la información de estado y donde no es necesario que el objeto, que mantiene la información de estado, sepa acerca de los formatos de visualización específicos utilizados. |
-->

<table>
<thead>
<tr>
<th style="text-align:left"></th>
<th style="text-align:left"></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Descripción</td>
<td style="text-align:left">Separa la vista del estado de un objeto del objeto en sí mismo y permite que se proporcionen vistas alternativas. Cuando el estado del objeto cambia, todas las vistas son automáticamente notificadas y actualizadas para reflejar el cambio.</td>
</tr>
<tr>
<td style="text-align:left">Descripción del problema</td>
<td style="text-align:left">En muchas situaciones se debe proporcionar varias vistas de información de estado, como por ejemplo una pantalla gráfica y una pantalla tabular. No todos ellos pueden ser conocidos cuando se especifica la información. Todas las presentaciones alternativas deben apoyar la interacción y, cuando se cambia el estado, todas las pantallas deben ser actualizados. Este patrón se puede utilizar en todas las situaciones en que se requiere más de un formato de visualización de la información de estado y donde no es necesario que el objeto, que mantiene la información de estado, sepa acerca de los formatos de visualización específicos utilizados.</td>
</tr>
</tbody>
</table>

----

### Múltiples vistas utilizando el patrón Observador

![Patron Observador](images/unidad7/patron-observador.jpg)

---
### IMPLEMENTACIÓN DEL SOFTWARE
Etapa de la Ingeniería de software en la que se crea la versión ejecutable.

Aspectos importantes en la implementación:
* Reutilización
* Administración de la configuración
* Desarrollo huésped – objetivo

---
### Reutilización
* Desde la década de 1960 hasta la década de 1990, la mayoría del nuevo software ha sido desarrollado desde
cero, escribiendo todo el código en un lenguaje de programación de alto nivel.
* La única reutilización significativa fue la reutilización de funciones y objetos en las bibliotecas de lenguajes de
programación.
* Los costos y la presión de las entregas causaron que este enfoque fuese cada vez más inviable,
especialmente para los sistemas comerciales y basados en Internet.

---
### Niveles de reutilización
<!-- .slide: style="font-size: 0.90em" -->
* **Nivel de abstracción**: En este nivel, no se emplea el software directamente, pero se utiliza el conocimiento de las 
abstracciones exitosas en el diseño de su software.
* **Nivel del objeto:** En este nivel, vuelve a utilizar directamente los objetos de una biblioteca en lugar de escribir 
el código manualmente.
* **Nivel de los componentes:** Los componentes son colecciones de objetos y clases
de objetos que se reutilizan en los sistemas de aplicación.
* **Nivel de sistema:** De vuelve a utilizar los sistemas de aplicación enteros.

---
### Costos de Reutilización
<!-- .slide: style="font-size: 0.90em" -->
* Los costos del tiempo invertido en busca de software para la reutilización y la evaluación de si es o no
ajustable a sus necesidades.
* Los costos de la compra de software reutilizable.
* Los costos de adaptación y configuración de los componentes o sistemas de software reutilizables para
reflejar los requisitos del sistema que se está desarrollando.
* Los costos de la integración de los elementos de software reutilizables entre sí (si está utilizando
software de fuentes diferentes) y con el nuevo código que se ha desarrollado.

---
### Gestión de la configuración
* La gestión de la configuración es el nombre que recibe el proceso general de la gestión de un sistema de software cambiante.
* El objetivo de la gestión de la configuración es apoyar el proceso de integración de sistemas para que todos los
desarrolladores puedan acceder al código y a la documentación del proyecto de una manera controlada,
averiguar qué cambios se han hecho, y compilar y enlazar componentes para crear un sistema.

---
### Actividades de gestión de configuración
<!-- .slide: style="font-size: 0.80em" -->
* **Gestión de versiones**, para realizar un seguimiento de las diferentes versiones de los componentes de software.
Los sistemas de gestión de la versión incluyen facilidades para coordinar el desarrollo de varios programadores.
* **Integración de sistemas**, proporciona apoyo a los desarrolladores a definir qué versiones de los
componentes se utilizan para crear cada versión de un sistema. Esta descripción se utiliza entonces para construir
un sistema de forma automática mediante la compilación y la vinculación a los componentes necesarios.
* **Seguimiento de problemas**, brinda apoyo para que los usuarios reporten errores y problemas. Los desarrolladores
ven quién está trabajando en estos problemas y cuando están resueltos.

---
### Desarrollo huesped - objetivo
<!-- .slide: style="font-size: 0.80em" -->
* La mayoría del software está desarrollado en un equipo pero se ejecuta en una máquina diferente (el objetivo).
* De manera más general, podemos hablar de una plataforma de desarrollo y una plataforma de ejecución.
* Una plataforma es algo más que hardware. Incluye el sistema operativo instalado, más otro software de soporte,
tal como un sistema de base de datos de gestión o, para las plataformas de desarrollo, un entorno de desarrollo
interactivo.
* La plataforma de desarrollo por lo general tiene el software instalado diferente de la plataforma de ejecución;
estas plataformas pueden tener diferentes arquitecturas.

---
### Herramientas de desarrollo
<!-- .slide: style="font-size: 0.90em" -->
* Un compilador integrado y sistema de edición dirigido a la sintaxis que le permite crear, editar y compilar código.
* Un sistema de depuración.
* Herramientas de edición de gráficos, tales como herramientas para editar los modelos UML.
* Herramientas de prueba, tales como Junit que puede ejecutar automáticamente una serie de pruebas en una
nueva versión de un programa.
* Herramientas de apoyo de proyectos que ayudan a organizar el código para diferentes proyectos de desarrollo.

---
### Entornos de desarrollo integrados (IDEs)
<!-- .slide: style="font-size: 0.90em" -->
* Las herramientas de desarrollo de software a menudo se agrupan para crear un entorno de desarrollo integrado (IDE).
* Un IDE es un conjunto de herramientas de software que es compatible con diferentes aspectos del desarrollo de
software, dentro de algún marco e interfaz de usuario comunes.
* Las IDEs son creados para apoyar el desarrollo de un lenguaje específico de programación como Java. El IDE
del lenguaje puede ser especialmente desarrollado, o puede ser una creación de instancias de un IDE de uso
general, con herramientas específicas del lenguaje de apoyo.

---
### Desarrollo de código abierto
<!-- .slide: style="font-size: 0.90em" -->
* Desarrollo de código abierto es un enfoque para el desarrollo de software en el que se publica el código fuente
de un sistema de software y se invita a los voluntarios a participar en el proceso de desarrollo
* Sus raíces están en la Free Software Foundation (www.fsf.org), que aboga que el código fuente no debe ser
propietario sino siempre debe estar disponible para que los usuarios examinen y modifiquen.
* El software de código abierto extendió esta idea a través de Internet para reclutar a una población mucho más
grande de desarrolladores voluntarios.

---
### Los sistemas de código abierto
* El producto de código abierto más conocido es, por supuesto, el sistema operativo Linux que es ampliamente utilizado.
* Otros productos de código abierto importantes son Java, el servidor web Apache, el sistema de gestión de base de
datos MySQL, el sistema de elearning Moodle, etc.

---
### Cuestiones de código abierto
* El producto que se está desarrollando, debería hacer uso de componentes de código abierto?
* Se debería utilizar un enfoque de código abierto para el desarrollo del software?

---
### Negocio de código abierto
* Cada vez más empresas están utilizando productos de un enfoque de código abierto para el desarrollo.
* Su modelo de negocio no depende de la venta de un producto de software, sino en la venta de soporte para ese producto.
* Ellos creen que la participación de la comunidad de código abierto permitirá que el software se desarrolle de
forma más barata, más rápida y creará una comunidad de usuarios para el software.

---
### Concesión de licencias de código abierto
<!-- .slide: style="font-size: 0.90em" -->
* Un principio fundamental de desarrollo de código abierto es que el código fuente debe estar disponible gratuitamente.
* Legalmente, el desarrollador del código (ya sea una empresa o un individuo) todavía posee el código y puede
imponer restricciones sobre cómo se utiliza mediante una licencia de software de código abierto.
* Algunos desarrolladores creen que si un componente de código abierto se utiliza para desarrollar un nuevo sistema,
ese sistema debe también ser de código abierto.
* Otros permiten que su código sea usado sin esta restricción y los sistemas desarrollados pueden ser como
sistemas de código cerrado.

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)

<!--https://refactoring.guru/es/design-patterns-->