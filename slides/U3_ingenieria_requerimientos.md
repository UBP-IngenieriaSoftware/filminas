---
title: Ingeniería de Requerimientos
theme: solarized
slideNumber: true
---

# Ingeniería de Software
## Ingeniería de Requerimientos
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

### Ingeniería de Requerimientos
* Definición
* Por que?
* Errores de Software
* Costos del software
* Productos de software
* Especificaciones del producto
* Preguntas sobre la ingeniería de Software
</div>

---
### Ingeniería de requerimientos
* El proceso de establecimiento de los servicios que el cliente necesita de un sistema y las limitaciones con las
que opera y se desarrolla.
* Los requisitos, en sí, son las descripciones de los servicios del sistema y las limitaciones que se generan
durante el proceso de ingeniería de requerimientos.

---
### Definicion de Requerimiento (Davis)
"Si una empresa desea realizar un contrato para un proyecto de desarrollo de software grande, debe definir sus necesidades de una
manera suficientemente abstracta para que no se malentienda la solución. Los requisitos deben ser escritos de manera que varios
contratistas puedan hacer una propuesta para el contrato, ofreciendo, tal vez, diferentes formas de satisfacer las necesidades de la
organización del cliente. Una vez que el contrato ha sido adjudicado, el desarrollador debe escribir una definición del sistema para el cliente
detalladamente para que el cliente entienda y pueda validar lo que el software hará. Ambos documentos pueden ser llamados el documento
de requerimientos para el sistema ".

---
### Qué es un requerimiento?
Propiedad o restricción, determinada con precisión, que un producto software debe satisfacer

* Como se expresa un requerimiento?
La definicion de un requerimiento puede variar de una declaración abstracta de un servicio o de una
restricción de sistema a una especificación funcional matemática detallada.

Que Problemas hay?
* Dificultad de comunicación entre el equipo de  desarrollo y el grupo de clientes/usuarios.
* Cambio de los requerimientos.
* Imposibilidad de identificar la totalidad de los requerimientos de un producto

---
### La comunicación...
![La comunicación](images/unidad3/analisis-columpio-en-el-arbol.jpg)

---
### Tipos de requerimientos
* Requerimientos del usuario (Alto nivel)
  * Declaraciones en lenguaje natural que define los servicios que  debe proporcionar el sistema y sus limitaciones. 
Escrito para que los clientes entiendan.
* Requerimientos del sistema (Detallado)
  * Descripciones detalladas de las funciones del sistema, los servicios y las limitaciones operativas. Define todo lo 
que debe ser implementado así que puede ser parte de un documento entre el cliente y el desarrollador.

---
### Requerimientos de usuario y del sistema
Requerimiento del usuario:
1. TEI software debe proveer un medio para representar y acceder a archivos externos creados por otras herramientas.

Especificación de los requerimientos del sistema:
1.1. Al usuario se le proveerá con los recursos para definir el tipo de archivos externos.
1.2. Cada tipo de archivo externo tendrá una herramienta asociada que será aplicada al archivo.
1.3. Cada tipo de archivo externo se representará como un icono específico sobre la pantalla del usuario.
1.4. Se proveerán recursos para que el usuario defina el icono que representa un tipo de archivo externo.
1.5. Cuando un usuario selecciona un icono que representa un archivo externo, el efecto de esa selección es aplicar la
herramienta asociada con este tipo de archivo al archivo representado por el icono seleccionado.

---
### Requerimientos funcionales y no funcionales
* Requerimientos funcionales
  * Enunciados acerca de los servicios del sistema que debe proporcionar, como el sistema debe reaccionar a entradas
generales y cómo el sistema debe comportarse en situaciones
particulares.
  * Pueden explicar lo que el sistema no debe hacer.
* Requerimientos no funcionales
  * Limitaciones en los servicios o funciones que ofrece el sistema, como restricciones de tiempo, restricciones del proceso de
desarrollo, normas, etc.
  * A menudo se aplica al sistema en su conjunto, en lugar de a las funciones o servicios individuales.
* Requerimientos de dominio 
  * Las restricciones en el sistema segun el dominio de operación

---
### Requerimientos funcionales
* Describe los servicios de funcionalidad o servicios del  sistema.
* Dependerá del tipo de software, los usuarios esperados y el tipo de entorno en el que se utiliza el software.
* Requerimientos funcionales de los usuarios son  declaraciones de alto nivel de lo que el sistema debe hacer
* Requerimientos funcionales de sistema deben describir los servicios del sistema en detalle.

