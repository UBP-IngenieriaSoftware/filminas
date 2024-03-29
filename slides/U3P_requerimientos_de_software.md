---
title: Requerimientos de Software
theme: solarized
slideNumber: true
---

# Ingeniería de Software
## Requerimientos de Software
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

### Requerimientos de Software
* Historial de Cambios
* **Introducción**
* Propósito
* Alcance
* Personal Involucrado
* Definiciones, Acrónimos y Abreviaturas
* Referencias
* Resumen
</div>
<div class="grid-item">

* **Descripción General**
* Perspectiva del Producto
* Funciones del Producto
* Características de los Usuarios
* Restricciones
* Supuestos y Dependencias
* **Requerimientos Específicos**
* Interfaces Externas
* Requerimientos Funcionales
* Requerimientos No Funcionales
</div>
</div>

---
## Historial de Cambios
<!-- .slide: style="font-size: 0.75em" -->
Permite realizar un seguimiento de las modificaciones, ediciones y revisiones que se han realizado en un archivo a lo 
largo del tiempo. Es útil en entornos de colaboración, y tiene varios propósitos:
1. **Control de versiones:** Permite llevar un registro de las diferentes versiones de un documento a medida que se 
realizan modificaciones. Esto facilita la identificación de quién hizo cada cambio, cuándo se realizó y qué cambios 
específicos se hicieron en cada revisión. Esto es esencial para rastrear la evolución del documento y asegurarse de 
que se conserve un registro completo de las ediciones.
2. **Colaboración:** Ayuda a evitar conflictos y a mantener una visión clara de quién contribuyó con qué. Permite a 
los colaboradores revisar las ediciones de los demás y aprobar o rechazar los cambios propuestos. Esto facilita el 
trabajo en equipo y la comunicación entre colaboradores.

----

<!-- .slide: style="font-size: 0.75em" -->
3. **Seguridad y recuperación:** Si se comete un error o se necesita volver a una versión anterior del documento, el 
historial de cambios permite restaurar una versión anterior del archivo. Esto puede ser útil para deshacer cambios no 
deseados o para recuperar información que se haya eliminado por accidente.
4. **Auditoría y cumplimiento:** Permite realizar auditorías y demostrar el cumplimiento de regulaciones. Proporciona 
una traza detallada de todas las modificaciones realizadas en un documento a lo largo del tiempo, lo que puede ser 
necesario para propósitos legales o regulatorios.
5. **Mejora de la calidad:** Al revisar el historial de cambios, los autores y revisores pueden aprender de las 
ediciones anteriores y mejorar gradualmente la calidad del documento. Esto permite una retroalimentación continua y la 
posibilidad de corregir errores y deficiencias con el tiempo.

----

El historial de cambios es una herramienta fundamental en la gestión de documentos que proporciona transparencia, 
control y seguridad en el proceso de edición y revisión. Facilita la colaboración y asegura que un documento evolucione 
de manera controlada y documentada.

---
## Sección 1: Introducción
* Propósito
* Alcance
* Personal Involucrado
* Definiciones, Acrónimos y Abreviaturas
* Referencias
* Resumen

---
### Propósito
<!-- .slide: style="font-size: 0.75em" -->
Se refiere a su razón de existir y guía el contenido, el formato y el enfoque del mismo. Se debe considerar:
1. **Objetivo claro:** ¿Qué se espera lograr con este documento? ¿Qué información se quiere comunicar o qué acción se 
desea impulsar? El objetivo ayuda a mantener el enfoque y la relevancia del documento.
2. **Audiencia objetivo:** Identificar a quiénes está dirigido el documento. Puede ser un grupo específico de personas, 
como empleados, clientes, inversores, estudiantes, o el público en general. Comprender las necesidades, intereses y 
nivel de conocimiento de la audiencia ayuda a adaptar el contenido y el tono del documento para que sea efectivo.
3. **Mensaje clave:** Determine cuál es el mensaje o la información más importante que se debe transmitir. Esto puede 
incluir datos clave, recomendaciones, instrucciones o cualquier otro contenido esencial.

----

