---
title: Introduccion
theme: solarized
slideNumber: true
---

# Ingeniería de Software
## Introducción
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

### Ingeniería de Software
* Definición
* Tipos de Drivers
* Desarrolladores de Drivers
* Actualización
* Descarga
* Windows: Administrador de dispositivos
* Linux: Hardware Map
</div>

---
## Ingenieria de Software
La ingeniería de software aplica teorías, métodos y herramientas para el desarrollo de software profesional.

---
## Ingenieria de Software. Por que?
* La economía de muchos países depende en alguna medida del software.
* Cada vez mas sistemas son controlados por software.
* El gasto en software representa una fracción significativa del PBI
* Los errores de software pueden ser muy caros

---
## Errores de Software
* El primer “bug”, una polilla entre los relés del Mark II en 1947.
* Los errores en el software son un problema común y...en muchos casos, no hay graves consecuencias, 
se soluciona con una nueva versión corregida
* EN MUCHOS OTROS CASOS PUEDE HABER CONSECUENCIAS FATALES, GRAVES O MUY CARAS.

---
### Algunos "Grandes Errores" de Software...
#### LA EXPLOSIÓN DEL ARIANE 5
1000 millones de dólares perdidos

¿El problema? reutilización de código.
Se reutilizó el código del  Ariane 4.
El código asignaba el valor de una variable de 64 bits a una de 16 bits
Lo que no era un problema en el Ariane 4, destruyó el Ariane 5


16 bits: −32.768 a 32.767

64 bits: −9.223.372.036.854.775.808 a 9.223.372.036.854.775.807

---
#### LA EXPLOSIÓN DEL ARIANE 5
<iframe width="560" height="315" src="https://www.youtube.com/embed/gp_D8r-2hwk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---
### Algunos "Grandes Errores" de Software...
#### EXCESO DE RADIACIÓN EN EL THERAC-25
<!-- .slide: style="font-size: 0.80em" -->
Mato a 5 pacientes

La máquina de radiación Therac-25 aplicó un exceso de radiación a varios pacientes provocando la muerte de al menos cinco de ellos.

¿ La causa?
El control de la concurrencia de las rutinas que se ejecutaban en paralelo.

UNA clásica RACE CONDITION

Si bien la interfaz indicaba que todo iba bien, los pacientes estaban recibiendo 125 veces más radiación que lo indicado.

---
#### EXCESO DE RADIACIÓN EN EL THERAC-25
![Therac-25](images/unidad1/therac-25.jpg)

---
### Algunos "Grandes Errores" de Software...
#### MARS CLIMATE ORBITER
<!-- .slide: style="font-size: 0.80em" -->
Un error de unidades

El sistema de control de la nave en la Tierra usaba el sistema métrico anglosajón

El sistema de navegación de la nave esperaba valores en el sistema métrico decimal.

La trayectoria de la nave se acerco a Marte y fue desintegrada por la fuerza de fricción atmosférica del planeta.

Se incumplieron  los requisitos del sistema donde se especificaba que todo el software debía usar el sistema métrico decimal

---
#### MARS CLIMATE ORBITER
![Mars Climate Orbiter](images/unidad1/mars_climate_orbiter.webp)

---
### Algunos "Grandes Errores" de Software...
#### DESPLIEGUE DE UNA VERSIÓN INCORRECTA
<!-- .slide: style="font-size: 0.80em" -->
Mas de 400 millones de U$S perdidos en 45 minutos

El grupo Knight Capital perdió 460 millones de dólares en menos de una hora.

Se desplego una nueva versión sin modificar la configuración del algoritmo.

Hubo 4 millones de operaciones en 45 minutos

Se ejecuto en modo test, donde, para probar el comportamiento en condiciones extremas, estaban desactivadas las restricciones.
El sistema comenzó a comprar y vender acciones sin evaluar las consecuencias.

---
#### DESPLIEGUE DE UNA VERSIÓN INCORRECTA
<!-- .slide: style="font-size: 0.80em" -->
![Knight Capital](images/unidad1/Knight_Capital.jpg)

---
### Costos del software

El costo del software suele ser mayor que el costo del hardware.

El mantenimiento del software cuesta más que el desarrollo del mismo.
Para sistemas que tienen una larga vida, los costos de mantenimiento superan ampliamente los costos de desarrollo.

La ingeniería de software tiene que ver con el desarrollo de software rentable.

---
### Productos de software

* **Productos genéricos**
Sistemas que se comercializan y venden a cualquier cliente:
Ejemplos - Software para gráficos, herramientas de gestión de proyectos; Software CAD; software para mercados específicos
(Sistema de turno para dentista)

* **Productos personalizados**
Software que encarga un cliente específico para satisfacer sus propias necesidades.
Ejemplos - Sistema de control o monitoreo, software de control del tráfico aéreo, etc.

---
### Especificaciones del producto

* **Productos Genéricos**
La especificación de lo que el software debe hacer es propiedad del desarrollador del software y las decisiones sobre 
los cambios en el software son hechas por el desarrollador.

* **Productos personalizados**
La especificación de lo que el software debe hacer es propiedad del cliente del software y el es el que toma decisiones 
sobre los cambios de software necesarios.

---
### Preguntas sobre la ingeniería de Software
<!-- .slide: style="font-size: 0.80em" -->
* ¿Qué es software?
Programas de cómputo y documentación asociada.
Los productos de software se desarrollan para un cliente en particular o para un mercado general.

* ¿Cuáles son los atributos del buen software?
El buen software debe entregar al usuario la funcionalidad y el desempeño requeridos, y debe ser sustentable, confiable y utilizable.

* ¿Qué es ingeniería de Software?
La ingeneiría de software es una disciplina de la ingeniería que se interesa por todos los aspectos de la producción de software.

* ¿Cuáles son las actividades fundamentales de la ingeniería de software?
Especificación, desarrollo, validación y evolución del software.

---
### Preguntas sobre la ingeniería de Software
<!-- .slide: style="font-size: 0.90em" -->
* ¿Cuál es la diferencia entre ingeniería de software y ciencias de la computación?
Las ciencias de la computación se enfocan en teoría y fundamentos; mientras la ingeniería de software se enfoca en el
sentido práctico del desarrollo y en la distribución de software.

* ¿Cuál es la diferencia entre ingeniería de software e ingeniería de Sistemas?
La ingeniería de sistemas se interesa por todos los aspectos del desarrollo de sistemas basados en computadoras, incluidos
hardware, software e ingeniería de procesos. La ingeniería de software es parte de este proceso más general.

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
