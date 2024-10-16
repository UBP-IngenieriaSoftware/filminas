---
title: Automatización de Casos de Pruebas
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Automatización de Casos de Pruebas
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

### Automatización de Casos de Pruebas
* Tecnologías de Automatización
* Cypress
* Características de Cypress
* En estadísticas...
* Otras herramientas
* Extensiones
* npm
* Ejercicio básico

</div>
<div class="grid-item">

* PageObject
* Locadores

</div>
</div>

---

### Tecnologías de Automatización
Existe una gran variedad de tecnologías que permiten el desarrollo de pruebas automatizadas.

Entre las más usadas en el mercado encontramos:
* Selenium
* Cypress

![Tecnologias de Automatizacion](images/unidad8_automatizacion/selenium_cypress.png)

----

![Downloads](images/unidad8_automatizacion/downloads.jpg)

---
#### [Cypress](https://docs.cypress.io/)
Es un framework de testing moderno, fácil de aprender y de usar y que permite ejecutar pruebas sobre aplicaciones web.
Se emplea JavaScript.

Si bien lleve menos tiempo en el mercado que Selenium, ya cuenta con una gran comunidad, y una documentación muy extensa
y completa.

Además, tiene actualizaciones frecuentes, que agregan funcionalidades.

----

#### Cypress: Ventajas

![Cypress: ventajas](images/unidad8_automatizacion/ventajas-cypress.jpg)

----

#### Cypress: Características
<!-- .slide: style="font-size: 0.90em" -->
* Se toman **capturas de pantalla** o **videos** de forma muy sencilla mientras se ejecutan los tests, sin uso de otras 
dependencias.
* Durante la ejecución, al realizar cambios en el código, los tests se **auto-ejecutan** solos.
* Es muy sencillo **espiar** un servicio, para verificar los valores ó **entubarlo** y **modificarlo**.
* Las pruebas se ejecutan de manera **rápida** y sencilla.
* **Depuración** con herramientas como Chrome DevTools.
* Se realizarn **esperas automáticas**, sin necesidad de waits o sleeps.

----

#### Cypress: Cross-Browser

![Cypress: Cross Browser](images/unidad8_automatizacion/cross-browser.jpg)

---
### Otras Herramientas
En el proceso de automatización es fundamentar contar con las siguientes herramientas:
* **IDE**: Entorno de Desarrollo Integrado
* Versionado de Código
* Integración Continua

![Otras herramientas](images/unidad8_automatizacion/otras-herramientas.png)