<!-- .slide: style="font-size: 0.75em" -->
4. **Acción deseada:** Si el documento busca impulsar una acción específica por parte de la audiencia es importante 
destacar cuál es y proporcionar la información necesaria para que pueda llevarla a cabo.
5. **Beneficios y valor:** Explique cómo la información contenida en el documento beneficia a la audiencia. ¿Qué valor 
agrega? Comunicar los beneficios puede motivar a la audiencia a prestar atención al documento y tomar medidas. 
6. **Contexto y antecedentes:** Permite comprender el contenido del documento. 
7. **Tono y estilo:** El tono y el estilo de redacción deben estar alineados con el propósito del documento y la 
audiencia objetivo.
8. **Estructura y formato**: Deben estar diseñados de manera coherente con su propósito. Esto incluye la organización de 
secciones, el uso de gráficos, tablas o imágenes, y la elección de la tipografía y los colores.

----

Definir claramente el propósito de un documento es esencial para crear un contenido efectivo y relevante. Esto 
garantiza que el documento cumpla con sus objetivos y llegue de manera efectiva a la audiencia deseada. Además, 
proporciona una base sólida para la planificación, redacción y revisión del documento.

---
<!-- .slide: style="font-size: 0.75em" -->
### Alcance
El alcance es una parte fundamental de la planificación, ya que define los límites y las dimensiones del proyecto, 
establece lo que se incluirá y lo que quedará fuera, y proporciona una visión general de los objetivos y metas del mismo. 

Los componentes clave del alcance de un proyecto de desarrollo de software:
* **Nombre del producto:** Es la identificación principal del proyecto y lo distingue de otros productos o proyectos. 
Este nombre debe ser descriptivo y fácil de recordar para que todos los interesados puedan referirse al proyecto de 
manera coherente.
* **Funcionalidades incluidas:** Se debe especificar qué funcionalidades o características se incluirán en el producto 
de software. Estas funciones deben estar directamente relacionadas con los objetivos y necesidades del cliente o usuario 
final.

----

<!-- .slide: style="font-size: 0.90em" -->
* **Funcionalidades excluidas:** Se recomienda definir lo que el producto de software no hará. Ayuda a evitar 
expectativas no cumplidas.
* **Beneficios y valor:** Describe los beneficios que el software aportará a los usuarios 
finales y a la organización. ¿Cómo mejorará la eficiencia, la productividad o la experiencia del usuario? ¿Qué valor 
agregado proporcionará en comparación con soluciones existentes o competidores?
* **Objetivos y metas:**  Esto podría incluir plazos específicos, métricas de rendimiento, metas de adopción por parte 
de los usuarios o cualquier otro indicador relevante. Los objetivos deben ser cuantificables y alcanzables.

----

<!-- .slide: style="font-size: 0.90em" -->
* **Requisitos no funcionales:**  Como por ejemplo el rendimiento, la seguridad, la escalabilidad y la usabilidad. 
Estos requisitos son esenciales para garantizar que el producto cumpla con los estándares de calidad y rendimiento esperados.
* **Restricciones y limitaciones:** situaciones que pueda afectar al proyecto, como restricciones presupuestarias, de 
recursos o de tiempo. Estas definiciones ayudarán a establecer expectativas realistas. 
* **Aprobación y aceptación:** El alcance del proyecto debe ser aprobado por todas las partes interesadas relevantes, 
incluidos los patrocinadores, los clientes y el equipo de desarrollo. Esto garantiza que todas las partes tengan una 
comprensión común y acordada del alcance del proyecto.

----

Definir el alcance de un proyecto de desarrollo de software es un paso crucial en su planificación y 
ejecución. Un alcance bien definido proporciona una base sólida para la gestión eficaz del proyecto, ayuda a evitar 
problemas de alcance y garantiza que todas las partes interesadas estén alineadas en cuanto a lo que se espera del 
proyecto y lo que no se espera.

---
### Personal Involucrado
El personal involucrado en un proyecto de desarrollo de software desempeña roles específicos y tiene responsabilidades 
definidas. Mantener un registro de esta información es fundamental para una gestión eficaz del proyecto y para 
garantizar una comunicación fluida y una colaboración exitosa entre los miembros del equipo. 

