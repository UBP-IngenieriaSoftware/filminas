---
title: Diseño Arquitectónico
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Diseño Arquitectónico

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

### Diseño Arquitectónico
* Arquitectura de Software
* Ventajas de la Arq. Explícita
* La Arq. y características del sistema
* Estructura del sistema
* Box y diagramas
* Decisiones de Diseño Arq.
* Reutilización de la Arq.
</div>
<div class="grid-item">

* Estilos Arquitectónicos
* Modelos Arquitectónicos
* Modelo Vista-Controlador
* Modelo Repositorio
* Modelo Cliente-Servidor
* Modelo de Capas
* Modelo de Tubería y Filtro
</div>
</div>

---

### Diseño Arquitectónico
Se refiere a la estructura y organización a gran escala de un sistema de software. Es la planificación de los componentes principales de un sistema y la forma en que interactúan entre ellos. El diseño arquitectónico se enfoca en la visión global del sistema, definiendo módulos, componentes, subsistemas, bases de datos, servidores y cómo todo se conecta y comunica.

----

### Diseño Arquitectónico: Ejemplo
- **Ejemplo:** Decidir si usar una arquitectura monolítica o una basada en microservicios.
- **Objetivo:** Crear una estructura robusta, escalable y eficiente que sirva de base para todo el sistema.

----

**Diseño Arquitectónico** y **Patrones de Diseño** NO son lo mismo.

----

### Patrones de Diseño
Son soluciones probadas y reutilizables para problemas comunes en el desarrollo de software a un nivel más detallado. Estos patrones se aplican a problemas específicos dentro del código o en la interacción de ciertos componentes, y son como "buenas prácticas" que se pueden seguir.

- **Ejemplo:** Patrones como Singleton, Factory, o Observer.
- **Objetivo:** Resolver problemas frecuentes de diseño en el nivel del código y mejorar la mantenibilidad y flexibilidad del software.


----

#### Diseño Arquitectónico vs. Patrones de Diseño
- **Escala:** El diseño arquitectónico trabaja a una escala más alta y global (visión del sistema completo), mientras que los patrones de diseño se centran en problemas más específicos y detallados dentro del código.
- **Finalidad:** El diseño arquitectónico es más estratégico y se refiere a la estructura general del sistema, mientras que los patrones de diseño son tácticos y se aplican a situaciones puntuales para mejorar la calidad del código.

---
### ARQUITECTURA DE SOFTWARE
* El diseño arquitectónico es un proceso de diseño que permite la identificación de los
sub-sistemas que componen un sistema y su comunicación
* El resultado de este proceso de diseño es una descripción de la arquitectura de software.

---
### DISEÑO ARQUITECTÓNICO
* Una fase temprana del proceso de diseño del sistema.
* Representa el vínculo entre los procesos de especificación y diseño.
* Suelen llevarse a cabo en paralelo con las actividades de algunas especificaciones.
* Se trata de identificar los principales componentes del sistema y sus comunicaciones.

---

##### Modelo Abstracto de arquitectura de un SISTEMA DE CONTROL DE ROBOT DE EMBALAJE

![Robot de Embalaje](images/unidad6/robot-de-embalaje.png)

----

Las arquitetcuras de sistemas se moden con frecuenca usando diagramas de bloques simples:
- **Recuadros:** Componentes o sub-componentes
- **Flechas:** Datos o sañales de control.

----

### BOX Y DIAGRAMAS
* Muy abstracto - que no muestran la naturaleza de los componentes ni las relaciones de las
  propiedades visibles externamente de los sub-sistemas.
* Sin embargo, útil para la comunicación con las partes interesadas y para la planificación de proyectos.

