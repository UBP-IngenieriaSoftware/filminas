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
Se refiere a la estructura y organización a gran escala de un sistema de software. Es la planificación de los componentes 
principales de un sistema y la forma en que interactúan entre ellos. El diseño arquitectónico se enfoca en la visión 
global del sistema, definiendo módulos, componentes, subsistemas, bases de datos, servidores y cómo todo se conecta y comunica.

----

### Diseño Arquitectónico: Ejemplo
- **Ejemplo:** Decidir si usar una arquitectura monolítica o una basada en microservicios.
- **Objetivo:** Crear una estructura robusta, escalable y eficiente que sirva de base para todo el sistema.

----

**Diseño Arquitectónico** y **Patrones de Diseño** NO son lo mismo.

----

### Patrones de Diseño
Son soluciones probadas y reutilizables para problemas comunes en el desarrollo de software a un nivel más detallado. 
Estos patrones se aplican a problemas específicos dentro del código o en la interacción de ciertos componentes, y son 
como "buenas prácticas" que se pueden seguir.

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

----

### ESTILOS ARQUITECTÓNICOS
- Un conjunto de componentes. 
- Un conjunto de conectores entre componentes (comunicación, coordinación, cooperación, etc.). 
- Restricciones que definen cómo se integran los componentes para formar el sistema. 
- Modelos que permiten comprender las propiedades de un sistema general.

----

### ¿Cómo elegir un estilo de arquitectura?
* Ventajas
* Desventajas
* Contexto

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

### MODELOS Arquitectónicos
1. Arquitectura en Capas
2. Arquitectura Cliente-Servidor
3. Arquitectura de Microservicios
4. Arquitectura de Capas N
5. Arquitectura Orientada a Servicios
6. Arquitectura Basada en Eventos
7. Arquitectura de Tubería y Filtro
8. Arquitectura de Espacio de Nombres
9. Arquitectura de Sistema Distribuido
10. Arquitectura Monolítica
11. Arquitectura de Microkernel
12. Arquitectura Hexagonal

----

### MODELOS Arquitectónicos

13. Arquitectura basada en Componentes
14. Arquitectura de Peer-to-Peer
15. Arquitectura CQRS (Command Query Responsibility Segregation)
16. Arquitectura Basada en Nubes
17. Arquitectura de Repositorio
18. Modelo-Vista-Controlador
19. Arquitectura de Máquina de Estados
20. Arquitectura Orientada a Objetos
21. Arquitetcura Broker (intermediario)
22. Arquitectura Master-Slave
23. Arquitectura Serverless

----

Al leer sobre cada Arquitetcura plantea si es Jerarquico o No Jerarquico

----

Estos modelos proporcionan distintas formas de organizar y estructurar un sistema de software según los requisitos del 
proyecto. La elección del modelo depende de factores como la escalabilidad, mantenimiento, distribución, complejidad y 
el tipo de problema que se está resolviendo.

---
### 1. Arquitectura en Capas
* Divide el sistema en capas o niveles donde cada capa tiene una responsabilidad específica. 
* La comunicación entre capas se da de manera jerárquica: una capa superior utiliza los servicios de una capa inferior.
* Las capas de nivel inferior representan servicios núcleo que es probable se utilicen a lo largo de todo el sistema.

----

### 1. Arquitectura en Capas: USO
* Al construirse nuevas facilidades encima de los sistemas existentes.
* Cuando el desarrollo se dispersa a través de varios equipos de trabajo, y cada uno es responsable  de una capa de funcionalidad.
* Cuando exista un requerimiento para seguridad multinivel.

----

### 1. Arquitectura en Capas: Ventajas
- Separación de preocupaciones: Cada capa tiene una responsabilidad bien definida. 
- Mantenibilidad: Los cambios en una capa no afectan directamente a otras capas. 
- Reusabilidad: Las capas pueden ser reutilizadas en diferentes sistemas.

----

### 1. Arquitectura en Capas: Desventajas
- Rendimiento: Puede haber overhead (sobrecarga) al pasar los datos a través de múltiples capas. 
- Rigidez: Puede ser difícil cambiar una capa sin afectar a las demás.

----

### 1. Arquitectura en Capas: Ejemplo
Aplicaciones web que tienen capas de presentación, lógica de negocio y acceso a datos.

----

### 1. SISTEMA DE GESTIÓN

![Sistema de Gestión](images/unidad6/sistema-gestion.jpg)

----

### 1. SISTEMA DE BIBLIOTECA

![Sistema de Biblioteca](images/unidad6/sistema-biblioteca.jpg)

----

### Arquitectura de sistema de información en capas

![Arquitectura de Capas](images/unidad6/capas.png)

----

### Arquitectura del MHC-PMS

![MHC-PMS](images/unidad6/MHC-PMS.png)


---
### 2. Arquitectura Cliente-Servidor
* Sistema distribuido que muestra cómo el modelo de datos y procesamiento se distribuye a través
  de una gama de componentes.