----

<!-- .slide: style="font-size: 0.70em" -->
Algunos campos que se pueden completar:
* **Nombre:** Ayuda a identificar a cada miembro del equipo y facilita la comunicación y la colaboración.
* **Rol:** Cada miembro del equipo desempeña un rol específico en el proyecto. Los roles pueden incluir, entre otros, analistas de negocios, desarrolladores de software, diseñadores de interfaz de usuario (UI/UX), testers, gerentes de proyecto, arquitectos de software y administradores de bases de datos. Es importante definir claramente el rol de cada persona para que sepan qué se espera de ellos.
* **Responsabilidades:** Enumerar las responsabilidades específicas que se les asignan. Esto ayuda a comprender sus 
tareas y contribuciones en el proyecto. 
* **Contacto:** Suele incluir direcciones de correo electrónico, números de teléfono y cualquier otra información 
relevante para la comunicación eficaz. También es útil incluir información sobre la disponibilidad de cada persona y los 
mejores momentos para contactarlos.

----

<!-- .slide: style="font-size: 0.80em" -->
Otra información útil...
* **Experiencia y habilidades:**  Experiencia previa y las habilidades específicas de cada miembro del equipo. Esto 
puede ayudar a la asignación de tareas y a garantizar que se aproveche al máximo el conjunto de habilidades del equipo.
* **Horarios y disponibilidad:** Suele ser importante en proyectos que involucran equipos distribuidos o colaboradores 
con diferentes husos horarios.
* **Expectativas de comunicación:** Suelen listarse las reuniones regulares, herramientas de colaboración, informes de 
estado, etc.
* **Formación y desarrollo:** Si se requieren habilidades específicas para el proyecto, es importante documentar 
cualquier formación o desarrollo adicional que se deba proporcionar a los miembros del equipo para cumplir con sus 
responsabilidades.

----

Mantener un registro detallado del personal involucrado en el desarrollo de software es esencial para una gestión 
efectiva del proyecto. Esto asegura que cada miembro del equipo comprenda su rol y responsabilidades, facilita la 
comunicación y la colaboración, y ayuda a garantizar que el proyecto se desarrolle de manera eficiente y se alcancen los 
objetivos establecidos.

---
<!-- .slide: style="font-size: 0.80em" -->
### Definiciones, Acrónimos y Abreviaturas
Esta sección es fundamental para garantizar la comprensión precisa del contenido del documento.

* **Definición:** Es una explicación precisa y clara de lo que significa una palabra, término o concepto. Ayuda a 
comprender el significado de la palabra en cuestión.
* **Acrónimo:** Es una palabra formada tomando las letras iniciales de una serie de palabras y usándolas juntas como una 
nueva palabra.
* **Abreviatura:** Es una forma corta de una palabra o frase que se crea mediante la omisión de una o más letras o sílabas.

----

La importancia de esta sección radica en:
* **Claridad y Comprensión:** Garantizar que los lectores del documento comprendan completamente los términos, acrónimos 
y abreviaturas utilizados a lo largo del texto. Al proporcionar definiciones claras y explicaciones para estas palabras 
y siglas, se reduce la posibilidad de malentendidos y confusiones.
* **Reducción de Ambigüedades:** Al definir con precisión los términos y las abreviaturas, se elimina la ambigüedad y se 
asegura que todos los lectores tengan la misma interpretación de los conceptos clave.

----

<!-- .slide: style="font-size: 0.70em" -->
* **Facilita la Referencia Cruzada:** Cuando un documento hace referencia a otros documentos, estándares o recursos 
externos, es importante incluir abreviaturas y acrónimos relacionados. Esto facilita la referencia cruzada y ayuda a los 
lectores a encontrar y comprender los recursos mencionados.
* **Ahorra Espacio:** En documentos extensos, el uso de abreviaturas puede ayudar a ahorrar espacio y a mantener el 
documento conciso. 
* **Mantenimiento y Actualización:** A medida que se desarrolla un proyecto o se actualiza un documento, es posible que 
surjan nuevos términos o acrónimos. Esta sección también sirve como un lugar para agregar definiciones y mantener el 
documento actualizado con el tiempo.
* **Formato y Organización:** La sección se organiza en orden alfabético para facilitar la búsqueda. Cada término se 
presenta junto con su significado o explicación. Los acrónimos y las abreviaturas se enumeran en orden alfabético y se 
expanden la primera vez que se utilizan en el texto.

