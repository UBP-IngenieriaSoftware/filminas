---
title: Casos de Pruebas
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Casos de Pruebas
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

### Casos de Pruebas
* Casos de Prueba: Definición
* Plantilla de Casos de Prueba
* Casos de Uso
* Identificador de caso de uso
* Identificador de la prueba
* Nombre del Caso de Uso
* Descripción de la Prueba
* Informador
* Responsable

</div>
<div class="grid-item">

* Fecha de la Prueba
* Prerrequisitos
* Entrada/s
* Detalle de la Prueba
* Detalle de lo que se Prueba
* Resultado esperado
* Resultado obtenido
* Funcionamiento
* Comentarios
* Resultado
* En la práctica...

</div>
</div>

---

### Casos de Prueba
En la norma ISO 29119 (Estándar Internacional para pruebas de Software) se define caso de prueba como:

Un conjunto de precondiciones, entradas y resultados esperados, desarrollados para impulsar la ejecución de un elemento 
de prueba para cumplir con los objetivos de la prueba, incluyendo la implementación correcta, la identificación de 
errores, el chequeo de la calidad y otras informaciones valiosas.


---

## Plantilla de Casos de Pruebas
<!-- .slide: style="font-size: 0.90em" -->
Es una descripción detallada de cómo se debe probar una funcionalidad o característica específica de una aplicación o 
sistema. 

Los casos de prueba son parte fundamental de las pruebas de software y tienen varios propósitos y beneficios importantes:
1. **Verificación de la calidad:** Los CP ayudan a garantizar que una aplicación o sistema funcione correctamente y 
cumpla con los requisitos establecidos. Al ejecutar pruebas exhaustivas, se pueden detectar y corregir errores y 
problemas antes de que lleguen a los usuarios finales.

----

## Plantilla de Casos de Pruebas
<!-- .slide: style="font-size: 0.80em" -->
2. **Documentación:** Los CP actúan como documentación detallada de cómo se debe probar una funcionalidad. Esto es útil 
para los equipos de desarrollo y pruebas, ya que proporciona instrucciones claras sobre qué se debe probar y cómo hacerlo.
3. **Automatización:** Los CP son esenciales para la automatización de pruebas. Pueden ser traducidos a scripts de 
pruebas automatizadas que permiten ejecutar las pruebas de forma repetitiva y consistente, lo que ahorra tiempo y 
recursos a largo plazo.
4. **Validación de cambios:** Cuando se realizan cambios en una aplicación o sistema, los CP existentes pueden utilizarse 
para verificar que las modificaciones no hayan introducido nuevos errores y que las funcionalidades existentes sigan 
funcionando como se espera.

----

## Plantilla de Casos de Pruebas
<!-- .slide: style="font-size: 0.80em" -->
5. **Reproducción de errores:** Los CP permiten a los equipos de desarrollo y pruebas reproducir errores informados por 
los usuarios. Esto facilita la identificación y corrección de problemas específicos.
6. **Estándares de calidad:** Los CP son una parte fundamental de los estándares de calidad en el desarrollo de software. 
Ayudan a mantener la coherencia en las pruebas y a garantizar que todas las funcionalidades se evalúen de manera adecuada.
7. **Mejora de la confiabilidad:** Al realizar pruebas sistemáticas y controladas, se mejora la confiabilidad y 
estabilidad del software, lo que reduce la probabilidad de fallos inesperados y garantiza una mejor experiencia para los usuarios.

---

![Plantilla de Caso de Prueba](images/unidad8/plantilla_caso_de_prueba.jpg)

---
### A tener en cuenta...

Los **casos de uso** y los **casos de prueba** NO son lo mismo.

---

### Caso de Uso
<!-- .slide: style="font-size: 0.80em" -->
* **Definición:** Un caso de uso es una descripción detallada de cómo un usuario o un actor interactúa con un sistema de 
software para lograr un objetivo específico. Los casos de uso se utilizan para modelar y documentar las interacciones 
entre el sistema y sus usuarios o actores externos.
* **Enfoque:** Los casos de uso se centran en la funcionalidad y la interacción desde una perspectiva de alto nivel. 
Describen las acciones que los usuarios pueden realizar en el sistema y cómo el sistema responde a esas acciones.
* **Objetivos:** Los casos de uso ayudan a comprender los requisitos del sistema, la lógica del flujo de trabajo y la 
interacción del usuario. También son útiles para la comunicación entre los miembros del equipo y los stakeholders del proyecto.