---
### Requerimientos funcionales para el MHC-PMS
* Un usuario debe ser capaz de buscar las listas de citas de todas las clínicas.
* El sistema deberá generar cada día, por cada clínica, una lista de pacientes que se espera que asistan a las
citas de ese día.
* Cada miembro del personal que utiliza el sistema deberá ser identificado únicamente por su número de empleado 8
dígitos.

---
### Imprecisión de requerimientos
* Los problemas surgen cuando los requerimientos no se expresan con precisión.
* Requisitos ambiguos pueden ser interpretados de diferentes maneras por los desarrolladores y usuarios.
* Considere el término ‘buscar' en un requerimiento
  * Intención del usuario - búsqueda de un nombre de paciente a través de todas las citas en todas las clínicas
  * Interpretación Desarrollador - buscar un nombre de paciente en una clínica individual. El usuario elige la clínica 
luego se realiza la búsqueda.

---
### La integridad y la coherencia de Requerimientos
En principio, los requerimientos deben ser a la vez completos y coherentes.
* **Completo:** Deben incluir una descripción de todos los servicios requeridos.
* **Coherente:** No debe haber conflictos o contradicciones en las descripciones de los servicios del sistema.

En la práctica, es dificil producir un documento de requisitos completo y consistente.

---
### Requerimientos no funcionales
Definen
* Propiedades transversales a todo el sistema :
  * Los requerimientos de fiabilidad 
  * Tiempo de respuesta. 
  * Necesidad almacenamiento.
* Limitaciones:
  * Uso de un IDE en particular 
  * Lenguaje de programación. 
  * Método de desarrollo.
  
Requisitos no funcionales pueden ser más críticos que los requerimientos funcionales. Si éstos no se cumplen, el sistema puede ser inútil.

---
### Requerimientos no funcionales
* Requisitos no funcionales pueden afectar a la arquitectura general de un sistema en lugar de a los componentes individuales.
    * Por ejemplo, para garantizar que se cumplen los requerimientos de rendimiento, puede que tenga que organizar el sistema para
      minimizar las comunicaciones entre componentes.
* Un requisito no funcional , como un requisito de seguridad, puede generar una serie de requerimientos
  funcionales relacionados que definen los servicios del sistema que se requieren.
    * También puede generar requerimientos que restringen los requerimientos existentes.
  
---
### Clasificación de requerimientos no funcionales
* **Requerimientos del producto**, que especifican como el producto debe comportarse, por ejemplo velocidad de
ejecución, fiabilidad, etc.
* **Requerimientos organizacionales**, que son consecuencia de las políticas y procedimientos de la organización, por 
ejemplo, estándares de procesos utilizados, los requisitos de implementación, etc.
* **Requerimientos externos**, que surgen de factores que son externos al sistema y su proceso de desarrollo, por 
ejemplo, requisitos de interoperabilidad, los requisitos legislativos, etc.

---
### Tipos de requerimientos no funcionales
![Requerimientos no funcionales](images/unidad3/requerimientos-no-funcionales.png)

---
### Ejemplo de requerimientos no funcionales de MHC-PMS
* **Requerimientos del producto**
El MHC-PMS estará a disposición de todas las clínicas durante las horas normales de trabajo (lun-vie, 08:30 a 17:30). 
El tiempo de inactividad dentro de las horas normales de trabajo no excederá de cinco segundos en cualquiera de un día.
* **Requerimiento organizacional**
Los usuarios del sistema MHC-PMS deberán autenticarse usando su tarjeta de identidad autoridad sanitaria.
* **Requisito externo**
El sistema deberá aplicar las disposiciones de privacidad del paciente según lo establecido en HStan-03-2006-priv.

---
### Ejemplo de requerimientos no funcionales sistema de bibliotecas LIBSYS
* Requerimiento del producto
  * La interfaz del usuario para LIBSYS deberá ser implementada como HTML simple sin marcos o applets.
* Requerimiento organizativo
  * El proceso de desarrollo del sistema y los documentos a entregar debe ajustarse al proceso y a los productos a entregar definifos en el STAN-95
* Requerimiento externo
  * El sistema no deberá revelar a sus operadores alguna información personal de los clientes excepto su nombre y número de referencia.

---
### Objetivos y requerimientos
Requerimientos no funcionales pueden ser muy difíciles de explicar y requerimientos imprecisos pueden ser muy difíciles de verificar

* Objetivos 
  * Una declaración general de lo que el cliente quiere, como la facilidad del uso.
* Requerimiento no funcional verificable 
  * Una declaración mediante una cierta medida que se puede probar de forma objetiva.
    
Los objetivos son útiles para los desarrolladores, ya que transmiten las intenciones de los usuarios del sistema.