---
### VENTAJAS DE LA ARQUITECTURA EXPLÍCITA
* **Comunicación entre los stakeholders**: La arquitectura puede ser utilizada como un foco de discusión del sistema 
por los stakeholders.
* **Análisis del sistema**: Analizar si el sistema puede
hacer frente a sus requerimientos no funcionales, como rendimiento, fiabilidad y mantenibilidad.
* **Reutilización a gran escala**: La arquitectura puede ser reutilizable a través
  de una variedad de sistemas que poseen requerimientos similares.
* **Forma de documentación**: Se pueden visualizar componentes, interfaces y conexiones.

---
### DECISIONES DE DISEÑO ARQUITECTÓNICO
* Diseño arquitectónico es un proceso creativo, por lo que el proceso es diferente dependiendo del
  tipo de sistema que se está desarrollado, antecedentes y experiencia del arquitetco.
* Es común una serie de decisiones, en todos los procesos de diseño.

----

### DECISIONES DE DISEÑO ARQUITECTÓNICO
1. ¿Existe una arquitectura de aplicaciones genéricas que se pueden utilizar?
2. ¿Cómo se distribuirá el sistema a través de núcleos y procesadores?
3. ¿Qué estilos arquitectónicos son apropiados?
4. ¿Qué enfoque se utilizará para la estructura del sistema?
5. ¿Cómo el sistema se descompone en módulos?
6. ¿Qué estrategia de control se debe utilizar para los componentes?
7. ¿Cuál arquitetcura es mejor en base a los requerimientos no funcionales?
8. ¿Cómo el diseño arquitectónico se evaluará?
9. ¿Cómo debe ser documentada la arquitectura?


---

### ARQUITECTURA y requerimientos NO funcionales
1. **Rendimiento:** Reducir al mínimo las operaciones de comunicaciones. Uso de grano grueso en lugar de
componentes de grano fino.
2. **Seguridad:** Una arquitectura con los procesos críticos en las **capas** interiores.
3. **Protección:** La protección se debe ubicar en pocos componentes individuales, para reducir validaciones.
4. **Disponibilidad:** Incluir componentes redundantes y los mecanismos de tolerancia a fallos.
5. **Mantenibilidad:** Uso de grano fino, los componentes reemplazables.

----

Algunos requerimientos se "contradicen" entre si, como el **rendimiento** que requiere componentes de grano grueso y
la **mantenibilidad** que requiere componentes de grano fino. Por eso debe encontrarse una **solución de compromiso**.

----

Es imposible representar toda la información relevante sobre la arquitectura de un sistema en un solo modelo arquitectónico,
ya que cada uno presenta una perspectiva del sistema.

---
### Vistas Arquitectónicas
1. **Vista Lógica:** Abstracciones como objectos o clases de objectos.
2. **Vista de Proceso:** Muestra como en tiempo de operación los componentes interactuan. (rendimiento y disponibilidad)
3. **Vista de Desarrollo:** Muestra como el software está descompuesto
4. **Vista Física:** Expone el hardware del sistema y como los componentes de software se distribuyen en los procesadores.
5. **Vista Abstracta:** Descomponer los requerimientos de alto nivel en especificaciones detalladas.

---
### ESTRUCTURA DEL SISTEMA
* Concerniente a la descomposición del sistema en sub-sistemas.
* El diseño arquitectónico se expresa normalmente como un diagrama de bloques que presentan un
panorama general de la estructura del sistema.
* Modelos más específicos muestran cómo los sub-sistemas comparten los datos, se distribuyen y la
interfaz con los demás también pueden ser desarrollados.

---
### REUTILIZACIÓN DE LA ARQUITECTURA
* Sistemas en el mismo dominio a menudo tienen arquitecturas similares que reflejan conceptos del dominio.
* La aplicación de líneas de producción se construye en torno a un núcleo con arquitectura
particular, con variantes que satisfagan las necesidades del cliente.

---
### ESTILOS ARQUITECTÓNICOS
* El modelo arquitectónico de un sistema puede ajustarse a un modelo genérico o estilo arquitectónico.
* La conciencia de estos estilos puede simplificar el problema de la definición de arquitecturas de sistemas.
* Sin embargo, la mayoría de los grandes sistemas son heterogéneos y no siguen un mismo estilo arquitectónico.