* Conjunto de servidores independientes que ofrecen servicios específicos, tales como la
  impresión, gestión de datos, etc
* Conjunto de clientes que envian solicitudes a éstos servidores, que los procesan y responden con los resultados.
* Red que permite a los clientes acceder a los servidores.

----

### 2. Arquitectura Cliente-Servidor: Evolución

| Generación       | Características                               |
|------------------|-----------------------------------------------|
| 1ª Generación    | 	Servidores físicos dedicados, cliente pesado |
| 2ª Generación    | 	Virtualización, cliente ligero               |
| 3ª‌ Generación   | Computación‌ en la ⁢nube, SaaS                |
| 4ª⁤ Generación   | 	Microservicios, ⁣contenedores, orquestación  |

----

### 2. BIBLIOTECA DE IMÁGENES Y PELÍCULAS

![Biblioteca de Imgágenes y películas](images/unidad6/imagenes-peliculas.jpg)

----

### 2. Arquitectura Cliente-Servidor: Ventajas
- Centralización: El servidor central puede controlar y gestionar los datos y el acceso.
- Escalabilidad: Es más fácil escalar el servidor que administrar múltiples clientes.
- Mantenimiento: Es más sencillo de mantener o de transladar con sencillez el servidor a nuevo hardware/software

----

### 2. Arquitectura Cliente-Servidor: Desventajas
- No hay un modelo de datos compartidos, así que los sub-sistemas utilizan diferentes datos de la organización.
  Intercambio de datos puede ser ineficaz;
- No hay registro central de nombres y servicios - que puede ser difícil de averiguar qué servidores y servicios están
  disponibles.
- Punto único de fallo: Si el servidor falla, todos los clientes se ven afectados.
- Sobrecarga del servidor: El servidor puede saturarse si recibe demasiadas solicitudes.

----

### 2. Arquitectura Cliente-Servidor: Ejemplo
Aplicaciones web y aplicaciones de bases de datos donde el cliente interactúa con un servidor.

---
### 3. Arquitectura de Microservicios
Divide el sistema en servicios pequeños, independientes y desplegables de manera individual.
Cada microservicio se encarga de una funcionalidad específica y se comunica con otros servicios a través de protocolos 
de red ligeros (ej., HTTP, REST, gRPC).

----

### 3. Arquitectura de Microservicios: Ventajas
- Escalabilidad independiente: Los microservicios pueden escalarse de manera individual. 
- Flexibilidad tecnológica: Cada microservicio puede usar tecnologías diferentes. 
- Despliegue ágil: Los microservicios se pueden desarrollar y desplegar de forma independiente.

----

### 3. Arquitectura de Microservicios: Desventajas
- Complejidad: Gestionar múltiples microservicios puede ser complicado. 
- Sobrecarga de red: La comunicación entre microservicios puede introducir latencia. 
- Dificultad en la depuración: El diagnóstico de errores es más difícil debido a la distribución.

----

### 3. Arquitectura de Microservicios
![Arquitetcura de Microservicios](images/unidad6/microservicios.png)

----

### 3. Arquitectura de Microservicios: Ejemplo
Plataformas como Netflix o Amazon utilizan microservicios para manejar diferentes módulos como facturación, inventario, etc.

---
### 4. Arquitectura de Capas N
Similar a la arquitectura en capas, pero con la distinción de que las capas se pueden distribuir físicamente en 
diferentes servidores o ubicaciones.
Típicamente tiene capas como la capa de presentación, capa de aplicación (lógica de negocio) y capa de datos.

----

### 4. Arquitectura de Capas N: Ventajas
- Distribución física: Las capas pueden ejecutarse en diferentes servidores. 
- Seguridad: Es más fácil controlar el acceso a los datos distribuyendo los niveles.

----

### 4. Arquitectura de Capas N: Desventajas
- Complejidad: Añadir más capas introduce complejidad en el desarrollo y mantenimiento. 
- Rendimiento: La interacción entre las capas distribuidas puede generar latencia.

----

### 4. Arquitectura de Capas N: Ejemplo
Aplicaciones empresariales distribuidas que manejan un alto volumen de datos y procesamiento.

----

### 4. Arquitectura de Capas N: Ejemplo
![Arquitectura en Capas NodeJS](images/unidad6/capasN-nodeJS.png)

---
### 5. Arquitectura Orientada a Servicios
Se basa en la creación de servicios reutilizables que ofrecen funcionalidad a través de interfaces bien definidas.
Los servicios se comunican entre sí a través de un bus de servicio o directamente usando protocolos estándar como SOAP o REST.

----

### 5. Arquitectura Orientada a Servicios: Ventajas
- Interoperabilidad: Los servicios pueden comunicarse usando protocolos estándar, independientemente de la tecnología. 
- Reusabilidad: Los servicios pueden ser reutilizados en múltiples aplicaciones.

----

