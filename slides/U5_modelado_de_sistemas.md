---
title: Modelado de Sistemas
theme: solarized
slideNumber: true
---

# Ingeniería de Software
## Modelado de Sistemas
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

### Modelado de Sistemas
* Modelos de Sistemas
* Perspectivas del Sistema
* Tipos de Diagramas UML
* Uso de modelos gráficos
* Modelos de Contexto
* Límites del sistema
* Perspectiva del proceso
* Modelos de Interacción
* Modelado de Casos de Uso
</div>
<div class="grid-item">

* Diagramas de Secuencia
* Modelos Estructurales
* Diagramas de Clases
* Generalización
* Agregación
* Modelos de Comportamiento
* Modelado Impulsado por Datos
* Modelado Impulsado por Eventos
* Modelos de Máquina de Estado
* Ingeniería Dirigida por Modelos
</div>
</div>

---
### Modelado de Sistemas

<!--https://diagramasuml.com/-->

Un **modelo es una abstracción** de un sistema o entidad del mundo real. 

Una **abstracción es una simplificación**, que incluye sólo aquellos detalles relevantes para algún determinado propósito.

El modelado permite abordar la complejidad de los sistemas.

---
### El modelado de sistemas
* El modelado de sistemas es el proceso de elaboración de modelos abstractos de un sistema, con cada modelo que presenta 
una vista o perspectiva diferente de ese sistema.
* El modelado de sistemas se representa mediante algún tipo de notación gráfica, casi siempre basada en anotaciones en 
el Lenguaje Unificado de Modelado (UML).
* El modelado de sistemas ayuda al analista a entender la funcionalidad del sistema y se pueden utilizar modelos para 
comunicarse con los clientes.

----

### Modelos de sistemas
* Los modelos del sistema se utilizan durante la ingeniería de requisitos para ayudar a explicar los requisitos 
propuestos a otros actores del sistema. Los ingenieros utilizan estos modelos para discutir las propuestas de diseño y 
documentar el sistema de aplicación.
* En un proceso de ingeniería basado en modelos, es posible generar una implementación completa o parcial del sistema 
desde el modelo del sistema.

---

### Perspectivas del sistema
* Una **perspectiva externa**, donde se modela el contexto o el entorno del sistema.
* Una **perspectiva de interacción**, donde se modelan las interacciones entre un sistema y su entorno, o entre los 
componentes de un sistema.
* Una **perspectiva estructural**, donde se modela la organización de un sistema o de la estructura de los datos que son 
procesados por el sistema.
* Una **perspectiva conductual**, en la que se modela el comportamiento dinámico del sistema y la forma en que responde 
a los eventos.

----

### Ejemplo:
````java
package codemodel;
public class Guitarist extends Person implements MusicPlayer {
    Guitar favoriteGuitar;
      public Guitarist (String name) {super(name);}
            //A couple of local methods for accessing the class's properties
      public void setInstrument(Instrument instrument) {
            if(instrument instanceof Guitar){
                this.favoriteGuitar = (Guiter) instrument;
            } else {
                System.out.println("I'm not playing that thing!");
            }
      }
      public Instrument getInstrument() {return this.favoriteGuitar;}
}
````
* Representa sólo la lógica e ignora el resto
* El ser humano lo interpreta muy lentamente
* No facilita la reutilización ni la comunicación

---
````cookie
Guitarist es una clase que contiene seis miembros: 1 estático y 5
no estáticos. Guitarist usa, y por lo tanto necesita, una instancia 
de Guitar; Sin embargo, dado que esto podría compartirse con otras 
clases en su paquete, la variable de instancia Guitar, llamada 
favoritoGuitar, se declara como predeterminada.
Cinco de los miembros dentro de Guitarist son métodos. Cuatro no son 
estáticos. Uno de estos métodos es un constructor que toma un argumento, 
y las instancias de String se llaman nombre, lo que elimina el constructor 
predeterminado.
Luego se proporcionan tres métodos regulares. El primero se llama setInstrument, 
y toma un parámetro, una instancia de Instrument llamada instrument, y 
no tiene tipo de retorno. El segundo se llama getInstrument y no tiene 
parámetros, pero su tipo de retorno es Instrument. El método final se 
llama play. El método de reproducción en realidad lo aplica la interfaz 
MusicPlayer que implementa la clase Guitarrista. El método play no toma 
parámetros y su tipo de retorno es nulo.
````
* Es ambigua y confusa
* Es lenta de interpretar
* Difícil de procesar