----

La sección de "Definiciones, Acrónimos y Abreviaturas" en un documento es una herramienta valiosa para garantizar la 
claridad, la precisión y la comprensión en la comunicación escrita. Ayuda a los lectores a navegar por el contenido de 
manera efectiva y evita malentendidos.

---
### Referencias
Este apartado lista las referencias a todos los documentos complementarios que se mencionan en el cuerpo del documento.

---
### Resumen
Es una descripción breve de la información expuesta y de cómo esta se organiza en el documento.
Suele listar las secciones.

---
## Sección 2: Descripción General
* Perspectiva del Producto
* Funciones del Producto
* Características de los Usuarios
* Restricciones
* Supuestos y Dependencias

---
### Descripción General
Esta sección describe cuáles son los factores que afectan al producto de software a desarrollar y a sus requerimientos.

---
### Perspectiva del Producto
Este apartado detalla cuál es la relación del producto de software a desarrollar con otros sistemas, en tanto que si lo 
desarrollado forma parte de un sistema más grande, describe cómo los requerimientos de ese sistema se relacionan con el 
que se está desarrollando. En ambos casos, se detallan las interfaces necesarias para llevar adelante la comunicación 
del producto de software.

---
### Funciones del Producto
Es el resumen de las funcionalidades más importantes que el producto de software a desarrollar debe cumplir. En 
ocasiones se utiliza un diagrama de caso de uso en esta sección.

---
### Características de los Usuarios
Esta sección establece las cualidades que deben poseer los usuarios para utiliza el producto de software a desarrollar.

| Tipo de Usuario | Formación | Habilidades | Actividades |
|-----------------|-----------|-------------|-------------|

---
### Restricciones
Este apartado señala las limitaciones a las que puede estar sujeto el desarrollo del producto; por ejemplo, políticas 
gubernamentales, limitaciones de hardware, protocolos de comunicación, consideraciones referentes a la seguridad, 
etc.

---
### Supuestos y Dependencias
Las dependencias de terceros en puntos determinados del proceso de desarrollo o la asunción de que una funcionalidad
determinada será provista por la base de datos y no por el producto de software.

---
## Sección 3: Requerimientos Específicos
* Interfaces Externas
* Requerimientos Funcionales
* Requerimientos No Funcionales

---
### Requerimientos Específicos
Esta es la sección más extensa e importante del documento. Describe todos los requerimientos del sistema, con un nivel 
suficiente de detalle de modo que estos puedan ser utilizados, por un lado, para diseñar el sistema, de forma tal que 
satisfaga estos mismos requerimientos y, por el otro, para que los testers los puedan utilizar como base para las 
pruebas funcionales.

---
### Interfaces Externas
<!-- .slide: style="font-size: 0.80em" -->
Se definen todas las entradas y las salidas que el producto de software debe soportar. En esta sección se definen los 
requerimientos de:
* **Interfaces de Usuario:** por ejemplo, el cliente puede haber solicitado la utilización de cierta plantilla o 
combinación de colores.
* **Interfaces Hardware:** características lógicas entre el producto software y el hardware. Por ejemplo, la utilización 
de un puerto serie para poder realizar ciertas funciones.
* **Interfaces Software:** si el producto software debe comunicarse con otros sistemas, se describen las interfaces 
(contenido y formato) que se utilizarán y los protocolos.