### 5. Arquitectura Orientada a Servicios: Desventajas
- Sobrecarga de comunicación: Los servicios se comunican a través de la red, lo que puede introducir latencia. 
- Complejidad de administración: Gestionar y coordinar muchos servicios puede ser complejo.

----

### 5. Arquitectura Orientada a Servicios: Ejemplo
Sistemas grandes como los de banca o telecomunicaciones que necesitan interoperabilidad entre diferentes servicios.

----

### 5. Arquitectura Orientada a Servicios: Esquema
![Arquitectura Orientada a Servicios](images/unidad6/Arquitectura-Orientada-a-Servicios-SOA.png)

---
### 6. Arquitectura Basada en Eventos
El sistema reacciona a eventos generados por diferentes componentes. Cada evento desencadena una o más acciones en otros 
componentes.
Se utiliza para sistemas distribuidos, asíncronos y que deben responder rápidamente a los cambios.

----

### 6. Arquitectura Basada en Eventos: Ventajas
- Desacoplamiento: Los componentes no dependen directamente entre sí, solo reaccionan a eventos. 
- Escalabilidad: Permite gestionar eventos de manera eficiente y escalar según la demanda.

----

### 6. Arquitectura Basada en Eventos: Desventajas
- Depuración difícil: Es más difícil rastrear el flujo de eventos en sistemas complejos. 
- Inconsistencia eventual: Dependiendo del diseño, puede haber retrasos en la propagación de eventos.

----

### 6. Arquitectura Basada en Eventos: Ejemplo
Sistemas de mensajería, notificaciones en tiempo real o sistemas de monitoreo.

----

### 6. Arquitectura Basada en Eventos: Esquema
![Orientación a Eventos](images/unidad6/orientacion-a-eventos.webp)

----

### 6. Arquitectura Basada en Eventos: Componentes
- **Productor de eventos:** Un productor de eventos es un componente o entidad dentro de un sistema que genera y emite eventos.
- **Consumidor de eventos:** Un consumidor de eventos es un componente o entidad dentro de un sistema que está interesado 
en recibir y procesar eventos generados por los productores de eventos. Su función principal es suscribirse a tipos 
específicos de eventos y tomar acciones en respuesta a esos eventos.

<!--Material MUY bueno https://medium.com/@diego.coder/introducci%C3%B3n-a-la-arquitectura-orientada-a-eventos-a532c71c9945 -->
<!--https://medium.com/@ktufernando/la-gu%C3%ADa-definitiva-de-la-arquitectura-del-software-f419db9c6bf7-->

---

### 7. Arquitectura de Tubería y Filtro
Organiza el procesamiento en una serie de pasos donde cada paso es un "filtro" que procesa datos y pasa el resultado al 
siguiente filtro a través de "tuberías". 
Se utiliza en aplicaciones de procesamiento de datos (tanto basadas en lotes como en transacciones),

----

### 7. Arquitectura de Tubería y Filtro

![Modelo de Tubería y Filtro](images/unidad6/modelo_tuberia-filtro.jpg)

----

### 7. Arquitectura de Tubería y Filtro: Ventajas
- Modularidad: Los filtros son independientes, lo que facilita agregar o quitar filtros. 
- Reusabilidad: Cada filtro puede reutilizarse en otros flujos de procesamiento.

----

### 7. Arquitectura de Tubería y Filtro: Desventajas
- Overhead: La transferencia de datos entre los filtros puede ser costosa. 
- Dependencia de la secuencia: El orden de los filtros puede volverse rígido y difícil de cambiar.

----

### Arquitectura de compilador de tubería y filtro

![Arquitetcura de Tubería y Filtro](images/unidad6/arquitetcura-tuberia-filtro.png)

----

### 7. Arquitectura de Tubería y Filtro: Ejemplo
Compiladores o sistemas de procesamiento de datos donde los datos pasan por varias etapas de transformación.

---
### 8. Arquitectura de Espacio de Nombres
Diseñada para sistemas altamente escalables y distribuidos, elimina la necesidad de una base de datos central y se basa 
en "espacios" de datos que son replicados o fragmentados.

----

### 8. Arquitectura de Espacio de Nombres: Ventajas
- Alta escalabilidad: Ideal para sistemas que requieren distribuir datos y procesamiento. 
- Tolerancia a fallos: Evita puntos únicos de fallo y permite replicación y partición de datos.

----

### 8. Arquitectura de Espacio de Nombres: Desventajas
- Complejidad: Requiere administración avanzada de los espacios de datos distribuidos. 
- Consistencia eventual: Puede haber tiempos en los que los datos no estén sincronizados.

----

### 8. Arquitectura de Espacio de Nombres: Ejemplo
Aplicaciones que requieren alta disponibilidad, baja latencia y gran escalabilidad horizontal, como sistemas 
financieros o redes sociales.

---
### 9. Arquitectura de Sistema Distribuido
En esta arquitectura, los componentes del sistema se ejecutan en múltiples máquinas distribuidas y se comunican entre sí 
a través de una red.

----