---
![UML: Guitarrista](images/unidad5/ejemplo_guitarrista.jpg)

<!-- .slide: style="font-size: 0.60em" -->
* No es ambigua ni confusa (una vez conocemos la semántica de cada elemento de modelado)
* Es fácil y rápida de interpretar
* Es fácil de procesar por herramientas

---
### UML
* Siglas de "Unified Modeling Language".
* Lenguaje de modelado estándar para modelado orientado a objetos.
* Tiene numerosos tipos de diagramas, pero en la gran mayoría de sistemas se usan solo 5.

![Logo UML](images/unidad5/logo-UML.png)

----

### ¿Por qué UML?
* Es **sencillo**
* Es capaz de modelar todo tipo de sistemas.
* Es un lenguaje universal
* Es fácilmente extensible.
* Es visual y, por lo tanto, intuitivo.
* Es independiente del desarrollo, del lenguaje y de la plataforma.
* Bien ejecutado aporta un conjunto considerable de buenas prácticas.

----

### Consideraciones sobre UML
Los diagramas UML NO son completos. Utilizando los distintos diagramas no podemos estar seguros de comprender con 
totalidad el sistema que va a desarrollarse. Los diagramas, para facilitar la comprensión pueden (y suelen) omitir 
información, pueden tener partes que se entienden de distintas maneras o, incluso, pueden tener conceptos que no 
pueden ser representados por ningún diagrama.

---

![Clasificación de los diagramas UML](images/unidad5/clasificacion-diagramas.png)

----

### Tipos de diagramas UML

<!-- .slide: style="font-size: 0.90em" -->
* **Diagramas de actividades:** Muestran las actividades involucradas en un proceso o en el procesamiento de datos.
* **Diagramas de casos de uso:** Muestran las interacciones entre un sistema y su entorno.
* **Diagramas de secuencia:** Muestran las interacciones entre los actores y el sistema y entre los componentes del sistema.
* **Diagramas de clases:** Muestran las clases de objetos en el sistema y las asociaciones entre estas clases.
* **Diagramas de estado:** Muestran cómo el sistema reacciona a los acontecimientos internos y externos.

---
### El uso de modelos gráficos
* Como una forma de facilitar el debate sobre un sistema
* Como una manera de documentar un modelo de sistema debe ser una representación exacta del sistema, pero no
tiene que ser completa.
* Como una descripción detallada del sistema en ese caso debe ser correcta y completa.

---
### Los modelos de contexto
* Se utilizan modelos de contexto para ilustrar el contexto operativo de un sistema, muestran lo que se
encuentra fuera de los límites del sistema.
* Las cuestiones organizacionales pueden influir en la decisión sobre dónde situar los límites del sistema.
* Los modelos de contexto muestran el sistema y su relación con otros sistemas.

----

### Límites del sistema
* Los límites del sistema se establecen para definir lo que está dentro y lo que está fuera del sistema, muestran otros
sistemas que se utilizan o dependen del sistema que está siendo desarrollado.
* La posición de los límites del sistema tiene un efecto profundo en los requisitos del sistema.
* La definición del límite del sistema es fundamental Si los límites del sistema aumentan y/o disminuyen cambia la
carga de trabajo de las diferentes partes de una organización.

----

#### El contexto del MHC-PMS
![Ejemplo de Diagrama de Contexto](images/unidad5/diagrama_contexto_mhc-pms.jpg)

---

### Perspectiva del proceso
* Los modelos de contexto, simplemente muestran los otros sistemas en ambiente, no cómo se utiliza el sistema
que está siendo desarrollado en ese entorno.
* Los modelos de proceso revelan cómo se utiliza el sistema en desarrollo en los procesos de negocio
* Diagramas de actividades de UML se pueden utilizar para definir los modelos de procesos de negocio.

----

### Diagrama de Actividad
![Modelo de proceso de la detención involuntaria](images/unidad5/modelo_proceso_detencion.jpg)

---
### Modelos de interacción
<!-- .slide: style="font-size: 0.90em" -->
* El modelado de la interacción de usuario es importante ya que ayuda a identificar las necesidades de los usuarios.
* El modelado de interaccion de sistema a sistema resalta los problemas de comunicación que puedan surgir.
* El modelo de interacción de componentes ayuda a comprender si la estructura del sistema propuesto es
adecuada para ofrecer el rendimiento y la fiabilidad del sistema necesario.
* Los **diagramas de casos** y **diagramas de secuencia** se pueden utilizar para el modelado de la interacción.