---
### MODELOS ARQUITECTÓNICOS
<!-- .slide: style="font-size: 0.90em" -->
* Utilizarse para documentar un diseño arquitectónico.
* Modelo estructural estático, que muestra los principales componentes del sistema.
* Modelo de proceso dinámico que muestra el modelo de proceso de la estructura del sistema.
* Modelo de interfaz que define las interfaces de sub-sistemas.
* Modelo de relaciones, como un modelo de flujo de datos que muestra las relaciones de sub-sistemas.
* Modelo de distribución que muestra cómo los sub-sistemas se distribuyen a través de computadoras.

---

### MODELOS
- Modelo Vista-Controlador
- Modelo de Capas
- Modelo Repositorio
- Modelo Cliente-Servidor
- Modelo de Tubería y Filtro

---
### MODELO VISTA-CONTROLADOR
- Separa **presentación** e **interacción** de los **datos** del sistema. 
- El sistema se estructura en **3** componentes lógicos. 
- El componente **Modelo** maneja los _datos_ del sistema y las operaciones asociadas a esos datos. 
- El componente **Vista** define y gestiona cómo se _presentan_ los datos al usuario. 
- El componente **Controlador** dirige la _interacción_ del usuario y pasa estas interacciones a Vista y Modelo.

----

### MODELO VISTA-CONTROLADOR

![Modelo Vista-Controlador](images/unidad6/modelo-vista-controlador.jpg)

----

### APLICACION WEB CON ARQUITECTURA MVC

![Arquitetcura MVC](images/unidad6/arquitetura-mvc.jpg)

----

### MODELO VISTA-CONTROLADOR: USO
- Cuando existen múltiples formas de ver e interactuar con los datos
- Al desconocerse los requerimientos futuros para la interacción y presentación.

----

### MODELO VISTA-CONTROLADOR: Ventajas & Desventajas
Ventajas:
- Permite que los datos cambien de manera independiente de su representación y viceversa. 
- Soporta en diferentes formas la presentación de los mismos datos.

Desventaja:
- Puede implicar código adicional y complejidad de código cuando el modelo de datos y las
  interacciones son simples.

---
### MODELO DE CAPAS
* Organiza el sistema en capas con funcionalidad relacionada con cada capa. 
* Una capa da servicios a la capa superior, de modo que las capas de nivel inferior representan
  servicios núcleo que es probable se utilicen a lo largo de todo el sistema.

----

### MODELO DE CAPAS: USO
* Al construirse nuevas facilidades encima de los sistemas existentes.
* Cuando el desarrollo se dispersa a través de varios equipos de trabajo, y cada uno es responsable  de una capa de funcionalidad. 
* Cuando exista un requerimiento para seguridad multinivel.

----

### MODELO DE CAPAS: Ventajas
* Permite la sustitución de capas completas en tanto se conserve la interfaz. 
* Aumenta la confiabilidad del sistema, en cada capa pueden incluirse facilidades redundantes
* 
----

### MODELO DE CAPAS: Desventajas
* Suele ser difícil ofrecer una separación limpia entre capas, lo que afecta el rendimiento.

----

### SISTEMA DE GESTIÓN

![Sistema de Gestión](images/unidad6/sistema-gestion.jpg)

----

### SISTEMA DE BIBLIOTECA

![Sistema de Biblioteca](images/unidad6/sistema-biblioteca.jpg)

---
### EL MODELO REPOSITORIO
* Sub-sistemas de intercambio de datos. Esto puede hacerse de dos maneras:
  * Datos compartidos se lleva a cabo en un repositorio o base de datos central y puede ser visitada por todos
los sub-sistemas;
  * Cada sub-sistema mantiene su propia base de datos y pasa datos explícitamente a otros subsistemas.
