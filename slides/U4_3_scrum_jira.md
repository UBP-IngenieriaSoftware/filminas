---
title: Desarrollo Ágil de Software
theme: solarized
slideNumber: true
---

# Ingeniería de Software
## Scrum
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
</style>
## Temario
<div class="grid-item">

### Desarrollo Ágil de Software
* Scrum: Definición
* Roles

</div>

---
### Scrum
Esta metodología se lleva adelante en “Sprints”. Al final de cada sprint, el equipo debe entregar una versión mejorada 
del proyecto para que sea analizada por todos los interesados; luego de eso, los evaluadores dan una devolución, lo 
que da inicio al proceso de mejora.

---
### Scrum
![Scrum](images/unidad4/scrum.webp)

---
### Scrum: Roles

<!-- .slide: style="font-size: 0.90em" -->

Los equipos de Scrum son auto-organizados y multifuncionales. Es decir, cada uno es responsable de unas tareas 
determinadas y de terminarlas en los tiempos acordados. Esto garantiza la entrega de valor del equipo completo, 
sin necesidad de ayuda o la supervisión minuciosa de otros miembros de la organización.

Al ser equipos multifuncionales, requiere de múltiples roles:
* Scrum Master
* Product Owner
* Equipo de Desarrollo (Dev. Front, Dev. Backend, QA)

---
### Rol: Product Owner
Es el responsable de maximizar el valor del trabajo, que viene de la mano de una buena gestión del Product Backlog.

El Product Owner es el único perfil que habla constantemente con el cliente, lo que le obliga a tener muchos 
conocimientos sobre el negocio.

---
### Rol: Scrum Master
Es el responsable de que las técnicas Scrum sean comprendidas y aplicadas en la organización. Es el manager de Scrum, 
un líder que se encarga de eliminar impedimentos o inconvenientes que tenga el equipo dentro de un sprint, aplicando 
las mejores técnicas para fortalecer el equipo.

Dentro de la organización, el Scrum Master tiene la labor de ayudar en la adopción del framework en todos los equipos.

---
### Rol: Equipo de desarrollo
Son los encargados de realizar las tareas priorizadas por el Product Owner. Es un equipo multifuncional y 
auto-organizado. Son los únicos que estiman las tareas del product backlog, sin dejarse influenciar por nadie.

Los equipos de desarrollo no tienen sub-equipos o especialistas. La finalidad de esto es transmitir la 
responsabilidad compartida si no se llegan a realizar todas las tareas de un sprint.

---
### Rol: UX
Son los encargados de realizar el diseño de la aplicación. Suelen conocer en profundidad el negocio, para poder realizar el diseño acorde a las necesidades del cliente.

Emplean herramientas como:
* Figma
* Adoba XD

---
### Scrum: Artefactos
* Product Backlog
* Sprint Backlog
* Incremento

---
### Product Backlog

<!-- .slide: style="font-size: 0.90em" -->

Listado de tareas que engloba todo un proyecto. Cualquier cosa que debamos hacer debe estar en el Product Backlog y 
con un tiempo estimado por el equipo de desarrollo.

La responsabilidad de ordenar este Backlog es del Product Owner, que se encuentra en constante comunicación con el 
cliente para asegurarse de que las prioridades están bien establecidas.

Las tareas que están más arriba deben de ser las de mayor prioridad. El equipo de desarrollo elige tareas del 
Product Backlog en el Sprint Planning para generar tanto el Sprint Backlog como el Sprint Goal.

---
### Sprint Backlog
Es el grupo de tareas del Product Backlog que el equipo de desarrollo elige en el Sprint Planning junto con el plan 
para poder desarrollarlas. Debe ser conocido por todo el equipo, para asegurarse de que el foco debe estar en este grupo de tareas.

El Sprint Planning no cambia durante el sprint, solo se permite cambiar el plan para poder desarrollarlas.

---
### Incremento
El Product Increment es el resultado de sumar todos los elementos del Product Backlog completados durante el sprint 
actual, añadiendo también el valor de todos los sprints anteriores.

La suma de los incrementos se presenta en cada Sprint Review, y se pueden crear varios incrementos de Scrum dentro de un mismo sprint.

