---
title: Ingenieria de Sistemas
theme: solarized
slideNumber: true
---

#### Ingeniería de Software

### Unidad II

# Ingeniería de Sistemas

Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

---

## Temario
 
### Ingeniería de Sistemas

- Ingeniería de Sistemas
- Arquitectura de Sistemas
- Definición de Requerimientos
- Diseño de Sistemas
- Modelado de Sistemas

---

### Ingeniería de Sistemas

La **Ingeniería de Sistemas** es la disciplina que se ocupa de analizar, diseñar, desarrollar y mantener sistemas complejos, considerando no solamente el software, sino también las personas, los procesos, el hardware, los datos, las comunicaciones y el entorno en el que el sistema funciona.

Su objetivo es lograr que todos estos elementos trabajen de manera coordinada para satisfacer determinadas necesidades.

----

### Ingeniería de Sistemas
En el caso de un sistema informático, la Ingeniería de Sistemas permite responder preguntas como:

- ¿Qué problema se quiere resolver?
- ¿Quiénes utilizarán el sistema?
- ¿Qué funciones debe proporcionar?
- ¿Con qué otros sistemas debe interactuar?
- ¿Qué restricciones existen?
- ¿Cómo se organizarán sus diferentes componentes?
- ¿Cómo se garantizarán aspectos como seguridad, rendimiento y disponibilidad?


----

### Ingeniería de Sistemas
Por lo tanto, tiene una visión global del sistema y no se limita exclusivamente a programar.

---

### Sistema

Un sistema es un conjunto de elementos relacionados entre sí que interactúan para alcanzar determinados objetivos.

---

### Propiedades de los sistemas
<!-- .slide: style="font-size: 0.90em" -->
- **Complejidad:** La cantidad de elementos y relaciones puede hacer difícil comprender el comportamiento global.
- **Emergencia:** El comportamiento del sistema puede surgir de la interacción de sus componentes y no estar presente en ninguno de ellos individualmente.
- **Interacción:** Los componentes dependen unos de otros.
- **Evolución:** Los sistemas pueden cambiar con el tiempo debido a: nuevos requerimientos, 
cambios tecnológicos, cambios legales, cambios organizacionales, cambios en los usuarios.
- **Restricciones:** El sistema debe funcionar dentro de determinadas limitaciones: presupuesto
tiempo, tecnología, legislación, infraestructura, seguridad.

---

### Arquitectura de Sistemas

La **Arquitectura de Sistemas** define la estructura general del sistema y la forma en que sus principales componentes se organizan y se relacionan.

La arquitectura proporciona una **visión de alto nivel**. Todavía no describe todos los detalles de implementación.

----

### Arquitectura de Sistemas
Se ocupa de establecer, entre otras cosas:

- cuáles serán los principales componentes del sistema
- qué responsabilidades tendrá cada componente
- cómo se comunicarán entre sí
- qué tecnologías o mecanismos pueden utilizarse
- dónde se ejecutará cada componente
- cómo se integrará el sistema con otros sistemas

----

### Decisiones arquitectónicas
<!-- .slide: style="font-size: 0.80em" -->
Una arquitectura implica tomar decisiones importantes.

- ¿Sistema monolítico o distribuido?
- ¿Cliente-servidor?
- ¿Arquitectura en capas?
- ¿Microservicios?
- ¿Aplicación web o móvil?
- ¿Base de datos centralizada o distribuida?
- ¿Comunicación síncrona o asíncrona?
- ¿Dónde se procesarán los datos?
- ¿Cómo se garantizará la seguridad?
- ¿Cómo se manejarán los errores?

Estas decisiones pueden ser difíciles de modificar posteriormente.

Por eso las decisiones arquitectónicas son decisiones de alto impacto.

---

### Definición de Requerimientos del Sistema

La **Definición de Requerimientos** del Sistema consiste en determinar y documentar qué debe hacer el sistema y bajo qué condiciones debe funcionar.

Los requerimientos representan las necesidades de los usuarios, clientes y demás partes interesadas.

