---
title: Introduccion
theme: solarized
slideNumber: true
---

#### Ingeniería de Software

# Introducción

Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

---

<!-- .slide: style="font-size: 0.60em" -->
<style>
.grid-item {
    border: 3px solid rgba(121, 177, 217, 0.8);
    padding: 20px;
    text-align: left !important;
}

.grid-container2 {
    display: grid;
    grid-template-columns: auto auto;
    font-size: 0.8em;
    text-align: left !important;
}
</style>

## Temario

<div class="grid-item">

### Ingeniería de Software

- Definición
- ¿Por qué es importante?
- Errores de Software
- Costos del software
- Productos de software
- Especificaciones del producto
- Preguntas sobre la ingeniería de Software
</div>

<div class="grid-container2">
<div class="grid-item">
    
### Ingeniería de Software

- Software
- Ingeniería de Software
  - Capas
- Importancia
- Errores de Software
- Costos
- Productos Genéricos
- Productos personalizados
</div>
<div class="grid-item">


- Disciplinas
- Tipos de aplicaciones
- Actividades
- Atributos Esenciales
- Afecta desarrollo
- Web
- Diseño: Arquitectura
- Atributos de calidad
</div>
</div>

---

# ¿Qué es la ingeniería de Software?

## ¿Qué es el software?

---

## Software

El software es el conjunto de instrucciones, programas y datos que permiten que una computadora o dispositivo electrónico realice tareas específicas.

Es intangible y está compuesto por código que puede ser interpretado o ejecutado por una máquina.

---

## Ingenieria de Software

“La ingeniería de software es una disciplina que se enfoca en el diseño, desarrollo, prueba, implementación y mantenimiento de sistemas de software de alta calidad”. 

Para ello es necesario aplicar de manera sistemática principios, teorías, métodos y herramientas para el desarrollo de software profesional, y satisfacer las necesidades de los usuarios y las empresas.

---

### Capas de la Ingeniería de Software

![Capas de la Ingeniería de Software](images/unidad1/capas-ingenieria-soft.png)

---

### Ingenieria de Software. ¿Por qué es importante?

- La economía de muchos países depende en alguna medida del software.
- Cada vez más sistemas son controlados por software.
- A largo plazo, es más barato realizar una buena planificación del software en una etapa inicial, que refactorizar continuamente.
- El gasto en software representa una fracción significativa del PBI
- Los errores de software pueden ser muy caros

---

## Errores de Software

Enfocarse en la **calidad del software** permite reducir los errores y problemas que el mismo puede tener asociados. 

----

## Errores de Software
En el software, los errores son llamados bugs, debido a que en 1947 Grace Hopper encontró que las fallas del Mark II, computadora electromecánica desarrollada en Harvard, se debían a una polilla, “bug”, entre los relés.

![First bug](images/unidad1/first_bug.png)

----

## Errores de Software

- Los errores en el software son un problema común y...en muchos casos, no hay graves consecuencias,
  se soluciona con una nueva versión corregida
- EN MUCHOS OTROS CASOS PUEDE HABER CONSECUENCIAS FATALES, GRAVES O MUY CARAS.

---

## Errores de Software

Para reflexionar sobre este tema vamos a ver el siguiente video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/IcbEAZTEjqs?si=vaQlTScIifOLNC_i" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

### Algunos "Grandes Errores" de Software...

#### LA EXPLOSIÓN DEL ARIANE 5

1000 millones de dólares perdidos

¿El problema? reutilización de código.
Se reutilizó el código del Ariane 4.
El código asignaba el valor de una variable de 64 bits a una de 16 bits.
Lo que no era un problema en el Ariane 4, destruyó el Ariane 5.

16 bits: −32.768 a 32.767

64 bits: −9.223.372.036.854.775.808 a 9.223.372.036.854.775.807

----

#### LA EXPLOSIÓN DEL ARIANE 5

<iframe width="560" height="315" src="https://www.youtube.com/embed/gp_D8r-2hwk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

----

### Algunos "Grandes Errores" de Software...

#### EXCESO DE RADIACIÓN EN EL THERAC-25

<!-- .slide: style="font-size: 0.80em" -->

Mato a 5 pacientes

La máquina de radiación Therac-25 aplicó un exceso de radiación a varios pacientes provocando la muerte de al menos cinco de ellos.

¿ La causa?
El control de la concurrencia de las rutinas que se ejecutaban en paralelo.

UNA clásica RACE CONDITION