---
### Ejercicio Product Backlog
1. Ingresa a Jira: [https://ubp2.atlassian.net](https://ubp2.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog)
2. Crea tickets/tareas con los ejercicios a realizar. Puedes ordenarlos por orden de prioridad.

---
### Scrum: Ceremonias

<!-- .slide: style="font-size: 0.90em" -->

Todas las **ceremonias** o **eventos** están enmarcadas o contenidas en un sprint.

Un sprint es un período de tiempo en el cuál se va a realizar la entrega de software. Habitualmente suele ser de 2 semanas.

Las ceremonias más habituales son:
* Sprint Planning
* Daily Meeting
* Sprint Review o Demo
* Retrospectiva
* Refinamiento

---
### Ceremonias: Sprint Planning
En esta reunión todo el equipo Scrum define qué tareas se van a abordar y cuál será el objetivo del sprint.

El equipo se hace las siguientes preguntas:
¿Qué se va a hacer en el sprint? En base a ello, se eligen tareas del Product Backlog.
¿Cómo lo vamos a hacer? El equipo de desarrollo define las tareas necesarias para completar cada ítem elegido del Product Backlog.
La definición de qué se va a hacer implica que el equipo tenga un objetivo y se encuentre comprometido con la entrega de 
valor que se hará al cliente al final del sprint. A esto se le llama Sprint Goal.

---
### Ceremonias: Daily Meeting

<!-- .slide: style="font-size: 0.90em" -->

Es una reunión diaria dentro del sprint que tiene como máximo 15 minutos de duración. En ella deben participar el equipo 
de desarrollo y el Scrum Master. El Product Owner no tiene la necesidad de estar presente.

En esta reunión diaria el equipo de desarrollo hace las siguientes 3 preguntas:
¿Qué hice ayer?
¿Qué voy a hacer hoy?
¿Tengo algún impedimento que necesito que me solucionen?

Una Daily Scrum es el lugar más oportuno para poder inspeccionar el trabajo y poder adaptarse en caso de que haya cambio 
de tareas dentro de un sprint.

---
### Ceremonias: Sprint Review o Demo
La review del valor que vamos a entregar al cliente se hace en esta reunión, al final de cada sprint. Suele asistir el 
cliente para ver los avances del proyecto.

En esta reunión el Product Owner presenta lo desarrollado al cliente y el equipo de desarrollo muestra su funcionamiento. 
El cliente valida los cambios realizados y además brinda feedback sobre nuevas tareas que el Product Owner tendrá que 
agregar al Product Backlog.

---
### Ceremonias: Sprint Retrospective
Es la reunión del equipo en la que se hace una evaluación de cómo se ha implementado el último sprint.

Es una gran oportunidad para el equipo Scrum de inspeccionarse a sí mismo, proponiendo mejoras para el siguiente sprint. 
El resultado es una lista de mejoras que debe aplicar el siguiente día, ya que al finalizar la retrospectiva, 
inmediatamente comienza un nuevo sprint, que incluye los mismos eventos mencionados anteriormente.

---
### Ceremonias: Refinamiento o Grooming
Es el tiempo de revisión que se dedica dentro de los equipos durante los sprints para refinar los requerimientos.

Las tareas de usuario se revisan con un par de sprints de ventaja para que cuando llegue el equipo ya esté todo listo 
para el desarrollo de la tarea.

---
### Ejercicio Planning
La idea es hacer una “simulación” de una planning.

La profe tomará el rol de “Scrum Master”, y se procederá a asignar las tareas a las diferentes personas del equipo.

Además, se emplearán técnicas de estimación.

---
### Estimación

<!-- .slide: style="font-size: 0.90em" -->

Si bien la estimación no tiene reglas generales para todos los equipos, habitualmente, los tiempos que se suelen asignar son:

<!-- .slide: style="font-size: 0.60em" -->
<!--
| Puntos  | Tiempo Estimado  | Notas                                         |
|:--------|:-----------------|:----------------------------------------------|
| 1       | 2hs o menos      | Tamaño de tarea ideal                         |
| 2       | de 2 a 4hs       | Tamaño de tarea ideal                         |
| 3       | Hasta 1 día      | Tamaño de tarea ideal                         |
| 5       | 1,5 a 2 días     | Tratar de dividir en 2 tareas                 |
| 8       | 3 a 5 días       | Tratar de dividir en 2 ó 3 tareas             |
| 13      | 5 a 8 días       | Si o SI debe dividirse en tareas más pequeñas |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Puntos</th>
<th style="text-align:left">Tiempo Estimado</th>
<th style="text-align:left">Notas</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">1</td>
<td style="text-align:left">2hs o menos</td>
<td style="text-align:left">Tamaño de tarea ideal</td>
</tr>
<tr>
<td style="text-align:left">2</td>
<td style="text-align:left">de 2 a 4hs</td>
<td style="text-align:left">Tamaño de tarea ideal</td>
</tr>
<tr>
<td style="text-align:left">3</td>
<td style="text-align:left">Hasta 1 día</td>
<td style="text-align:left">Tamaño de tarea ideal</td>
</tr>
<tr>
<td style="text-align:left">5</td>
<td style="text-align:left">1,5 a 2 días</td>
<td style="text-align:left">Tratar de dividir en 2 tareas</td>
</tr>
<tr>
<td style="text-align:left">8</td>
<td style="text-align:left">3 a 5 días</td>
<td style="text-align:left">Tratar de dividir en 2 ó 3 tareas</td>
</tr>
<tr>
<td style="text-align:left">13</td>
<td style="text-align:left">5 a 8 días</td>
<td style="text-align:left">Si o SI debe dividirse en tareas más pequeñas</td>
</tr>
</tbody>
</table>


---
### Ejercicio: Ejecutar la tarea
Cada persona debe realizar la tarea que se le asignó (10min de tiempo se dejará para hacerlo).

Cuando empiezas a realizar tu tarea, debes moverla de columna en Jira…Y pasarla a en progreso.

---
### Ejercicio: Ceremonia Daily
Hagamos de cuenta que pasó un día, y debemos notificar en una “Daily” lo que pasó el día anterior:

Alguien tomará el papel de “Scrum Master”, y cada persona del equipo debe informar en la reunión sobre:
* ¿En que trabajaste ayer?
* ¿En qué trabajaras hoy?
* ¿Tienes algún problema con tu tarea?

---
### Ejercicio: Ceremonia Demo
Hagamos de cuenta que pasaron las 2 semanas (el sprint), y se debe mostrar de forma rápida un resumen de en que se trabajó:

Alguien tomará el papel de “Scrum Master”, y cada persona del equipo debe mostrar brevemente su pantalla, e indicar en 
qué pruebas realizó, que funcionalidad o componente probó.

---
### Ejercicio: Ceremonia Retro
Hagamos de cuenta que pasaron las 2 semanas (el sprint), y se debe evaluar el resultado del sprint:

Alguien tomará el papel de “Scrum Master”, y cada persona del equipo debe participar de la ceremonia empleando:

[Tablero de Retro](https://easyretro.io/publicboard/DjiIuVtUvCTMCCU8Tas0zQW4e5r1/37f26b42-0af9-4985-9e14-aa130b5f21b1)

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