---
### Modelado de casos de uso
* Los casos de uso se desarrollaron originalmente para apoyar la obtención de requisitos y están incorporados en el UML.
* Cada caso de uso representa una tarea discreta que implica la interacción externa con un sistema.
* Los actores de un caso de uso pueden ser personas u otros sistemas.
* Representación esquemática para proporcionar una visión general de los casos de uso.
* Representación textual para proporcionar una visión detallada.

----

### Uso de datos de transferencia de caso
Un caso de uso en el MHC-PMS:
![Un caso de uso en el MHC-PMS](images/unidad5/ejemplo_1_caso_de_uso.jpg)

----

### Los casos de uso en el MHC-PMS que implica el papel 'Médico Recepcionista'
![Casos de uso Médico Recepcionista](images/unidad5/ejemplo_caso_de_uso.jpg)

---
### Los diagramas de secuencia
<!-- .slide: style="font-size: 0.90em" -->
* Los diagramas de secuencia son parte de UML y se utilizan para modelar las interacciones entre los actores y
los objetos dentro de un sistema.
* Un diagrama de secuencia muestra la secuencia de interacciones que tienen lugar durante un caso de uso en particular.
* Los objetos y los actores involucrados están listados en la parte superior del diagrama, con una línea de puntos
trazada verticalmente a partir de estos.
* Las interacciones entre los objetos se indican mediante flechas anotadas.

----

### Diagrama de secuencia para Ver la información del paciente
![Diagrama de secuencia: Ver información del paciente](images/unidad5/diagrama_secuencia.jpg)

----

#### Diagrama de secuencia para la transferencia de datos
![Diagrama de secuencia: Transferencia de datos](images/unidad5/diagrama_secuencia_transferencia_datos.jpg)

---
### Los modelos estructurales
* Los modelos estructurales muestran la organización de un sistema en función de los componentes que conforman
este sistema y sus relaciones.
* Los modelos estructurales son modelos estáticos, que muestran la estructura del sistema.

---
### Los diagramas de clases
* Los diagramas de clases se utilizan en el desarrollo de un modelo de sistema orientado a objetos para mostrar las
clases de un sistema y las asociaciones entre estas clases.
* Una clase de objeto es una definición general de un tipo de objeto del sistema.
* Una asociación es una relación entre clases.
* Los objetos representan algo en el mundo real, tal como un paciente, una prescripción, médico, etc.

----

### Clases UML y asociación
![Clases UML y asociación](images/unidad5/UML_y_asociacion.jpg)

----

### Las clases y asociaciones en el MHC-PMS
![Clases y asociaciones en el MHC-PMS](images/unidad5/clases_asociaciones_MHC-PMS.jpg)

----

### La clase de consulta
![La clase de consulta](images/unidad5/clase_de_consulta.jpg)

---
### Generalización
* La generalización es una técnica que utilizamos para gestionar la complejidad.
* En lugar de definir las características detalladas de cada entidad, ponemos estas características en las clases
más generales (animales, coches, casas, etc).
* Esto nos permite inferir que los diferentes miembros de estas clases tienen algunas características comunes. 

----

### Generalización
<!-- .slide: style="font-size: 0.90em" -->
* En los sistemas de modelado, a menudo es útil examinar las clases de un sistema para ver si hay posibilidades de
generalización.
* En lenguajes orientados a objetos, la generalización se realiza utilizando los mecanismos de herencia.
* En una generalización, los atributos y las operaciones asociadas a las clases de nivel superior también están
asociadas a las clases de menor nivel.
* Las clases de nivel inferior son subclases que heredan los atributos y operaciones de sus superclases. Estas
clases de nivel inferior son más especificas y pueden añadir atributos y operaciones.

----

### Una jerarquía de generalización
![Una jerarquía de generalización](images/unidad5/jerarquia_de_generalizacion.jpg)

----

### Una jerarquía de generalización con caracteristicas agregadas
![Generalización con caracteristicas agregadas](images/unidad5/jeneralizacion_caracteristicas_agregadas.jpg)