Si bien la interfaz indicaba que todo iba bien, los pacientes estaban recibiendo 125 veces más radiación que lo indicado.

----

#### EXCESO DE RADIACIÓN EN EL THERAC-25

![Therac-25](images/unidad1/therac-25.jpg)

----

### Algunos "Grandes Errores" de Software...

#### MARS CLIMATE ORBITER

<!-- .slide: style="font-size: 0.80em" -->

Un error de unidades

El sistema de control de la nave en la Tierra usaba el sistema métrico anglosajón.

El sistema de navegación de la nave esperaba valores en el sistema métrico decimal.

La trayectoria de la nave se acerco a Marte y fue desintegrada por la fuerza de fricción atmosférica del planeta.

Se incumplieron los requisitos del sistema donde se especificaba que todo el software debía usar el sistema métrico decimal.

----

#### MARS CLIMATE ORBITER

![Mars Climate Orbiter](images/unidad1/mars_climate_orbiter.webp)

----

### Algunos "Grandes Errores" de Software...

#### DESPLIEGUE DE UNA VERSIÓN INCORRECTA

<!-- .slide: style="font-size: 0.80em" -->

Mas de 400 millones de U$S perdidos en 45 minutos

El grupo Knight Capital perdió 460 millones de dólares en menos de una hora.

Se desplego una nueva versión sin modificar la configuración del algoritmo.

Hubo 4 millones de operaciones en 45 minutos

Se ejecuto en modo test, donde, para probar el comportamiento en condiciones extremas, estaban desactivadas las restricciones.
El sistema comenzó a comprar y vender acciones sin evaluar las consecuencias.

----

#### DESPLIEGUE DE UNA VERSIÓN INCORRECTA

<!-- .slide: style="font-size: 0.80em" -->

![Knight Capital](images/unidad1/Knight_Capital.jpg)

---

### Ejercicio

Construye una tabla para analizar la información obtenida y la información del video:
<!-- .slide: style="font-size: 0.80em" -->
<table>
<thead>
<tr>
<th>Año</th>
<th>Software afectado</th>
<th>Sector</th>
<th>Causa del Error</th>
<th>Impacto</th>
</tr>
</thead>
<tbody>
<tr>
<td>1985–1987</td>
<td>Therac-25</td>
<td>Médico</td>
<td>Fallos al cambiar parámetros rápidamente</td>
<td>Al menos 5 pacientes recibieron dosis letales de radiación</td>
</tr>
<tr>
<td></td>
<td>Ariane 5</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>Mars Climate Orbiter</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>Knight Capital</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>Y2K</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


---

### Ejercicio

<img src="images/question.png" style="float: left">

¿Qué otros escenarios catastróficos pero realistas se les ocurren que hagan que el fallo en un programa pudiera ocasionar un gran daño económico o humano?

---

### Costos del software

El costo del software suele ser mayor que el costo del hardware.

El mantenimiento del software cuesta más que el desarrollo del mismo.
Para sistemas que tienen una larga vida, los costos de mantenimiento superan ampliamente los costos de desarrollo.

La ingeniería de software tiene que ver con el desarrollo de software rentable.

----

### Costos del software

![Costos del Software](images/unidad1/costos-software.png)

El costo de mantenimiento suele ser del **67%** del total del ciclo de desarrollo.

---

### Productos de software

<!-- .slide: style="font-size: 0.90em" -->

- **Productos genéricos** <br>
  Sistemas que se comercializan y venden a cualquier cliente:
  Ejemplos - Software para gráficos, herramientas de gestión de proyectos; Software CAD; software para mercados específicos
  (Sistema de turno para dentista).

- **Productos personalizados** <br>
  Software que encarga un cliente específico para satisfacer sus propias necesidades.
  Ejemplos - Sistema de control o monitoreo, software de control del tráfico aéreo, etc.

---

### Especificaciones del producto

- **Productos Genéricos** <br>
  La especificación de lo que el software debe hacer es propiedad del desarrollador del software y las decisiones sobre
  los cambios en el software son hechas por el desarrollador.

- **Productos personalizados** <br>
  La especificación de lo que el software debe hacer es propiedad del cliente del software y el es el que toma decisiones
  sobre los cambios de software necesarios.

----

### Ejercicio

<img src="images/question.png" style="float: left">

Nombre ejemplos de software que sean **productos genéricos** y software que sean **productos personalizados**.

----

### Ejercicio

<img src="images/question.png" style="float: left">