### 9. Arquitectura de Sistema Distribuido: Ventajas
- Escalabilidad horizontal: Puedes añadir más nodos al sistema para escalar. 
- Disponibilidad: Los nodos distribuidos pueden mantener el sistema operativo, incluso si algunos fallan.

----

### 9. Arquitectura de Sistema Distribuido: Desventajas
- Consistencia: Mantener los datos consistentes en diferentes nodos puede ser complicado. 
- Latencia de red: La comunicación entre nodos distribuidos puede generar demoras.

----

### 9. Arquitectura de Sistema Distribuido: Ejemplo
Sistemas de computación en la nube o aplicaciones que utilizan redes P2P (peer-to-peer).

---
### 10. Arquitectura Monolítica
El sistema se construye como una única aplicación, donde todos los componentes están interconectados y ejecutados juntos.

----

### 10. Arquitectura Monolítica: Esquema
![Arquitetcura Monolítica](images/unidad6/monolitica.png)

----

### 10. Arquitectura Monolítica: Ventajas
- Simplicidad: Más fácil de desarrollar y desplegar en las primeras etapas. 
- Eficiencia: Todo el código corre en un solo proceso, reduciendo la latencia de comunicación.

----

### 10. Arquitectura Monolítica: Desventajas
- Difícil de escalar: A medida que crece el sistema, es difícil escalar partes específicas. 
- Mantenibilidad: Los cambios en una parte pueden afectar otras partes del sistema.

----

### 10. Arquitectura Monolítica: Ejemplo
Aplicaciones tradicionales o más simples, como pequeñas aplicaciones empresariales.

---
### 11. Arquitectura de Microkernel o Plug-in
Separa el núcleo de la aplicación (core system) de la funcionalidad extensible, permitiendo que se agreguen plugins o 
módulos que amplíen las funcionalidades.

----

### 11. Arquitectura de Microkernel: Esquema
![Arquitetcura de Microkernel](images/unidad6/microkernel.webp)

----

### 11. Arquitectura de Microkernel: Ventajas
- Extensibilidad: Nuevos módulos pueden añadirse sin afectar el núcleo del sistema. 
- Mantenibilidad: El núcleo es pequeño y fácil de mantener.

----

### 11. Arquitectura de Microkernel: Desventajas
- Rendimiento: La comunicación entre el núcleo y los módulos puede ser ineficiente. 
- Complejidad en la gestión de plugins: Puede ser complicado gestionar las interacciones entre módulos.

----

### 11. Arquitectura de Microkernel: Ejemplo
Sistemas operativos o aplicaciones que necesitan una base estable pero pueden ampliarse mediante módulos.

---
### 12. Arquitectura Hexagonal
También conocida como Arquitectura de Puertos y Adaptadores, separa la lógica de negocio del sistema de las interfaces 
externas mediante "puertos" (interfaces) y "adaptadores" (que conectan la lógica con esas interfaces).

----

### 12. Arquitectura Hexagonal: Esquema
![Esquema Hexagonal](images/unidad6/hexagonal.png)

----

### 12. Arquitectura Hexagonal: Ventajas
- Desacoplamiento: Permite cambiar las interfaces externas sin modificar la lógica central. 
- Testabilidad: Facilita la creación de pruebas unitarias, dado el aislamiento de los puertos.

----

### 12. Arquitectura Hexagonal: Desventajas
- Complejidad: Puede ser más difícil de entender y configurar para pequeños proyectos. 
- Curva de aprendizaje: Requiere más tiempo para que los desarrolladores comprendan completamente su estructura.

----

### 12. Arquitectura Hexagonal: Ejemplo
Aplicaciones que necesitan ser adaptables y mantenibles con diferentes interfaces (por ejemplo, interfaz web, API REST).

---
### 13. Arquitectura basada en Componentes
El sistema se construye ensamblando componentes modulares que interactúan entre sí. Cada componente es independiente y 
puede ser reemplazado o reutilizado.

----

### 13. Arquitectura basada en Componentes: Ventajas
- Modularidad: Facilita la actualización o reemplazo de componentes sin afectar el resto del sistema. 
- Reusabilidad: Los componentes pueden ser reutilizados en diferentes aplicaciones.

----

### 13. Arquitectura basada en Componentes: Desventajas
- Interdependencias: Asegurar que los componentes encajen bien entre sí puede ser complicado. 
- Overhead de comunicación: La comunicación entre componentes introduce una sobrecarga.

----

### 13. Arquitectura basada en Componentes: Ejemplo
Aplicaciones empresariales donde diferentes módulos pueden ser desarrollados y mantenidos por equipos distintos.

---
### 14. Arquitectura de Peer-to-Peer
En lugar de un servidor central, cada nodo en la red actúa tanto como cliente y como servidor, compartiendo y recibiendo 
datos directamente con otros nodos.

----

### 14. Arquitectura de Peer-to-Peer: Esquema
![Arquitetcura de Peer-to-Peer](images/unidad6/p2p.jpg)

----