---
### Agregación
* Un modelo de agregación muestra cómo las clases se componen de otras clases.
* Los modelos de agregación son similares a la parte de la relación en los modelos de datos semánticos.

----

### Agregación
![Agregacion](images/unidad5/agregacion.jpg)

---

### Modelos de comportamiento
* Modelos de comportamiento son los modelos del comportamiento dinámico de un sistema, cuando se está ejecutando.
* Muestran lo que ocurre cuando un sistema responde a un estímulo de su entorno.
* Los estímulos pueden ser de dos tipos: **Datos** o **Eventos**

----

### El modelado impulsado por datos
* Muchos sistemas empresariales son sistemas de procesamiento de datos. Son controlados por la entrada de
datos al sistema, con relativamente poco procesamiento de eventos externos.
* Estos modelos muestran la secuencia de las acciones involucradas en el procesamiento de datos de entrada y la
salida asociada.
* Son particularmente útiles durante el análisis de los requisitos, ya que pueden ser utilizados para mostrar el
procesamiento de extremo a extremo en un sistema.

----

### Un modelo de actividad de la operación de la bomba de insulina

![Modelo de actividad de Bomba de insulina](images/unidad5/modelo_actividad_bomba_insulina.jpg)

---- 

### El procesamiento de pedidos

![Procesamiento de pedidos](images/unidad5/procesamiento_de_pedidos.jpg)

---- 

### Modelado impulsado por eventos

* Sistemas de tiempo real son a menudo gestionados por eventos, con un procesamiento de datos mínimo.
* Modelado por eventos muestra cómo un sistema responde a acontecimientos externos e internos.
* Se basa en la suposición de que un sistema tiene un número finito de estados y que los acontecimientos
(estímulos) puede causar una transición de un estado a otro.

---
### Modelos de máquina de Estado
* Estos modelan el comportamiento del sistema en respuesta a eventos externos e internos.
* Muestran las respuestas del sistema a los estímulos tan a menudo se utilizan para el modelado de sistemas de tiempo real.
* Modelos de máquinas de estado muestran los estados del sistema como nodos y eventos como arcos entre estos
nodos. Cuando ocurre un evento, el sistema pasa de un estado a otro.

----

### Diagrama de estado de un horno de microondas
![Diagrama de estado: Microondas](images/unidad5/diagrama_estado_microondas.jpg)

----

### Los Estados y los estímulos para el horno de microondas
<!-- .slide: style="font-size: 0.50em" -->
<!--
| Estado            | Descripción                                                                                                                                                                                                                                                                    |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esperando         | El horno está a la espera para la entrada. La pantalla muestra la hora actual.                                                                                                                                                                                                 |
| Potencia Media    | La potencia del horno es de 300 vatios. La pantalla muestra 'Potencia Media'.                                                                                                                                                                                                  |
| Potencia Completa | La fuente de horno se establece en 600 vatios. La pantalla muestra 'Potencia Máxima'.                                                                                                                                                                                          |
| Establecer tiempo | El tiempo de cocción se ajusta al valor de entrada del usuario. La pantalla muestra el tiempo de cocción seleccionado y se actualiza a medida que el tiempo se ajusta.                                                                                                         |
| Deshabilitar      | El funcionamiento del horno está deshabilitado por seguridad. Luz interior del horno está encendido. La pantalla muestra "No está listo'.                                                                                                                                      |              
| Habilitado        | Se habilita el funcionamiento del horno. Luz interior del horno está apagado. La pantalla muestra "Listo para cocinar'.                                                                                                                                                        |   
| Operacion         | Horno en funcionamiento. Luz interior del horno está encendido. La pantalla muestra la cuenta atrás del temporizador. Al término de la cocción, el zumbador suena durante cinco segundos. La luz del horno está encendido. La pantalla muestra 'Cocinando completa ", mientras |                                                                                                                                                                                                                                                       
-->
<table>
<thead>
<tr>
<th style="text-align:left">Estado</th>
<th style="text-align:left">Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Esperando</td>
<td style="text-align:left">El horno está a la espera para la entrada. La pantalla muestra la hora actual.</td>
</tr>
<tr>
<td style="text-align:left">Potencia Media</td>
<td style="text-align:left">La potencia del horno es de 300 vatios. La pantalla muestra &#39;Potencia Media&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Potencia Completa</td>
<td style="text-align:left">La fuente de horno se establece en 600 vatios. La pantalla muestra &#39;Potencia Máxima&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Establecer tiempo</td>
<td style="text-align:left">El tiempo de cocción se ajusta al valor de entrada del usuario. La pantalla muestra el tiempo de cocción seleccionado y se actualiza a medida que el tiempo se ajusta.</td>
</tr>
<tr>
<td style="text-align:left">Deshabilitar</td>
<td style="text-align:left">El funcionamiento del horno está deshabilitado por seguridad. Luz interior del horno está encendido. La pantalla muestra &quot;No está listo&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Habilitado</td>
<td style="text-align:left">Se habilita el funcionamiento del horno. Luz interior del horno está apagado. La pantalla muestra &quot;Listo para cocinar&#39;.</td>
</tr>
<tr>
<td style="text-align:left">Operacion</td>
<td style="text-align:left">Horno en funcionamiento. Luz interior del horno está encendido. La pantalla muestra la cuenta atrás del temporizador. Al término de la cocción, el zumbador suena durante cinco segundos. La luz del horno está encendido. La pantalla muestra &#39;Cocinando completa &quot;, mientras</td>
</tr>
</tbody>
</table>