Clasifica los siguientes productos de software en:
- **Producto genérico:** desarrollado para un público amplio, con funcionalidades estándar.
- **Producto personalizado:** desarrollado específicamente para una organización, empresa o necesidad concreta.

----

<!-- .slide: style="font-size: 0.70em" -->
Listado de software para clasificar:
1. Microsoft Word
2. App de gestión para una clínica veterinaria local
3. Canva
4. Sistema de reservas de vuelos de Aerolíneas Argentinas
5. Spotify
6. Aplicación web para controlar el inventario de un supermercado de barrio
7. WhatsApp
8. Plataforma Moodle personalizada para una universidad
9. Google Chrome
10. Software hecho a medida para controlar el ingreso al gimnasio
11. Mercado Libre
12. Sistema de facturación hecho por un programador freelance para un taller mecánico
13. Adobe Photoshop
14. Aplicación de pedidos interna para una cadena de restaurantes
15. Excel

---

### Diferentes disciplinas

En el desarrollo de software intervienen distintas disciplinas que, aunque todas relacionadas, tienen enfoques y objetivos específicos.

- Ciencias de la computación
- Ingeniería de software
- Ingeniería de sistemas

----

### Diferentes disciplinas
<!-- .slide: style="font-size: 0.80em" -->
- **Ciencias de la computación:** Se enfocan en teoría y fundamentos de la computación (algoritmos, estructuras de datos, complejidad, etc).

- **Ingeniería de software:** Se ocupa de todos los aspectos de la producción de software desde las etapas iniciales de la especificación del sistema hasta el mantenimiento del mismo después de que haya entrado en uso.

- **Ingeniería de sistemas:** Se ocupa del desarrollo completo de sistemas basados en computadoras, integrando hardware, software y procesos. 

---


### Ingeniería de software

- Disciplina de Ingeniería <br>
  El uso de las teorías y los métodos adecuados para resolver los problemas teniendo en cuenta las limitaciones financieras y de organización.

- Todos los aspectos de la producción de software <br>
  No sólo el proceso técnico de desarrollo. También la gestión de proyectos y el desarrollo de herramientas, métodos, etc. para apoyar la producción de software.

---

### Importancia de la ingeniería de software

<!-- .slide: style="font-size: 0.90em" -->

- Cada vez más personas y la sociedad en general dependen de sistemas de software avanzados. Tenemos que ser capaces de
  producir sistemas fiables de manera económica y rápida.

- Por lo general es más barato, en el largo plazo, el uso de métodos de ingeniería de software y técnicas para los
  sistemas de software en lugar de escribir los programas como si fuera un proyecto de programación personal.

- La mayor parte de los costos corresponde a los costos de corregir el software después de que ha entrado en uso.

---

### Diversidad en la ingeniería de software
Hay muchos tipos diferentes de sistemas de software y no existe un conjunto universal de las técnicas de software que sea aplicable a todas ellas.

Los **métodos** de ingeniería de software y las **herramientas** que se utilizan dependen del tipo de aplicación que se está desarrollando, los requisitos del cliente y los antecedentes del equipo de desarrollo. 

----

### Diversidad en la ingeniería de software
<!-- .slide: style="font-size: 0.80em" -->
Si bien todo proyecto de software debe **gestionarse y desarrollarse** de manera profesional, existen diferentes técnicas que son adecuadas para distintos tipos de sistema. 

Por ejemplo, los juegos siempre deben diseñarse usando una serie de prototipos, mientras que los sistemas críticos de control de seguridad requieren de una especificación completa y analizable para su desarrollo. 

No puede decirse que un método sea mejor que otro. La elección del método de gestión y desarrollo depende del tipo de software que se debe contruir.


----

### Tipos de aplicaciones

1. Aplicaciones autónomas
2. Aplicaciones basadas en transacciones interactivas
3. Sistemas embebidos o de control
4. Sistemas de procesamiento por lotes
5. Sistemas de entretenimiento
6. Sistemas para el modelado y simulación
7. Sistemas de adquisición de datos
8. Sistemas de sistemas

----

### Tipos de aplicaciones

<!-- .slide: style="font-size: 0.80em" -->

- **1. Aplicaciones autónomas** <br>
  Estos son los sistemas de aplicación que se ejecutan en un equipo local, como un PC. Incluyen toda la funcionalidad
  necesaria y no es necesario estar conectado a una red.