---
### Requerimientos de usabilidad
* El sistema debe ser fácil de usar por el personal médico y debe ser organizado de tal manera que los
errores de los usuarios se reducen al mínimo. (Objetivo)
* El personal médico debe ser capaz de utilizar todas las funciones del sistema después de cuatro horas de
entrenamiento. Después de este entrenamiento, el número medio de errores cometidos por los usuarios
experimentados no excederá de dos por cada hora de uso del sistema. (Requerimiento no funcional verificable)

---
### Métricas para la especificación de requisitos no funcionales
| Propiedad | Medida                                                                                                                           |
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| Velocidad | Transacciones procesadas por segundo <br> Tiempo de respuesta al usuario y a eventos <br> Tiempo de actualización de la pantalla | 
| Tamaño | M Bytes <br> Número de chips de ROM |
| Facilidad de uso | Tiempo de formación <br> Número de marcos de ayuda |
| Confiabilidad | Tiempo medio entre fallos <br> Probabilidad de no disponibilidad <br> Tasa de ocurrencia de dallos <br> Disponibilidad |
| Robustez | Tiempo de reinicio después de fallo <br> Porcentaje de eventos que causan fallos <br> Probabilidad de corrupción de datos después de un fallo |
| Portabilidad | Porcentaje de declaraciones dependientes de objetivo |

---
### Requerimientos del dominio
* Dominio operacional del sistema impone requerimientos.
  * Por ejemplo, un sistema de control de trenes tiene que tener en cuenta las características de frenado en diferentes
condiciones climáticas.
* Requerimientos de dominio generan nuevos requisitos funcionales, limitaciones sobre los requisitos existentes o definir
cálculos específicos.
* Si los requerimientos de dominio no están satisfechos, el sistema puede ser inutilizable.

---
### Problemas de los requerimientos de dominio
* Comprensibilidad
  * Los requerimientos se expresan en el lenguaje del dominio de aplicación
  * A menudo, esto no es entendido por los ingenieros de software de desarrollo del sistema.
* Implícito 
  * Especialistas del dominio entienden la zona tan bien, que no piensan en hacer de las exigencias de dominio explícito.

---
### Documento de requerimientos de software
* El documento de requisitos de software es la declaración oficial de lo que se requiere de los
desarrolladores del sistema.
* Debe incluir tanto una definición de los requisitos del usuario y una especificación de los requisitos del sistema.
* NO es un documento de diseño.

Debe establecer de lo QUE el sistema DEBE hacer y NO COMO es que debe hacerlo.

---
### Métodos agiles y requerimientos
* Muchos métodos ágiles argumentan que la producción de un documento de requisitos es una pérdida de tiempo que
los requisitos cambian tan rápidamente.
* El documento es, por tanto, siempre actualizado.
* Métodos como XP utilizan requisitos expresados como "historias de usuario”
* Esto es práctico para ciertos sistemas, pero problemático para los sistemas que requieren una gran cantidad de
análisis previo a la entrega (por ejemplo, sistemas críticos) o sistemas desarrollados por varios equipos.

---
### Los usuarios de un documento de requerimientos
![Documento de requerimientos](images/unidad3/roles.jpg)

---
### Documento de Requerimientos
* La información contenida en el documento de requerimientos depende del tipo de sistema y el enfoque
de desarrollo utilizado.
* Los sistemas desarrollados por incrementos, por lo general, tienen menos detalle en el documento de requerimientos.
* Las Normas para documentos de requerimientos estan especificadas por el estándar IEEE. En su mayoría son
aplicables a los requisitos para los grandes proyectos de ingeniería de sistemas.

---
### La estructura de un documento de requerimientos
| Capitulo | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prefacio | Esto debe definir el número de lectores se espera del documento y describir su historial de versiones, incluyendo una justificación para la creación de una nueva versión y un resumen de los cambios realizados en cada versión.                                                                                                                               |
| Introducción | Esto debería describir la necesidad de que el sistema. Debe describir brevemente las funciones del sistema y explicar cómo va a funcionar con otros sistemas. También debe describir cómo el sistema se ajusta a los objetivos generales de la empresa o estratégicos de la organización puesta en marcha del software.                                         |
| Glosario | Esto debería definir los términos técnicos utilizados en el documento. No debería hacer suposiciones acerca de la experiencia o los conocimientos del lector.                                                                                                                                                                                                   | 
| Definición de requerimientos de usuario | Aquí, usted describe los servicios proporcionados por el usuario. Los requisitos del sistema no funcionales también deben ser descritos en esta sección. Esta descripción puede usar el lenguaje natural, diagramas u otras anotaciones que sean comprensibles para los clientes. Las normas de productos y de procesos que deben seguirse deben especificarse. |
| Arquitectura del sistema | Este capítulo debe presentar una descripción de alto nivel de la arquitectura del sistema previsto, que muestra la distribución de funciones a través de los módulos del sistema. Los componentes arquitectónicos que se reutilizan deben destacarse.                                                                                                           |