---
### Caso de Prueba (Test Case)
<!-- .slide: style="font-size: 0.80em" -->
* **Definición:** Un caso de prueba es una descripción detallada de una condición o escenario específico que debe 
probarse en una aplicación o sistema de software. Los casos de prueba se utilizan para verificar si una determinada 
funcionalidad del software funciona como se esperaba.
* **Enfoque:** Los casos de prueba se centran en verificar una funcionalidad específica del software y en determinar si 
produce los resultados correctos bajo ciertas condiciones.
* **Objetivos:** Los casos de prueba son una parte fundamental del proceso de pruebas de software. Ayudan a identificar 
errores y problemas en el software y a garantizar que cumpla con los requisitos y las especificaciones.

---
### Plantilla de casos de Prueba
<!-- .slide: style="font-size: 0.70em" -->
Idealmente debe contener los siguientes campos:
* Identificador de caso de uso
* Nombre de caso de uso
* Identificador de la prueba
* Descripción de la Prueba
* Responsable
* Fecha de la Prueba
* Prerrequisitos
* Entrada/s
* Detalle de la Prueba
* Detalle de que se Prueba
* Resultado esperado
* Resultado obtenido
* Funciona / No Funciona / Requiere mantenimiento perfectivo
* Comentarios
* Resultado: ACEPTADO / NO ACEPTADO

---
### Identificador de caso de uso e Identificador de la prueba
<!-- .slide: style="font-size: 0.60em" -->
El **ID** es una etiqueta o número único que se asigna a un CU ó Test en la documentación de un sistema de software. 
Su propósito principal es proporcionar una forma rápida y sencilla de identificar y referirse a casos de uso ó tests específicos 
dentro de un sistema o proyecto.

Los identificadores de son útiles para varias finalidades:
* **Organización:** Especialmente proyectos grandes y complejos, donde suelen existir numerosos casos de uso ó tests. 
Los identificadores ayudan a organizarlos y a mantener un seguimiento de cada uno.
* **Referencia rápida:** Es más sencillo hacer referencia a un caso de uso o test en la documentación, en conversaciones con 
otros miembros del equipo o en el código fuente.
* **Seguimiento de cambios:** Cuando se realizan modificaciones o actualizaciones en un proyecto, los identificadores 
permiten realizar un seguimiento más eficaz de los casos de uso o tests afectados por esos cambios.
* **Facilitar la comunicación:** Los identificadores proporcionan un lenguaje común y estandarizado que facilita la 
comunicación entre los miembros del equipo de desarrollo, los diseñadores, los probadores y otros interesados en el proyecto.

----

### Identificador de caso de uso e Identificador de la prueba
<!-- .slide: style="font-size: 0.90em" -->
Un identificador de caso de uso puede ser una etiqueta alfanumérica única o un número, y a menudo se organiza de manera 
estructurada para reflejar la jerarquía o el flujo de trabajo de un sistema. Por ejemplo, podría tener un formato como 
"CU-001" para el primer caso de uso de un sistema, "CU-002" para el segundo, y así sucesivamente. Y de manera similar
para los tests "TST-001", "TST-002".

La elección del formato y la convención de nomenclatura dependen de las prácticas específicas de documentación adoptadas 
por el equipo de desarrollo.

---

### Nombre del Caso de Uso
Sirve para identificar y describir brevemente el propósito o la funcionalidad que se está modelando en ese caso de uso 
específico. 

Se suele utilizar una etiqueta o título corto que ayuda a los miembros del equipo de desarrollo, probadores y otros 
stakeholders del proyecto a comprender rápidamente de qué se trata el caso de uso. 

----

### Nombre del Caso de Uso
<!-- .slide: style="font-size: 0.80em" -->
Los principales propósitos del nombre son:
* **Identificación:** El nombre del caso de uso es una forma rápida de identificar un CU particular dentro de la 
documentación del sistema. Proporciona un nombre único y distintivo que facilita la referencia y la comunicación entre 
los miembros del equipo.
* **Clarificación del Propósito:** El nombre del CU proporciona una descripción concisa del propósito o la funcionalidad 
que el caso de uso representa. Esto ayuda a responder la pregunta "¿Qué hace este caso de uso?" sin necesidad de una 
descripción detallada.

----

### Nombre del Caso de Uso
<!-- .slide: style="font-size: 0.80em" -->
* **Comunicación Efectiva:** El nombre del CU actúa como un medio de comunicación eficiente al proporcionar un resumen 
rápido y legible de la funcionalidad que se está abordando.
* **Búsqueda y Referencia:** Permite a los miembros del equipo buscar y hacer referencia rápidamente a un CU específico 
cuando sea necesario.
* **Contextualización:** Ayuda a poner en contexto el CU en el flujo general de trabajo o el comportamiento del sistema. 
El nombre debe ser lo suficientemente descriptivo para que otros puedan entender su función sin tener que leer toda la 
documentación detallada.

