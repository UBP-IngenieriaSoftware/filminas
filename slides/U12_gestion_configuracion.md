---
title: Gestión de la Configuración
theme: solarized
slideNumber: true
---

#### Ingeniería de Software

## Gestión de la Configuración y
## Control de Versiones

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

### Gestión de la configuración
  - Introducción
  - Ventajas

</div>
<div class="grid-item">

</div>
</div>

---

### Gestión de la configuración

Tiene como objetivo asegurar que el producto de software sea consistente, trazable y controlado durante todo su ciclo de vida.

Podemos definir **SCM – Software Configuration Management** como el conjunto de actividades destinadas a identificar, controlar, auditar y registrar los cambios que se realizan sobre los artefactos del software.

---

### Gestión de la configuración: Ventajas
- Evitar la pérdida o sobreescritura de trabajo.
- Permitir la colaboración entre varios desarrolladores.
- Controlar versiones liberadas y en desarrollo.
- Facilitar la trazabilidad entre requisitos, código y versiones.

---

### Componentes de la gestión de configuración

<!-- .slide: style="font-size: 0.80em" -->

<table>
<thead>
    <tr>
        <th>Actividad</th>
        <th>Descripción</th>
        <th>Ejemplo</th>
</thead>
<tbody>
<tr>
    <td>
        Identificación de la configuración
    </td>
    <td>
        Determinar qué elementos (código, docs, datos, scripts) forman parte del sistema.
    </td>
    <td>
        Definir qué repositorios y carpetas están bajo control de versiones.
    </td>
</tr>
<tr>
    <td>
        Control de versiones y cambios
    </td>
    <td>
        Registrar las versiones, controlar modificaciones y resolver conflictos.
    </td>
    <td>
        Uso de Git para ramas, merges y pull requests.
    </td>
</tr>
<tr>
    <td>
        Gestión de builds y releases
    </td>
    <td>
        Automatizar la construcción del software y la entrega de versiones.
    </td>
    <td>
        CI/CD con GitHub Actions o Jenkins.
    </td>
</tr>
<tr>
    <td>
        Auditoría y trazabilidad
    </td>
    <td>
        Verificar que las versiones cumplan con los estándares y estén correctamente documentadas.	
    </td>
    <td>
        Tagging de versiones y revisión de commits.
    </td>
</tr>
<tr>
    <td>
        Gestión del cambio
    </td>
    <td>
        Evaluar, aprobar e implementar cambios de manera controlada.
    </td>
    <td>
        Sistema de tickets (Jira, Trello) con políticas de aprobación.
    </td>
</tr>
</tbody>
</table>

---

### Control de versiones
<!-- .slide: style="font-size: 0.80em" -->

Es el proceso de registrar y gestionar los cambios en los archivos de un proyecto, permitiendo mantener un historial y volver a estados previos.

Tipos de sistemas de control de versiones:

<table>
<thead>
<tr>
    <td>Tipo</td>
    <td>Características</td>
    <td>Ejemplo</td>
</tr>
</thead>
<tbody>
    <tr>
        <td>Local</td>
        <td>Guardan las versiones en la misma máquina.</td>
        <td>RCS</td>
    </tr>
    <tr>
        <td>Centralizado (CVCS)</td>
        <td>Un servidor central gestiona todas las versiones.</td>
        <td>SVN, Perforce</td>
    </tr>
    <tr>
        <td>Distribuido (DVCS)</td>
        <td>Cada desarrollador tiene una copia completa del repo con su historial.</td>
        <td>Git, Mercurial</td>
    </tr>
</tbody>
</table>

---

### Git: Flujo básico

```bash
git init
git add .
git commit -m "Primer commit"
git branch feature/login
git checkout feature/login
git merge main
git push origin main
```

---
### Git: Conceptos importantes

- **Repositorio:** contenedor del proyecto.
- **Commit:** snapshot de los cambios.
- **Branch:** línea de desarrollo independiente.
- **Merge:** integración de cambios entre ramas.
- **Tag:** marcador de una versión específica (ej. v1.0).
- **Remote:** copia alojada en un servidor (GitHub, GitLab, Bitbucket).

---

### Estrategias de branching y releases
<!-- .slide: style="font-size: 0.80em" -->

<table>
<thead>
    <tr>
        <th>Estrategia</th>
        <th>Descripción</th>
        <th>Cuándo usar</th>
    <tr>
</thead>
<tbody>
    <tr>
        <td>Feature Branching</td>
        <td>Una rama por funcionalidad.</td>
        <td>Equipos pequeños, proyectos ágiles.</td>
    </tr>
    <tr>
        <td>Git Flow</td>
        <td>Ramas principales (main, develop) y ramas de soporte (feature, release, hotfix).</td>
        <td>Equipos medianos-grandes con releases planificados.</td>
    </tr>
    <tr>
        <td>Trunk-Based Development</td>
        <td>Cambios frecuentes en main con feature flags.</td>
        <td>Integración continua, despliegue rápido.</td>
    </tr>
</tbody>
</table>

---

### Herramientas

Git, GitHub, GitLab, Bitbucket, Azure DevOps.

---
### Buenas prácticas de Versionado
- Commits pequeños, descriptivos y frecuentes.
- Usar mensajes significativos: `Ejemplo: fix: corrige validación de contraseña o feat: agrega autenticación JWT.` (emplear [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/))
- Revisiones de código mediante pull requests.
- Etiquetar versiones liberadas (git tag v1.0.0).
- Documentar convenciones (GitFlow, convención de commits, políticas de merge).

---

### TAU

Plataforma para hacer cursos (cortos), 100% gratuita, con certificados que puedes publicar en linkedin!

[Source Control for Test Automation with Git](https://testautomationu.applitools.com/git-tutorial/)

---

### Ejercicio

Aplicar control de versiones en equipo.
1. Crear un repo en GitHub.
2. Clonar el repo en grupo (2–3 integrantes).
3. Crear una rama por integrante (feature/usuario, feature/producto).
4. Cada uno agrega un módulo o archivo con una función simple.
5. Generar commits con mensajes significativos.
6. Hacer merge en develop y luego en main.
7. Crear un tag v1.0 y subirlo.

Bonus: configurar una acción de CI (GitHub Actions) para correr tests automáticos.

---
### Beneficios de una buena gestión de configuración:

- Trazabilidad total de cambios.
- Mejora la colaboración.
- Facilita auditorías y control de calidad.
- Reduce riesgos de pérdida o inconsistencia.
- Permite despliegues más seguros y automatizados.

---

## ¿Dudas, Preguntas, Comentarios?

![DUDAS](images/pregunta.gif)