---
### Herramientas para Cypress
* [Nodejs](https://nodejs.org/es)
* [Git](https://git-scm.com/)
* [VSC](https://code.visualstudio.com/)

----

#### Ejercicio 1: Instalar NodeJs
1. Ingresar a https://nodejs.org/es
2. Descargar la versión recomendada
3. Realizar la instalación

----

#### Ejercicio 2: Instalar Git
1. Ingresar a https://git-scm.com/
2. Descargar git para el SO correspondiente
3. Realizar la instalación

----

#### Ejercicio 3: Instalar VSC
1. Ingresar a https://code.visualstudio.com/
2. Descargar VSC
3. Realizar la instalación

----

### Plugin o Extensiones
Son componentes adicionales que se pueden instalar en el editor de código para agregar nuevas características,
funcionalidades y mejoras.

----

### Plugin o Extensiones
<!-- .slide: style="font-size: 0.90em" -->
Algunos plugin de utilidad son:
* **ESLint**: Es una herramienta de análisis estático que ayuda al proceso de **linting**. Es decir, realiza una revisión
del código para encontrar: errores de sintaxis, código poco intuitivo o difícil de mantener, uso de "malas prácticas", 
uso de estilos inconsistentes, entre otros.
* **Path Intellisense**: Realiza el autocompletado de rutas de archivos en el código. Reduce el riesgo de errores tipográficos.
* **Prettier**: Permite formatear automáticamente el código. Mejora la legibilidad del código.

----

### Plugin o Extensiones
* **Cypress Snippets**: Permite seleccionar tests rápidamente como .only para ejecutar solo uno. También agiliza escribir funciones.
* **Cypress Helper**: Agiliza procesos de autocompletado, go to definition, entre otros.
* **Better Comments**: Coloriza los comentarios para facilitar su lectura.

----

### Plugin o Extensiones
* **Bracket Pair Colorization Toggler**: Permite asignar colores diferentes a las llaves y paréntesis para facilitar la
lectura del código.
* **GitLens**: Permite ver con facilidad quien modificó las líneas de código y cuando (especialmente útil cuando se
trabaja en equipo).

----

#### Ejercicio 4: Instalar plugins en VSC
Instalar todos los plugins necesarios en el VSC:
* ESLint
* Path Intellisense
* Prettier
* Cypress Snippets
* Cypress Helper
* Better Comments
* Bracket Pair Colorization Toggler
* GitLens

---

### Node Package Manager
**npm** es el manejador de paquetes de node, que permite descargar e instalar paquetes de JavaScript para usar en 
nuestro proyecto.

Todo proyecto **node** contiene un **package.json** donde se listan todas las librerías necesarias para el proyecto.

----

### npm init
Para crear el **package.json** por primera vez, se debe ejecutar el comando **npm init**.
Al ejecutar el comando, se permite ingresar:
* versión
* descripción
* entry point
* comandos de tests
* palabras clave
* repositorio de git
* autor
* licencia

----

#### Ejercicio 5: Instalar npm
1. Abrir el VSC
2. Ejecutar el comando **npm init** en la terminal
3. Verificar que el **package.json** se generó

----

#### Ejercicio 6: Instalar Cypress
1. Ejecutar el comando **npm install cypress** en la terminal
2. Verificar que el **package.json** se agregó cypress con la versión

----

#### Ejercicio 7: Inicializar Cypress
<!-- .slide: style="font-size: 0.90em" -->
1. Ejecutar el comando **npx cypress open** en la terminal
2. Seleccionar la opción **E2E testing**
3. Verificar los archivos nuevos que se generarán, y clickear en **Continue**
4. Seleccionar un navegador, y presionar **Start E2E testing in Chrome**
5. Click en **Scaffoolf example specs**
6. Click en **Okay, I got it!**
7. verificar que en el VSC se genero una carpeta llamada **Cypress** con 2 subcarperas> 1-getting-started y 2-advanced-examples
8. Seleccionar alguno de los tests-autogenerados de ejemplo para ejecutarlos.

---
### Page Object
Es un **patrón de diseño** que permite modelar el código y hacerlo más mantenible y utilizable (generalmente cuando hay cambios en la UI, suelen
ser de selectores, no tanto de funcionalidad, por lo que solo hay que actualizar el pageObject y no el test).

----

### Page Object

Consiste en crear un objeto por cada conjunto de elementos significativos de la interfaz con la que interactuamos.

![Page Object Model](images/unidad8_automatizacion/POM.png)

----

### Page Object
* Representa componentes web
* Evita duplicación de código
* Automatizaciones mantenibles y fáciles de entender

![Page Object Model](images/unidad8_automatizacion/POM2.png)

----

### Page Object
Aunque el nombre sugiere representar una página de nuestra aplicación, si dentro de la página existen componentes, se
puede construir un page object de ese elemento para reutilizarlo.

----

### Page Object
Ejemplo: El header se repite a través de todas las páginas de esta web, entonces, en lugar de integrar los elementos
en el PageObject de la Home, es conveniente crear un PageObject a parte.
![Componentes](images/unidad8_automatizacion/componentes.png)

----

### Page Object: Modelo 1

En la parte superior se definen los locadores de los elementos, 
en la parte inferior las funciones que devuelven esos objetos.
![POM](images/unidad8_automatizacion/pom_modelo1.jpg)

----

### Page Object: Modelo 1

Para emplearlo en los tests, primero se importa, y luego se instancia el pageObject.
![POM](images/unidad8_automatizacion/pom_modelo1_uso.jpg)

----

### Page Object: Modelo 1
**Ventajas:**
Separación de la lógica del localizador (selector) y los métodos de interacción. Esto puede hacer que el código sea más
organizado y más fácil de mantener, especialmente si la página posee muchos elementos o acciones repetitivos.

**Desventajas**
Requiere crear una instancia del pageObject antes de utilizar los métodos. 

----

### Page Object: Modelo 2

Los locadores van dentro de los métodos.

![POM](images/unidad8_automatizacion/pom_modelo2.jpg)

----

### Page Object: Modelo 2

Para emplearlo en los tests, solo se debe importar.

![POM](images/unidad8_automatizacion/pom_modelo2_uso.jpg)

----

### Page Object: Modelo 2
**Ventajas:**
Se pueden emplear los métodos directamente sin necesidad de crear una instancia de la clase. Los métodos están 
disponibles globalmente para su uso directo, lo que puede resultar en un código más conciso. 

**Desventajas**
Se puede volver más complicado si hay muchos elementos o acciones repetitivas en la página. Se podría terminar repitiendo
el mismo selector en múltiples métodos.

---
### Locadores

Un localizador es una query que busca y devuelve elementos específiicos del DOM (Document Object Model).

Orden de preferencia:
* Data-test o Data-cy
* ID
* Input Name
* Class Name
* Xpath

----

### Locadores: Data-test

![Locadores: Data-test](images/unidad8_automatizacion/locator-datatest.jpg)

----

### Locadores: ID

![Locadores: ID](images/unidad8_automatizacion/locator-id.jpg)

----

### Locadores: Name

![Locadores: Name](images/unidad8_automatizacion/locator-name.jpg)

----

### Locadores: Class

![Locadores: Class](images/unidad8_automatizacion/locator-class.jpg)

----

### Locadores: Xpath

![Locadores: xpath](images/unidad8_automatizacion/locator-xpath.jpg)

----

### Locadores: Modificadores
<!-- .slide: style="font-size: 0.80em" -->
* ```^```: Permite encontrar los elementos que en el nombre de la clase, id o atributo **empieza** con un determinado
texto. Ej: ```div[class^="ayuda_position"]```
* ```*```: Permite encontrar los elementos que en el nombre de la clase, id o atributo **contienen** un determinado
    texto. Ej: ```div[class*="user_name"]```
* ```$```: Permite encontrar los elementos que en el nombre de la clase, id o atributo **terminan** con un determinado
    texto. Ej: ```div[class$="summary_content"]```
* ```nth-child(X)```: Permite encontrar elementos en función de su posición entre un **grupo de hermanos**
Ej: ```th:nth-child(2)```
* ```nth-of-type(X)```: Permite encontrar elementos de un **tipo dado** en función de su posición entre un **grupo de hermanos**
  Ej: ```div:nth-of-type(1)```

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