---
### La estructura de un documento de requerimientos
| Capitulo | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Especificación de requerimientos del sistema | Esto debería describir los requisitos funcionales y no funcionales en más detalle. Si es necesario, mayor detalle puede añadirse a los requerimientos no funcionales. Interfaces para otros sistemas pueden ser definidos.                                                                                                                                                                                                            |
| Modelos del sistema | Esto podría incluir modelos gráficos del sistema que muestran las relaciones entre los componentes del sistema y el sistema y su entorno. Ejemplos de posibles modelos son modelos de objetos, modelos de flujo de datos, o los modelos de datos semánticos.                                                                                                                                                                          |
| Sistema de evaluación | Este debe describir los supuestos fundamentales en que se basa el sistema, y cualquier cambio previsto debido a la evolución del hardware, cambios en las necesidades de los usuarios, y así sucesivamente. Esta sección es útil para los diseñadores de sistemas, ya que puede ayudar a evitar las decisiones de diseño que limitarían los probables cambios futuros en el sistema.                                                  |
| Apéndices | Estos deben proporcionar información detallada y la información específica que se relaciona con la aplicación en desarrollo; por ejemplo, el hardware y las descripciones de bases de datos. Requerimientos de hardware definen las configuraciones de mínimos y óptimos para el sistema. Los requerimientos de base de datos definen la organización lógica de los datos utilizados por el sistema y las relaciones entre los datos. |
| Índice | Se pueden incluir varios índice. Así como un índice alfabético normal, puede haber un índice de diagramas, un índice de funciones, y así sucesivamente. |

---
### Especificación de requerimientos
* El proceso de escribir los requerimientos del sistema del usuario y en un documento de requisitos.
* Los requerimientos de usuario tienen que ser comprensibles por los usuarios finales y los clientes quienes no tienen una formación técnica.
* Los requerimientos del sistema son requerimientos más detallados y pueden incluir más información técnica.
* Los requerimientos pueden ser parte de un contrato para el desarrollo del sistema 
  * Por lo tanto, es importante que estos sean tan completos como sea posible.

---
### La estructura de un documento de requerimientos
| Notación | Descripción                                                                                                                                                                                                                                                                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lenguaje natural | Los requerimientos están escritos con oraciones numeradas en lenguaje natural. Cada oración debe expresar un requerimiento.                                                                                                                                                                                                                                                                       |
| Lenguaje natural Estructurado | Los requerimientos están escritos en lenguaje natural en un formulario o plantilla estándar. Cada campo proporciona información acerca de un aspecto del requerimiento.                                                                                                                                                                                                                           |
| Lenguajes de descripción de Diseño | Este enfoque utiliza un lenguaje como un lenguaje de programación, pero con características más abstractas para especificar los requisitos mediante la definición de un modelo operacional del sistema. Este enfoque se utiliza raramente aunque puede ser útil para las especificaciones de interfaz.                                                                                            |
| Notaciones graficas | Modelos gráficos, complementada con anotaciones de texto, se utilizan para definir los requisitos funcionales para el sistema; UML de casos de uso y diagramas de secuencia se utilizan comúnmente.                                                                                                                                                                                               |
| Especificaciones matemáticas | Estas anotaciones se basan en conceptos matemáticos, tales como máquinas de estados finitos o conjuntos. Aunque estas especificaciones no ambiguas pueden reducir la ambigüedad en un documento de requisitos, la mayoría de los clientes no entienden una especificación formal. Ellos no pueden controlar que representa lo que quieren y se resisten a aceptarlo como un contrato del sistema. |

---
### Diseño y requerimientos
En principio, los requerimientos deberán establecer lo que el sistema debe hacer y el
diseño debe describir cómo se hace esto.

* En práctica, los requerimientos y el diseño están unidos 
* Una arquitectura de sistema puede ser diseñada para respetarlos requisitos
* El sistema puede interoperar con otros sistemas que generan requisitos de diseño
* Puede ser necesario el uso de una arquitectura específica para satisfacer los requisitos no funcionales o esta puede ser
la consecuencia de un requisito reglamentario.

---
### Especificación en lenguaje natural
* Los requerimientos se escriben como sentencias en lenguaje natural complementados con diagramas y tablas.
* Se utiliza para la escritura de los requisitos, ya que es expresiva, intuitiva y universal.

**Los requisitos deben ser entendidos por los usuarios y clientes**

---

32 de 74

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