### 14. Arquitectura de Peer-to-Peer: Ventajas
- Escalabilidad: No hay un punto central de control, lo que permite agregar más nodos fácilmente. 
- Tolerancia a fallos: Si un nodo falla, otros pueden asumir sus responsabilidades.

----

### 14. Arquitectura de Peer-to-Peer: Desventajas
- Seguridad: La naturaleza distribuida puede hacer que sea más difícil asegurar. 
- Coordinación: Es complicado mantener una coordinación eficiente entre los nodos.

----

### 14. Arquitectura de Peer-to-Peer: Ejemplo
Aplicaciones como BitTorrent, Skype, o sistemas blockchain.

---
### 15. Arquitectura CQRS
Divide el manejo de los comandos (escribir o modificar datos) y las consultas (leer datos) en dos modelos separados, 
permitiendo una optimización independiente.

----

### 15. Arquitectura CQRS: Esquema
![Esquema CQRS](images/unidad6/CQRS.png)

----

### 15. Arquitectura CQRS: Ventajas
- Optimización independiente: Lecturas y escrituras pueden ser optimizadas por separado. 
- Escalabilidad: Es más fácil escalar la parte de lectura o de escritura según sea necesario.

----

### 15. Arquitectura CQRS: Desventajas
- Complejidad: Introduce más complejidad al tener dos modelos de datos separados. 
- Consistencia eventual: La sincronización entre los dos modelos puede no ser instantánea.

---

### 15. Arquitectura CQRS: Ejemplo
Aplicaciones que tienen requerimientos muy distintos para lectura y escritura de datos, como sistemas bancarios.

---
### 16. Arquitectura Basada en Nubes
Aprovecha los servicios y capacidades de la computación en la nube, distribuyendo la carga de trabajo y el almacenamiento 
en servidores remotos.

----

### 16. Arquitectura Basada en Nubes: Consta de...
- Una capa de **hardware**, que incluye servidores bare metal, equipamiento de red y dispositivos de almacenamiento
- Una capa de **virtualización**, que incluye hipervisores y componentes de redes definidos por software (SDN) para virtualizar los recursos físicos 
- Una capa de **servicios**, que incluye los recursos de nube que el proveedor entrega a los usuarios 

----

### 16. Arquitectura Basada en Nubes: Ventajas
- Elasticidad: Fácil de escalar dinámicamente según las necesidades de la aplicación. 
- Costo eficiente: Solo pagas por los recursos que usas.

----

### 16. Arquitectura Basada en Nubes: Desventajas
- Dependencia de terceros: Dependes de proveedores externos para la infraestructura. 
- Latencia: Los recursos en la nube pueden tener mayor latencia que los locales.

----

### 16. Arquitectura Basada en Nubes: Ejemplo
Aplicaciones SaaS (Software as a Service) como Google Drive, Dropbox o aplicaciones que usan Amazon Web Services (AWS) o 
Microsoft Azure.

----

### 16. Ejemplo de arquitectura en la nube de un sistema de gestión de documentos
<!-- .slide: style="font-size: 0.60em" -->
![Cloud Architecture](images/unidad6/cloud-architecture.png)
<!--https://www.akamai.com/es/blog/cloud/what-is-cloud-architecture-->

---
### 17. Arquitectura de Repositorio
Todos los componentes del sistema se comunican y comparten datos a través de un repositorio común centralizado.

El Sub-sistemas de intercambio de datos puede hacerse de dos maneras:
* Datos compartidos se lleva a cabo en un repositorio o base de datos central y puede ser visitada por todos
    los sub-sistemas;
* Cada sub-sistema mantiene su propia base de datos y pasa datos explícitamente a otros subsistemas. 

Cuando grandes cantidades de datos sean compartidos, el modelo de repositorio compartido es más comúnmente utilizado.

----

### 17. Arquitectura de Repositorio: Ventajas
- Centralización: Todos los módulos acceden a un repositorio común. 
- Facilita la integración: Los datos centralizados permiten una integración sencilla entre componentes.
- Manera eficaz de compartir grandes cantidades de datos
- Sub-sistemas no tienen por qué preocuparse de cómo los datos se producen, por ejemplo, la gestión centralizada
  copia de seguridad, seguridad, etc
- Un modelo a compartir se publica como el esquema del repositorio.

----

### 17. Arquitectura de Repositorio: Desventajas
<!-- .slide: style="font-size: 0.90em" -->
- Punto único de fallo: Si el repositorio falla, todo el sistema se ve afectado. 
- Cuello de botella: El acceso concurrente al repositorio puede ser un cuello de botella en el rendimiento.
- Sub-sistemas deben ponerse de acuerdo sobre un modelo repositorio de datos. Inevitablemente, un compromiso
- La evolución de datos es difícil y costosa
- No hay lugar para las políticas de gestión específica
- Difícil de distribuir de manera eficiente


----

### 17. Arquitectura de Repositorio: Ejemplo
Sistemas de bases de datos o sistemas de información compartida donde múltiples módulos acceden a un almacenamiento común.