- **2. Aplicaciones basadas en transacciones interactivas** <br>
  Las aplicaciones que se ejecutan en un equipo remoto y se puede acceder por los usuarios desde sus propios ordenadores
  o terminales. Esto incluye aplicaciones web.

- **3. Sistemas embebidos o de control** <br>
  Se trata de sistemas de software que controlan y gestionan dispositivos de hardware. Su número es superior a cualquier
  otro tipo de sistema.

----

### Tipos de aplicaciones

<!-- .slide: style="font-size: 0.80em" -->

- **4. Sistemas de procesamiento por lotes** <br>
  Estos son que están diseñados para procesar los datos en grandes lotes. Procesan un gran número de entradas individuales
  para crear salidas correspondientes.

- **5. Sistemas de entretenimiento** <br>
  Se trata de sistemas que son principalmente para su uso personal y que están destinados a entretener al usuario.

- **6. Sistemas para el modelado y simulación** <br>
  Se trata de sistemas cuyo objetivo es modelar procesos físicos donde distintas entidades interactúan entre si.

----

### Tipos de aplicaciones

- **7. Sistemas de adquisición de datos**
  Se trata de sistemas que recopilan datos de su entorno utilizando un conjunto de sensores y envían estos datos a otros
  sistemas para el procesamiento.

- **8. Sistemas de sistemas**
  Estos son sistemas que están compuestos de un número de otros sistemas de software.

----

### Ejercicio

Clasifique los siguientes Softwares según tipos de aplicaciones:

<div class="grid-container2">
<div class="grid-item">
    
  - Aplicaciones autónomas
  - Aplicaciones basadas en transacciones interactivas
  - Sistemas embebidos o de control
  - Sistemas de procesamiento por lotes
  - Sistemas de entretenimiento
  - Sistemas para el modelado y simulación
  - Sistemas de adquisición de datos
  - Sistemas de sistemas
</div>
<div class="grid-item">

- Liquidación de sueldos
- Home Banking
- Estaciones meteorológicas
- Minecraft
- Controlador de un ascensor
- Simulador de vuelo
- Sistema de gestión de una ciudad inteligente
- Visual Studio Code
</div>
</div>

---

### Actividades

Tareas que se deben llevar a cabo en el proceso de desarrollo:

1. **Especificación del software:** clientes e ingenieros definen qué debe hacer el software y sus restricciones.
2. **Desarrollo del software:** diseño y programación.
3. **Validación del software:** verificación de que cumple con los requisitos.
4. **Evolución del software:** adaptación a nuevos requerimientos del cliente o del mercado.

----

![Actividades](images/unidad1/actividades.png)

---

### Atributos esenciales de un buen software

 Un buen software debe reunir ciertas cualidades fundamentales que garanticen su utilidad,calidad y sostenibilidad a lo largo del tiempo. 
 
 Los atributos esenciales de un buen software son:

- Mantenimiento
- Confiabilidad y seguridad
- Eficiencia
- Aceptabilidad

----

### Atributos esenciales de un buen software

<!-- .slide: style="font-size: 0.80em" -->

- **Mantenimiento:** El software debe escribirse de tal forma que pueda evolucionar para satisfacer las necesidades cambiantes de los clientes. Éste es un atributo crítico porque el cambio del software es un requerimiento inevitable de un entorno empresarial variable.

- **Confiabilidad y seguridad:** La confiabilidad del software implica su capacidad para funcionar correctamente sin fallos graves. La seguridad asegura que usuarios malintencionados no puedan acceder o dañar el sistema.


----

### Atributos esenciales de un buen software

<!-- .slide: style="font-size: 0.80em" -->

- **Eficiencia:** El software debe optimizar el uso de los recursos del sistema, como la memoria y los ciclos del procesador. Por lo tanto, la eficiencia incluye la capacidad de respuesta, el tiempo de procesamiento, la utilización de la memoria, etc.

- **Aceptabilidad:** El software debe ser aceptable para el tipo de usuario para el que está diseñado. Esto significa que debe ser comprensible, utilizable y compatible con otros sistemas que utilizan.

----

### Ejercicio

<img src="images/question.png" style="float: left">

¿Da ejemplos positivos o negativos donde se vea claramente la presencia o ausencia muy marcada de los atributos escenciales de un buen software?
- Mantenimiento
- Confiabilidad y seguridad
- Eficiencia
- Aceptabilidad

----

### Ejercicios

A continuación, se presentan distintas situaciones relacionadas con programas o sistemas de uso común.
Identificar qué atributo esencial del software está en juego en cada caso.