----

### Definición de Requerimientos del Sistema

Podemos clasificarlos, por ejemplo, en:

- Requerimientos funcionales
- Requerimientos no funcionales

----

### Definición de Requerimientos del Sistema
**Requerimientos funcionales** 
Describen servicios o funciones que el sistema debe proporcionar.

Ejemplo:
El sistema deberá permitir que un usuario registre una cuenta utilizando su dirección de correo electrónico.

----

### Definición de Requerimientos del Sistema
**Requerimientos no funcionales** 

Describen restricciones o características de calidad del sistema.

El sistema deberá responder a las solicitudes de los usuarios en menos de 2 segundos bajo condiciones normales de operación.

----

### Definición de Requerimientos No funcioanles del Sistema
También pueden existir restricciones relacionadas con:

- legislación
- hardware
- tecnologías
- seguridad
- presupuesto
- organización
- interoperabilidad

----

### Definición de Requerimientos del Sistema
El resultado de esta actividad debería permitir establecer qué se espera del sistema, independientemente de cómo se vaya a construir.

---

### Diseño de Sistemas

El Diseño de Sistemas transforma los requerimientos en una descripción más detallada de cómo se construirá el sistema.

Mientras que los requerimientos responden principalmente:
**¿Qué debe hacer el sistema?** el diseño comienza a responder **¿Cómo se organizará y construirá el sistema para hacerlo?**

----

### Diseño de Sistemas
El diseño puede incluir aspectos como:

- diseño de componentes
- diseño de módulos
- diseño de interfaces
- diseño de bases de datos
- diseño de clases
- diseño de algoritmos
- diseño de comunicaciones
- diseño de interfaces de usuario
- mecanismos de seguridad

----

### Principios de diseño

- abstracción
- modularidad
- encapsulamiento
- separación de responsabilidades
- bajo acoplamiento
- alta cohesión
- reutilización
- ocultamiento de información

---

### Modelado de Sistemas

El Modelado de Sistemas consiste en representar un sistema mediante modelos que permiten comprender, analizar, comunicar y documentar diferentes aspectos del mismo.

Un modelo es una representación simplificada de una parte de la realidad.

----

<!-- .slide: style="font-size: 0.90em" -->
### Modelado de Sistemas
Por ejemplo, podemos utilizar:

- diagramas de **casos de uso** para representar funcionalidades y actores
- diagramas de **clases** para representar la estructura del software
- diagramas de **secuencia** para representar interacciones
- diagramas de **actividades** para representar procesos
- diagramas de **estados** para representar comportamientos
- diagramas de **componentes** para representar la organización del software
- diagramas de **despliegue** para representar dónde se ejecutan los componentes

----

### Modelado de Sistemas
El modelado no necesariamente significa que estemos programando. Los modelos sirven para pensar y comunicar cómo funciona o cómo estará construido el sistema.
---

<!-- .slide: style="font-size: 0.60em" -->

<table>
<thead>
<tr>
<th>Concepto</th>
<th>Pregunta principal</th>
<th>Resultado</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Ingeniería de Sistemas</strong></td>
<td>¿Cómo abordamos el sistema como un todo?</td>
<td>Visión integral</td>
</tr>
<tr>
<td><strong>Requerimientos</strong></td>
<td>¿Qué necesita el sistema?</td>
<td>Especificación de necesidades</td>
</tr>
<tr>
<td><strong>Arquitectura</strong></td>
<td>¿Cómo organizamos sus grandes componentes?</td>
<td>Estructura de alto nivel</td>
</tr>
<tr>
<td><strong>Diseño</strong></td>
<td>¿Cómo construiremos sus componentes?</td>
<td>Diseño detallado</td>
</tr>
<tr>
<td><strong>Modelado</strong></td>
<td>¿Cómo representamos y comunicamos el sistema?</td>
<td>Modelos y diagramas</td>
</tr>
</tbody>
</table>

---

## ¿Dudas, Preguntas, Comentarios?

![DUDAS](images/pregunta.gif)