----

### 17. ARQUITECTURA DE REPOSITORIO IDE

![Repositorio IDE](images/unidad6/repositorio-IDE.jpg)

---

#### 17. Arquitectura de repositorio para un sistema de procesamiento de lenguaje

![Arquitetcura de Repositorio para un sistema de Procesamiento de Lenguaje](images/unidad6/Arquitetcura-de-repositorio.png)

---
### 18. Arquitectura Modelo-Vista-Controlador
<!-- .slide: style="font-size: 0.80em" -->
- Separa **presentación** e **interacción** de los **datos** del sistema.
- El sistema se estructura en **3** componentes lógicos.
- El componente **Modelo** maneja los _datos_ del sistema y las operaciones asociadas a esos datos.
- El componente **Vista** define y gestiona cómo se _presentan_ los datos al usuario.
- El componente **Controlador** dirige la _interacción_ del usuario y pasa estas interacciones a Vista y Modelo.

----

### 18. Arquitectura Modelo-Vista-Controlador

![Modelo Vista-Controlador](images/unidad6/modelo-vista-controlador.jpg)

----

### 18. APLICACION WEB CON ARQUITECTURA MVC

![Arquitetcura MVC](images/unidad6/arquitetura-mvc.jpg)

----

### 18. Arquitectura Modelo-Vista-Controlador: USO
- Cuando existen múltiples formas de ver e interactuar con los datos
- Al desconocerse los requerimientos futuros para la interacción y presentación.
- Aplicaciones web y frameworks como Django (Python), Ruby on Rails, ASP.NET, y Spring (Java). En el contexto de 
aplicaciones de una sola página (SPA), frameworks como Angular, React y Vue.js utilizan variantes de MVC o patrones similares como MVVM (Model-View-ViewModel).

----

### 18. Arquitectura Modelo-Vista-Controlador: Ventajas
<!-- .slide: style="font-size: 0.80em" -->
- Separación de responsabilidades: Divide la aplicación en tres componentes independientes (modelo, vista y controlador), 
lo que facilita el mantenimiento y la evolución del código.
- Reusabilidad de la vista: Las vistas pueden cambiarse o reutilizarse sin afectar la lógica de negocio ni el controlador.
- Facilita el desarrollo en equipo: Los desarrolladores pueden trabajar en la lógica de negocio (modelo), en la interfaz (vista) y en la interacción (controlador) de forma paralela. 
- Mejor organización del código: Promueve una estructura modular y limpia, haciendo más fácil agregar nuevas funcionalidades. 
- Escalabilidad: La separación de componentes permite escalar cada parte del sistema de manera más controlada.

----

### 18. Arquitectura Modelo-Vista-Controlador: Desventajas
<!-- .slide: style="font-size: 0.80em" -->
- Complejidad inicial: Para proyectos pequeños o simples, MVC puede ser demasiado complejo y crear overhead innecesario. 
- Dependencias entre componentes: Aunque los componentes están separados, suelen existir fuertes dependencias entre el controlador y la vista, lo que puede dificultar el desacoplamiento completo. 
- Curva de aprendizaje: Entender y dominar bien el patrón MVC puede ser desafiante, especialmente para nuevos desarrolladores. 
- Sobrecarga en pequeñas aplicaciones: Puede añadir complejidad innecesaria cuando se aplica en sistemas pequeños que no requieren tal nivel de separación.

---
### 19. Arquitectura de Máquina de Estados
Organiza el sistema en una serie de estados predefinidos que reaccionan a eventos. Cada transición entre estados se 
desencadena por un evento específico, y la máquina de estados pasa de un estado a otro en función de la entrada recibida. 
Es especialmente útil para sistemas donde el comportamiento varía según el estado actual del sistema.

----

### 19. Arquitectura de Máquina de Estados: Ventajas
- **Claridad y Simplicidad:** Facilita la representación clara del comportamiento del sistema en función de estados y transiciones. 
- **Predecible y fácil de depurar:** Cada estado tiene un comportamiento bien definido, lo que hace que sea más fácil depurar el sistema. 
- **Manejo sencillo de eventos:** Ideal para aplicaciones que dependen de eventos, como sistemas de control o automatización. 
- **Modularidad:** Los estados pueden diseñarse como módulos independientes, lo que facilita el mantenimiento y la evolución del sistema.

----

### 19. Arquitectura de Máquina de Estados: Desventajas
- **Complejidad:** Si hay demasiados estados o transiciones, el sistema puede volverse difícil de gestionar y escalar.
- **Dificultad en cambios dinámicos:** Cambiar o agregar nuevos estados y transiciones puede ser complicado sin romper la lógica existente.
- **Rígido:** No es ideal para sistemas donde el comportamiento no se puede describir fácilmente en términos de estados discretos.
- **Sobrecarga en diseño:** Para sistemas simples, el diseño de una máquina de estados puede ser innecesariamente complejo.

----