---

### Descripción de la Prueba
<!-- .slide: style="font-size: 0.70em" -->
Proporciona una explicación breve pero clara de lo que se está probando en ese caso en particular. 

* **Claridad:** Ayuda a comprender de manera rápida y concisa qué funcionalidad o característica del software se está 
evaluando en ese caso de prueba en particular.
* **Comunicación:** Facilita la comunicación entre los miembros del equipo de prueba, los desarrolladores y otros 
interesados en el proyecto al proporcionar un contexto claro sobre el caso de prueba.
* **Rastreabilidad:** Permite rastrear y relacionar cada caso de prueba con los requisitos o las especificaciones del 
software. Esto es útil para garantizar que todos los aspectos requeridos del software se estén probando adecuadamente.
* **Organización:** Ayuda a mantener una estructura coherente y organizada en la documentación de los casos de prueba, 
lo que facilita la gestión y la revisión de los mismos.

---

### Informador
Se especifica quién es la persona o el equipo que documentó la prueba a realizar. 

---
### Responsable
Se especifica quién es la persona o el equipo encargado de ejecutar la prueba. Es importante para asignar la 
responsabilidad de ejecutar y documentar la prueba.

---
### Fecha de la Prueba
Se registra cuándo se realizó la prueba. Esto es crucial para llevar un registro de cuándo se ejecutó el caso de prueba 
y para rastrear el progreso del proceso de pruebas.
En algunos sistemas habitual tener múltiples campos tipo fecha: Fecha de Creación, Fecha de Última Modificación, FechaS
de ejecuciones, etc.

---
### Prerrequisitos
Los prerrequisitos enumeran las condiciones o configuraciones necesarias que deben estar en su lugar antes de ejecutar 
el caso de prueba. Ayudan a garantizar que el entorno de prueba sea adecuado y que no falte ningún elemento necesario.

---
### Entrada/s
Este campo describe los datos de entrada que se utilizarán para ejecutar la prueba. Es importante especificar los 
valores, archivos o información requerida para llevar a cabo la prueba.

---
### Detalle de la Prueba
El detalle de la prueba proporciona una descripción general de lo que se va a probar y los objetivos de la prueba. 
Ofrece un contexto más amplio para comprender la prueba en su conjunto.

---
### Detalle de lo que se Prueba
Este campo se enfoca en los aspectos específicos o las características que se están probando en este caso de prueba en 
particular. Ayuda a definir claramente el alcance de la prueba.

---
### Resultado esperado
Aquí se especifican los resultados que se anticipan cuando la prueba se ejecuta correctamente. Estos resultados deben 
ser medibles y verificables.
Suele adjuntarse capturas del diseño de pantalla para clarificar como debe visualizarse (UI), o esquemas de la respuesta
del servicio.

---
### Resultado obtenido
Después de ejecutar la prueba, este campo se utiliza para registrar los resultados reales observados. Comparar el 
resultado obtenido con el resultado esperado permite determinar si la prueba fue exitosa o no.
Suele adjuntarse capturas de pantalla de cómo se visualiza la UI cuando se ejecuta la prueba.

---
### Funciona / No Funciona / Requiere mantenimiento perfectivo
Este campo indica si el caso de prueba funciona según lo esperado, no funciona (en caso de fallo) o si se requiere 
realizar ajustes o mejoras en el software (mantenimiento perfectivo).

---
### Comentarios
Los comentarios permiten agregar información adicional, aclaraciones o detalles relevantes relacionados con la ejecución 
de la prueba. Pueden ser útiles para proporcionar contexto adicional o explicar situaciones específicas.

---
### Resultado: ACEPTADO / NO ACEPTADO
Al finalizar la ejecución de la prueba, este campo indica si el caso de prueba se considera aceptado (cumple con los 
criterios de aceptación) o no aceptado (falló en algún aspecto).

---
### Cómo se suele realizar en la práctica?
Se suele emplear **Jira**, **Azure** o cualquier herramienta de tickets, que permita crear incidencias de tipo **test**.

---

![Jira 1](images/unidad8/jira1.jpg)

---

![Jira 2](images/unidad8/jira2.jpg)

---

![Jira Ejemplo 1](images/unidad8/jira-ejemplo1.jpg)

---

![Jira Ejemplo 2](images/unidad8/jira-ejemplo2.jpg)

---

![Jira Ejemplo 3](images/unidad8/jira-ejemplo3.jpg)

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