---
### Requerimientos Funcionales
<!-- .slide: style="font-size: 0.70em" -->
Son aquellos que satisfacen las acciones elementales que tienen lugar en el producto de software a desarrollar. Para 
describir en forma correcta estas acciones, estas comienzan con: “El sistema deberá...”.
* Comprobación de validez de las entradas
* Secuencia exacta de operaciones
* Respuesta a situaciones anormales (desbordamientos, comunicaciones, recuperación de errores)
* Parámetros Generación de salidas
* Relaciones entre entradas y salidas (secuencias de entradas y salidas, fórmulas 	para la conversión de información)
* Especificación de los requisitos lógicos para la información que será almacenada en base de datos (tipo de información, 
requerido)

---
![Tabla efectos](images/unidad3/tabla_efecto.jpg)

---
### Requerimientos No Funcionales
Esta sección detalla todos los requerimientos no funcionales que deben estar presentes en el producto software a 
desarrollar, por ejemplo: performance, seguridad, disponibilidad, mantenibilidad, portabilidad, etc.

----

Los Requerimientos No Funcionales, también conocidos como **atributos de calidad** o **criterios de calidad**, son 
aspectos fundamentales que definen cómo debe comportarse un sistema de software en lugar de qué debe hacer. 

Estos elementos son esenciales para garantizar que el producto final cumpla con las expectativas de los usuarios y las 
necesidades del negocio. 

----

<!-- .slide: style="font-size: 0.80em" -->
Algunos de los Requerimientos No Funcionales comunes:
* **Performance:** Se refiere a la capacidad del software para realizar sus funciones de manera eficiente, en términos 
de velocidad y capacidad de respuesta. Los aspectos de rendimiento incluyen el tiempo de carga de la aplicación, la 
velocidad de procesamiento de datos y la gestión eficiente de recursos como la memoria y la CPU.
* **Seguridad:** Es un factor crítico para proteger los datos y garantizar que el sistema no sea vulnerable a amenazas 
externas o internas. Los requerimientos de seguridad pueden incluir la autenticación de usuarios, el control de acceso, 
la encriptación de datos y la prevención de ataques cibernéticos.

----

<!-- .slide: style="font-size: 0.80em" -->
* **Disponibilidad:** Se refiere a la capacidad del software para estar disponible y en funcionamiento cuando los 
usuarios lo necesitan. La alta disponibilidad implica minimizar el tiempo de inactividad no planificado y garantizar 
que el sistema sea resistente a fallos.
* **Mantenibilidad:** Se relaciona con la facilidad de mantener y mejorar el software con el tiempo. 
Esto incluye la legibilidad del código, la documentación adecuada, la modularidad y la capacidad de realizar cambios sin 
causar efectos secundarios no deseados.
* **Portabilidad:** Se refiere a la capacidad del software para ejecutarse en diferentes plataformas y entornos sin 
necesidad de modificaciones significativas. Esto puede incluir sistemas operativos, bases de datos, navegadores web y dispositivos.

----

<!-- .slide: style="font-size: 0.80em" -->
* **Escalabilidad:** Se refiere a la capacidad del software para adaptarse a un aumento en la carga de trabajo sin una 
degradación significativa del rendimiento. Esto es esencial para garantizar que el sistema pueda crecer con la demanda 
sin necesidad de una reescritura importante.
* **Usabilidad:** Es un aspecto importante de la experiencia del usuario. Implica la facilidad de uso, la navegación 
intuitiva y la capacidad de los usuarios para completar sus tareas de manera eficiente.

----

<!-- .slide: style="font-size: 0.80em" -->
* **Cumplimiento normativo:** Algunas aplicaciones deben cumplir con regulaciones y estándares específicos, como GDPR 
para la privacidad de datos o HIPAA para la salud. Los requerimientos de cumplimiento normativo aseguran que el software 
cumpla con estas regulaciones.
* **Eficiencia en el uso de recursos:** Se refiere a la optimización de recursos como el consumo de energía, 
el ancho de banda de red o el espacio de almacenamiento.

----

Estos son solo algunos ejemplos de Requerimientos No Funcionales que deben ser considerados al desarrollar un producto 
de software. La identificación y gestión adecuada de estos requerimientos son esenciales para garantizar que el software 
cumpla con las expectativas del cliente y las necesidades del negocio, además de proporcionar una experiencia de usuario 
sólida y confiable.

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