### 19. Arquitectura de Máquina de Estados: Uso
- Sistemas de control en tiempo real: Como controladores de tráfico, robots, ascensores. 
- Videojuegos: Para gestionar estados de personajes, niveles y eventos de juego. 
- Protocolos de comunicación: Donde las conexiones pasan por diferentes estados como conectando, conectado, desconectado. 
- Interfaces de usuario: Donde las interacciones del usuario y las interfaces gráficas se pueden representar mediante estados.

---

### 20. Arquitectura Orientada a Objetos
Organiza el sistema en objetos, que encapsulan tanto datos (atributos) como comportamientos (métodos). Estos objetos 
interactúan entre sí enviando mensajes o invocando métodos, y cada uno representa una entidad o concepto del mundo real.

----

### 20. Arquitectura Orientada a Objetos: Ventajas
- **Reusabilidad:** Los objetos y clases pueden reutilizarse en otros proyectos o partes del sistema mediante herencia y polimorfismo.
- **Modularidad:** El sistema se organiza en objetos que pueden desarrollarse y mantenerse de forma independiente.
- **Escalabilidad:** Facilita la creación de sistemas complejos mediante la creación de relaciones entre objetos (composición, herencia).
- **Mantenibilidad:** Facilita el mantenimiento y la evolución del sistema, ya que los cambios en un objeto no necesariamente afectan a otros.
- **Correspondencia con el mundo real:** Representar entidades del mundo real como objetos hace que el diseño sea más intuitivo y natural.

----

### 20. Arquitectura Orientada a Objetos: Desventajas
- **Sobrecarga de rendimiento:** Las llamadas a métodos y la interacción entre objetos pueden generar una pequeña sobrecarga en el rendimiento.
- **Complejidad inicial:** Puede ser más complicado de entender para desarrolladores sin experiencia en programación orientada a objetos.
- **Riesgo de sobre-ingeniería:** A veces los desarrolladores tienden a crear clases y objetos innecesarios, complicando el sistema.
- **Herencia compleja:** El mal uso de la herencia puede llevar a un diseño rígido y difícil de cambiar.

---

### 21. Arquitectura Broker (Intermediario)
Los componentes de software (clientes y servidores) no interactúan directamente entre sí, sino que lo hacen a través de 
un broker o intermediario que gestiona las comunicaciones. 

El broker recibe solicitudes de los clientes y las envía al servidor adecuado para su procesamiento.

----

### 21. Arquitectura Broker: Ventajas
- **Escalabilidad:** Al ser todas las tareas ejecutadas independientes las unas de las otras es posible escalar 
facilmente el sistema y sólo es necesario disponer de nuevos servidores que puedan procesar las peticiones del broker.
- **Rendimiento:** Al ser un gran número de nodos conectados a lo que simplemente actúa como un puente con el cliente 
el rendimiento puede mantenerse siempre en altas escalas ya que es posible redistribuir si es necesario y procesar 
grandes cargas de peticiones en momentos de saturación

----

### 21. Arquitectura Broker: Desventajas
- **Costo:** Es necesario tener un gran número de servidores, que deben de ser mantenidos independientemente, con 
diferentes piezas de software distribuidas entre ellos.
- **Mantenimiento:** Este sistema distribuido implica que cualquier falla debe de poder deberse a cualquier pieza, 
igualmente realizar tareas de mantenimiento en la máquina broker puede implicar tiempos sin disponibilidad de servicio.

----

### 21. Arquitectura Broker: Ejemplos
Arquitecturas de mensajería o middleware, como sistemas de colas de mensajes (MQ).
RabbitMQ, Apache Kafka o sistemas de intermediación de datos en servicios distribuidos.

----

### 21. Arquitectura Broker: Esquema

![Broker](images/unidad6/broker.png)

---

### 22. Arquitectura Master-Slave
Un nodo principal (master) controla uno o más nodos secundarios (slaves). El master delega tareas a los slaves, 
coordina su trabajo y recopila resultados. 

Esta arquitectura es común cuando se necesita distribuir tareas y luego consolidar los resultados.

----

### 22. Arquitectura Master-Slave: Ventajas
- **Gestión centralizada:** Destaca para el diseño de tareas multi-tarea ya que permite dividir las tareas en diferentes 
módulos que pueden ser ejecutados de forma independiente.
- **Control:** Al partir todas las tareas de un único nodo orquestador, se mantiene mayor control ya que las tareas se 
ejecutan de manera independiente y reciben el contexto y su procesamiento final de un único punto de la ejecución.
- **Escalabilidad:** Al ser todas las tareas ejecutadas independientes las unas de las otras es posible escalar 
fácilmente el sistema de forma que añadir nuevos nodos esclavos se termine traduciendo en un más que posible aumento del rendimiento.

----

### 22. Arquitectura Master-Slave: Desventajas
- **Implementación:** NDebe de existir la posibilidad de dividir el proyecto en módulos que puedan actuar aislados de 
la ejecución principal del programa.
- **Dependencia:** Fuerte dependencia con el sistema en el que se haya implementado que en muchas ocasiones hace difícil 
portarlo a otras máquinas distintas.