----

🔍 Situaciones:
<!-- .slide: style="font-size: 0.70em" -->
1. Un software de facturación permite incorporar fácilmente nuevas reglas impositivas cada vez que cambia la ley.
2. Una app de transferencias bancarias muestra errores inesperados al confirmar montos y algunas veces duplica pagos.
3. Una página web de inscripción a becas funciona rápido y consume pocos recursos del navegador.
4. Un sistema educativo online no se adapta bien a dispositivos móviles y muchos usuarios lo consideran difícil de usar.
5. Un programa que gestiona turnos médicos incluye copias de seguridad automáticas y encriptación de los datos.
6. Una empresa cambia su sistema contable y el nuevo software se adapta fácilmente a sus procesos sin necesidad de rehacer todo.
7. Un videojuego popular recibe constantes actualizaciones para corregir errores y agregar contenido.
8. Una app de mensajería encripta los mensajes y solo permite el acceso con doble autenticación.

<!--
N°	Atributo
1	Mantenimiento
2	Confiabilidad
3	Eficiencia
4	Aceptabilidad
5	Seguridad
6	Mantenimiento
7	Mantenimiento
8	Seguridad
-->

---

### Detalles que afectan el desarrollo del software

<!-- .slide: style="font-size: 0.80em" -->

- **Heterogeneidad** <br>
  Cada vez con mayor frecuencia se requieren sistemas que operen como sistemas distribuidos a través de redes que incluyan
  diferentes tipos de computadoras y dispositivos móviles.

- **Cambio empresarial y social** <br>
  Los negocios y la sociedad cambian de manera rápida, conforme se desarrollan las economías emergentes y nuevas
  tecnologías están a la disposición. Ambos necesitan tener la posibilidad de cambiar su software existente y desarrollar
  rápidamente uno nuevo.

- **Seguridad y confianza** <br>
  Dado que el software está vinculado con todos los aspectos de la vida, es esencial confiar en dicho software

---

### Fundamentos de la ingeniería de software

<!-- .slide: style="font-size: 0.80em" -->

Algunos principios se aplican a todos los tipos de sistema de software:
- **Proceso controlado:** Los sistemas deben desarrollarse mediante un proceso dirigido y comprendido.
- **Fiabilidad y rendimiento:** Son esenciales en todo tipo de sistema.
- **Gestión de requisitos:** Entender y administrar correctamente lo que el software debe hacer es clave.
- **Reutilización:** Siempre que sea posible, se deben reutilizar componentes de software existentes en lugar de desarrollarlos desde cero.

---

### La ingeniería de software y la web

La Web es hoy una plataforma estándar y las organizaciones están utilizando cada vez más los sistemas basados en la web en lugar de los sistemas locales.

En este modelo, conocido como SaaS (Software as a Service), las aplicaciones se ejecutan de forma remota en la 'nube', y los usuarios pagan por el acceso y el uso del software en lugar de comprarlo de manera tradicional. Algunos ejemplos de SaaS son Gmail, Google Drive o Netflix.

----

### La ingeniería de software y la web

- **Reutilización de software:** Se diseña a partir de componentes y sistemas de software pre-existentes.

- **Desarrollo y entrega incremental:** en general no es práctico especificar todos los requisitos para este tipo de sistemas con anticipación.

Las **interfaces** de usuario dependen de las capacidades de los navegadores web.

---

### Diseño de sistemas

Es el proceso de definición global de un sistema, que contempla:
- Arquitectura
- Módulos
- Interfaces
- Datos 
para satisfacer requisitos específicos de los usuarios.

Este proceso busca garantizar que el sistema sea eficiente, escalable y mantenible a lo largo del tiempo.

----

### Diseño de sistemas: Arquitectura
La **arquitectura** de sistemas se refiere al diseño de alto nivel que define cómo interactúan los diferentes componentes de un sistema, incluyendo hardware, software, redes y bases de datos, para lograr un objetivo común.

- Una arquitectura bien diseñada debe:
- Responder a los requerimientos del sistema.
- Asegurar la eficiencia en el uso de recursos.
- Permitir la escalabilidad para adaptarse a futuros cambios.
- Facilitar la mantenibilidad del sistema.

----

### Diseño de sistemas: Arquitectura
El diseño arquitectónico debe estar siempre basado en los requerimientos funcionales y no funcionales que expresan las necesidades del usuario.