----

### Los Estados y los estímulos para el horno de microondas
<!-- .slide: style="font-size: 0.60em" -->
<!--
| Estimulo | Descripción                                                   |
|:---------|:--------------------------------------------------------------|
| Potencia Media | El usuario ha pulsado el botón de media potencia.       |
| Potencia Máxima | El usuario ha pulsado el botón de alta potencia.       |
| Temporizador | El usuario ha pulsado el botón del temporizador.          |
| Nú mero | El usuario ha pulsado una tecla numérica.                     |
| Puerta Abierta | El interruptor de la puerta del horno no está cerrada.  |
| Puerta Cerrada | El interruptor de la puerta del horno está cerrada.     |
| Iniciar | El usuario ha pulsado el botón de Inicio.                     |
| Cancelar | El usuario oprime el botón Cancelar                           |
-->
<table>
<thead>
<tr>
<th style="text-align:left">Estimulo</th>
<th style="text-align:left">Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Potencia Media</td>
<td style="text-align:left">El usuario ha pulsado el botón de media potencia.</td>
</tr>
<tr>
<td style="text-align:left">Potencia Máxima</td>
<td style="text-align:left">El usuario ha pulsado el botón de alta potencia.</td>
</tr>
<tr>
<td style="text-align:left">Temporizador</td>
<td style="text-align:left">El usuario ha pulsado el botón del temporizador.</td>
</tr>
<tr>
<td style="text-align:left">Número</td>
<td style="text-align:left">El usuario ha pulsado una tecla numérica.</td>
</tr>
<tr>
<td style="text-align:left">Puerta Abierta</td>
<td style="text-align:left">El interruptor de la puerta del horno no está cerrada.</td>
</tr>
<tr>
<td style="text-align:left">Puerta Cerrada</td>
<td style="text-align:left">El interruptor de la puerta del horno está cerrada.</td>
</tr>
<tr>
<td style="text-align:left">Iniciar</td>
<td style="text-align:left">El usuario ha pulsado el botón de Inicio.</td>
</tr>
<tr>
<td style="text-align:left">Cancelar</td>
<td style="text-align:left">El usuario oprime el botón Cancelar</td>
</tr>
</tbody>
</table>

----

### El funcionamiento del horno de microondas
![Funcionamiento Microondas](images/unidad5/funcionamiento_microondas.jpg)

---
### Ingeniería dirigida por modelos
<!-- .slide: style="font-size: 0.90em" -->
* Ingeniería dirigida por modelos (MDE) es un enfoque para el desarrollo de software donde los modelos en lugar
de los programas son los principales resultados del proceso de desarrollo.
* Los programas que se ejecutan en una plataforma de hardware / software se generan automáticamente a partir
de los modelos.
* Los defensores de la MDE sostienen que esto eleva el nivel de abstracción en la ingeniería de software para que
los ingenieros ya no tienen que preocuparse por los detalles del lenguaje de programación o las características
específicas de plataformas de ejecución.

----

### Ingeniería dirigida por modelos
- **Modelo Independiente de Computación (CIM):** Modela las importantes abstracciones de dominio usadas en el sistema.
- **Modelo Independiente de Plataforma (PIM):** Modela la operación del sistema sin referencia a su implementación.
- **Modelos específicos de plataforma (PSM)**

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