----

### 22. Arquitectura Master-Slave: Ejemplos
En sistemas de bases de datos distribuidas, los masters controlan las réplicas de slaves; en el caso de sistemas de alta 
disponibilidad, el master toma decisiones, y los slaves actúan como copias de respaldo o ejecución en paralelo.

----

### 22. Arquitectura Master-Slave: Esquema

![Master-Slave](images/unidad6/master.png)

---
### 23. Arquitectura Serverless
No significa que no haya servidores, sino que la administración de servidores está completamente abstraída del 
desarrollador. Los desarrolladores solo se ocupan del código y la lógica de negocio, mientras que el proveedor de la 
nube maneja la infraestructura, escalabilidad y disponibilidad automáticamente.

----

### 23. Arquitectura Serverless: Ejemplos
Servicios como AWS Lambda, Azure Functions o Google Cloud Functions permiten ejecutar código en respuesta a eventos 
sin preocuparse por la infraestructura subyacente.

----

### 23. Arquitectura Serverless: Uso
Se utiliza principalmente en arquitecturas basadas en eventos, para implementar microservicios, y en casos donde la 
elasticidad es crucial, ya que se escala automáticamente según la demanda.

---
Hay muchas más arquitetcuras... 
- Arquitectura de Cola de Mensajes
- Arquitectura de Barrera (Barrier)
- Arquitectura de Mensajería Asíncrona
- Arquitectura Lambda
- Arquitectura de Controlador de Interrupciones
- Arquitectura de Seguridad Zero-Trust
- Arquitectura de Capas Limpias o Clean Architecture

---

### Ejercicio
¿Qué estilo o estilos arquitectónicos resultan aplicables?
1. La aplicación necesita procesar la entrada en forma de flujo continuo (stream) y producir
una salida también en forma de flujo continuo.
2. Hay una gran cantidad de usuarios que se conectarán al sistema a través de una red.
3. La aplicación necesita ser ejecutada en diferentes plataformas.
4. El sistema debe tener una alta performance tanto en tiempo como en espacio (memoria).
5. El sistema debe ser capaz de ser ajustado para alcanzar el mejor uso de los recursos de
software y hardware, los cuales pueden ser cambiados en el futuro.
6. Una componente clave del sistema es la solución de un problema recurrente en el
dominio de aplicación. Se desea reusar lo componentes en sistemas similares.

---
### Jerarquía
Los estilos arquitectónicos pueden clasificarse en jerárquicos y no jerárquicos, según la forma en que organizan y 
estructuran los componentes dentro del sistema.

----

#### Estilos Arquitectónicos Jerárquicos
Estos estilos organizan el sistema de forma estructurada, donde las capas o componentes tienen una jerarquía y se 
comunican de manera controlada o secuencial.
1. Arquitectura en Capas
2. Arquitectura de Capas N
3. Arquitectura Cliente-Servidor
4. Arquitectura Monolítica
5. Arquitectura de Microkernel
6. Arquitectura de Sistema Distribuido (si incluye jerarquía de nodos)
7. Modelo-Vista-Controlador (MVC)
8. Arquitectura Master-Slave
9. Arquitectura CQRS
10. Arquitectura Broker

----

#### Estilos Arquitectónicos No Jerárquicos
Estos estilos permiten una estructura más flexible, donde los componentes se comunican directamente entre sí sin una 
dependencia estricta de capas o jerarquías predefinidas.
1. Arquitectura de Microservicios
2. Arquitectura Orientada a Servicios (SOA)
3. Arquitectura Basada en Eventos
4. Arquitectura de Tubería y Filtro
5. Arquitectura de Espacio de Nombres
6. Arquitectura Hexagonal
7. Arquitectura basada en Componentes
8. Arquitectura Peer-to-Peer
9. Arquitectura Basada en Nubes
10. Arquitectura de Repositorio
11. Arquitectura de Máquina de Estados
12. Arquitectura Orientada a Objetos
13. Arquitectura Serverless

---
### Ejercicio
Elabora una tabla comparativa de los diseños arquitectónicos comparando:
- Rendimiento
- Escalabilidad
- Complejidad de Desarrollo
- Mantenibilidad
- Reusabilidad
- Modularidad
- Tolerancia a Fallos
- Eficiencia

---
### Estructura de las aplicaciones de procesamiento de transacción

![Estructura de las aplicaciones de procesamiento de transacción](images/unidad6/procesamiento-transaccion.png)

---
### Arquitectura de software de un sistema ATM

![ATM](images/unidad6/ATM.png)

---
#### Arquitectura de un sistema de procesamiento de lenguaje

![Lenguaje de Procesamiento del Sistema](images/unidad6/arquitetcura-procesamiento.png)

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)

<!--https://refactoring.guru/design-patterns/what-is-pattern-->
<!--https://blog.spanish-smartbrain.com/software-architecture-patterns-types.html-->