Para simplificar y mejorar el proceso de diseño, se utiliza el modelado de sistemas. 

----

### Diseño de sistemas: Modelado
<!-- .slide: style="font-size: 0.80em" -->
El modelado consiste en la creación de modelos abstractos que representan diferentes perspectivas del sistema, ayudando a comprender su estructura y comportamiento.

Generalmente, estos modelos se expresan mediante notaciones gráficas, siendo el Lenguaje Unificado de Modelado (UML) uno de los estándares más utilizados.

El modelado de sistemas cumple dos funciones esenciales:
- Ayuda a los analistas y diseñadores a comprender la funcionalidad del sistema.
- Sirve como medio de comunicación efectivo con los clientes y usuarios.

---

### Atributos de Calidad en el Diseño de Sistemas
Durante el diseño, es fundamental considerar ciertos atributos de calidad que impactarán en la confiabilidad y desempeño del sistema:

- Confiabilidad
- Disponibilidad
- Seguridad
- Protección

Un diseño de sistemas exitoso debe equilibrar estos atributos para construir soluciones robustas, seguras y adaptables.

----

### Atributos de Calidad en el Diseño de Sistemas
- **Confiabilidad:** Es la probabilidad de que el sistema funcione correctamente y sin errores durante un período de tiempo determinado en un entorno específico.
- **Disponibilidad:** Representa la capacidad del sistema para estar operativo y accesible cuando los usuarios lo necesitan, minimizando interrupciones o tiempos de inactividad.

----

### Atributos de Calidad en el Diseño de Sistemas
- **Seguridad:** Consiste en proteger el sistema frente a amenazas externas y garantizar su resistencia ante ataques cibernéticos. La seguridad debe ser considerada a lo largo de todo el ciclo de vida del software, desde los requisitos hasta el mantenimiento.
- **Protección:** Se refiere a salvaguardar la propiedad intelectual del software, proteger información confidencial y prevenir copias o accesos no autorizados.

---
### Diferencias: Atributos del software y del diseño
Los **atributos esenciales** están más ligados a la experiencia del usuario y a lo que se espera del software terminado.

Los **atributos de calidad** del diseño están más relacionados con la estructura interna del sistema, facilitando su evolución, mantenimiento y escalabilidad.

----

### Ejercicio

<img src="images/question.png" style="float: left">

¿Da ejemplos positivos o negativos donde se vea claramente la presencia o ausencia muy marcada de los atributos de calidad de un software?
- Confiabilidad
- Disponibilidad
- Seguridad
- Protección

----

#### Ejercicio

A continuación, se presentan diferentes situaciones relacionadas con el diseño de un sistema informático.
Identificar qué atributo de calidad se ve más involucrado en cada caso (confiabilidad, disponibilidad, seguridad o protección).

----

🔍 Situaciones:
<!-- .slide: style="font-size: 0.75em" -->
1. Una app de home banking presenta fallos cada vez que los usuarios intentan hacer transferencias por la noche.
2. Un sistema de turnos online para un hospital permanece caído durante más de 3 horas, sin notificaciones a los usuarios.
3. Un sitio de comercio electrónico cifra los datos de tarjeta de crédito antes de enviarlos al servidor.
4. Un sistema bloquea automáticamente a un usuario tras 3 intentos fallidos de inicio de sesión.
5. Una empresa pierde datos de clientes tras una caída inesperada del sistema y no tiene respaldo actualizado.
6. Una app de mensajería implementa doble autenticación para ingresar desde un nuevo dispositivo.
7. Una plataforma de streaming funciona bien, pero se desconecta cada vez que hay muchos usuarios conectados al mismo tiempo.
8. En una empresa, los usuarios solo pueden acceder a las secciones del sistema correspondientes a su rol.

<!--
N°	Atributo	Justificación breve
1	Confiabilidad	La app falla en una función clave (transferencias).
2	Disponibilidad	El sistema no está operativo por varias horas.
3	Seguridad	Se protege la información sensible con cifrado.
4	Protección	Se limita el acceso tras intentos fallidos.
5	Confiabilidad	No hay respaldo ante una falla, lo que afecta la confianza del sistema.
6	Seguridad	Se protege el acceso con doble autenticación.
7	Disponibilidad	El sistema no soporta alta demanda de usuarios.
8	Protección	Se restringe el acceso según el rol del usuario.
-->

---

## ¿Dudas, Preguntas, Comentarios?

![DUDAS](images/pregunta.gif)