* Cuando grandes cantidades de datos sean compartidos, el modelo de repositorio compartido es más comúnmente utilizado.

----

### ARQUITECTURA DE REPOSITORIO IDE

![Repositorio IDE](images/unidad6/repositorio-IDE.jpg)

----

### MODELO REPOSITORIO CARACTERÍSTICAS
**Ventajas**
* Manera eficaz de compartir grandes cantidades de datos;
* Sub-sistemas no tienen por qué preocuparse de cómo los datos se producen, por ejemplo, la gestión centralizada
copia de seguridad, seguridad, etc
* Un modelo a compartir se publica como el esquema del repositorio.

----

### MODELO REPOSITORIO CARACTERÍSTICAS
**Desventajas**
* Sub-sistemas deben ponerse de acuerdo sobre un modelo repositorio de datos. Inevitablemente, un compromiso;
* La evolución de datos es difícil y costosa;
* No hay lugar para las políticas de gestión específicas;
* Difícil de distribuir de manera eficiente.

---
### MODELO CLIENTE-SERVIDOR
* Sistema distribuido que muestra cómo el modelo de datos y procesamiento se distribuye a través
de una gama de componentes.
* Conjunto de servidores independientes que ofrecen servicios específicos, tales como la
impresión, gestión de datos, etc
* Conjunto de clientes que piden a éstos los servicios.
* Red que permite a los clientes acceder a los servidores.

----

### BIBLIOTECA DE IMÁGENES Y PELÍCULAS

![Biblioteca de Imgágenes y películas](images/unidad6/imagenes-peliculas.jpg)

----

### CLIENTE-SERVIDOR CARACTERÍSTICAS
**Ventajas**
* Distribución de datos es sencilla;
* Hace un uso eficaz de los sistemas en red. Puede requerir hardware más barato;
* Fácil añadir nuevos servidores o actualizar los servidores existentes.

----

### CLIENTE-SERVIDOR CARACTERÍSTICAS
**Desventajas**
* No hay un modelo de datos compartidos, así que los sub-sistemas utilizan diferentes datos de la organización. 
Intercambio de datos puede ser ineficaz;
* Redundantes en la gestión de cada servidor;
* No hay registro central de nombres y servicios - que puede ser difícil de averiguar qué servidores y servicios están
disponibles.

---
### MODELO DE TUBERIA Y FILTRO
* Cada componente de procesamiento (filtro) es discreto y realiza un tipo de transformación de datos.
* Los datos fluyen (como en una tubería) de un componente a otro para su procesamiento.
* Se utiliza en aplicaciones de procesamiento de datos (tanto basadas en lotes como en transacciones),

----

### MODELO DE TUBERIA Y FILTRO

![Modelo de Tubería y Filtro](images/unidad6/modelo_tuberia-filtro.jpg)

---
### Estructura de las aplicaciones de procesamiento de transacción

![Estructura de las aplicaciones de procesamiento de transacción](images/unidad6/procesamiento-transaccion.png)

---
### Arquitectura de software de un sistema ATM

![ATM](images/unidad6/ATM.png)

---
### Arquitectura de sistema de información en capas

![Arquitectura de Capas](images/unidad6/capas.png)

---
### Arquitectura del MHC-PMS

![MHC-PMS](images/unidad6/MHC-PMS.png)

---
#### Arquitectura de un sistema de procesamiento de lenguaje

![Lenguaje de Procesamiento del Sistema](images/unidad6/arquitetcura-procesamiento.png)

---
### Arquitectura de compilador de tubería y filtro

![Arquitetcura de Tubería y Filtro](images/unidad6/arquitetcura-tuberia-filtro.png)

---
#### Arquitectura de repositorio para un sistema de procesamiento de lenguaje

![Arquitetcura de Repositorio para un sistema de Procesamiento de Lenguaje](images/unidad6/Arquitetcura-de-repositorio.png)

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)

<!--https://refactoring.guru/design-patterns/what-is-pattern-->