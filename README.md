<div style="font-size: 16px; line-height: 1.65;">

<br/>
<div align="center">
  <img src="assets/images/upc-logoo.png" alt="UPC Logo" width="80">
</div>
<br/>
<h3 align="center"><strong>Universidad Peruana de Ciencias Aplicadas</strong></h3>
<h3 align="center"><strong>Carrera de Ingeniería de Software</strong></h3>

<h2 align="center"><strong>1ASI0730</strong></h2>
<h2 align="center"><strong>Aplicaciones Web</strong></h2>
<h3 align="center">NRC</h3>
<h2 align="center"><strong>16129</strong></h2>
<h2 align="center"><strong>Informe del Trabajo</strong></h2>
<h3 align="center">Docente</h3>
<h2 align="center"><strong>Sanchez Seña, Alberto Wilmer</strong></h2>
<h3 align="center">Equipo</h3>
<h2 align="center"><strong>NutriStartup</strong></h2>
<h3 align="center">Proyecto</h3>
<h2 align="center"><strong>NutriApp Integral</strong></h2>

<h2 align="center"><strong>Integrantes:</strong></h2>

<div align="center">
  <table align="center">
    <thead>
      <tr>
        <th align="center" >Código</th>
        <th align="center" >Apellidos y Nombres</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td align="center" >U202418250</td>
        <td align="center" >Poly Gabriel Alcantara Baldeon</td>
      </tr>
      <tr>
        <td align="center" >U202412447</td>
        <td align="center" >Waldo Alonso Portal Inga</td>
      </tr>
      <tr>
        <td align="center" >U202316162</td>
        <td align="center" >Giordano Sebastian Del Ángel Trejo Espejo</td>
      </tr>
      <tr>
        <td align="center" >U202416903</td>
        <td align="center" >Gabriel Alejandro Vilchez Vite</td>
      </tr>
      <tr>
        <td align="center" >U202312343</td>
        <td align="center" >Alejandro Franklin, Mendoza Vergara</td>
      </tr>
    </tbody>
  </table>
</div>

<h2 align="center"><strong>Período 202620</strong></h2>
<h2 align="center"><strong>Setiembre 2026</strong></h2>

</div>

# Capítulo V: Product Implementation

## 5.1. Software Configuration Management

A continuación, presentaremos el proceso por el cual organizamos, gestionamos y controlamos los cambios en el desarrollo de este proyecto.

### 5.1.1. Software Development Environment Configuration

Requirements Management

1. Trello: Es una herramienta utilizada para gestionar el flujo de trabajo de proyectos principalmente basados en marcos de
   trabajos ágiles. Será empleado para visualizar y actualizar el estado actual de las tareas e historias de usuario
   pertenecientes al sprint a desarrollar.  
   Ruta de referencia: https://trello.com/es

Product UX/UI Design

1. Figma: Plataforma de elaboración de prototipos y edición gráfica, principalmente utilizado para el diseño digital. En el
   caso del proyecto, será utilizado para el prototipado de la aplicación y sus versiones de Desktop y Mobile Web Browser.

   Ruta de referencia: https://www.figma.com/login

2. Lucidchart: Aplicación para diagramar flujos. Será empleado para el diseño de wireflows, user-flows y el diagrama de
   clases asociado a la aplicación.

   Ruta de referencia: https://www.lucidchart.com/

Software Development

1. WebStorm: Entorno de desarrollo integrado elegido por su soporte completo para tecnologías web como JavaScript, HTML, CSS y frameworks como React y Angular. Ofrece refactorización avanzada, depuración, integración con Git y la posibilidad de agregar plugins. Es compatible con varios sistemas operativos, facilitando la colaboración en equipo.

   Ruta de referencia: https://www.jetbrains.com/webstorm/
   <br>

2. HTML5: HyperText Markup Language, o por sus siglas HTML, es un lenguaje de etiquetado para páginas web. Será
   empleado en el desarrollo del proyecto para la presentación del contenido en la aplicación.

   Ruta de referencia: https://www.w3schools.com/html/html5_syntax.asp  
   <br>

3. CSS: Cascading Style Sheets es un lenguaje que maneja el diseño y presentación de las páginas web, el cual va de la mano
   con HTML.

   Ruta de referencia: https://google.github.io/styleguide/htmlcssguide.html
   <br>
   <br>

4. JavaScript: Es un lenguaje de programación interpretado y orientado a objetos. Se utilizará para elaborar la interfaz de
   usuario dentro de la aplicación.

   Ruta de referencia: https://developer.mozilla.org/es/docs/Web/JavaScript

 <br>

5. Git: Una herramienta de control de versiones que facilita el registro y la gestión de las distintas versiones del programa. Su propósito es mantener un historial de cambios y simplificar la corrección de errores. Los integrantes del equipo
   accederán a través de la línea de comandos en sus sistemas locales.

Ruta de referencia: https://git-scm.com/
<br>
<br>
Software Documentation and Project Management 6. Github: Una plataforma en la nube que hospedará los repositorios de código del proyecto. Permitirá la colaboración en
tiempo real y la revisión de contribuciones de cada miembro del equipo. Los integrantes del equipo podrán acceder a través de sus navegadores web.

Ruta de referencia: https://github.com/

<br>

Software Deployment

1. Github Pages: GitHub Pages es un servicio de alojamiento web que permite a los usuarios crear y publicar sitios web estáticos directamente desde sus repositorios de GitHub. Es especialmente útil para proyectos personales, portafolios, documentación de proyectos o blogs.

Ruta de referencia: https://pages.github.com/

### 5.1.2. Source Code Management

El proyecto seguirá las convenciones del flujo de trabajo establecido por el modelo GitFlow para el control de versiones, empleando GitHub como plataforma y sistema de control de versiones. A continuación, se describirá la implementación de GitFlow como un flujo de trabajo para el control de versiones, junto con el enlace del Landing Page.

Repositorio de GitHub:

- Enlace para acceder a la organización en GitHub: https://github.com/1ASI0730-2620-16129-G2-NutriStartup
- Enlace para acceder al repositorio de la landing Page: https://github.com/1ASI0730-2620-16129-G2-NutriStartup/LandingPage
- Enlace para acceder al repositorio del reporte: https://github.com/1ASI0730-2620-16129-G2-NutriStartup/Report

Flujo de trabajo GitFlow

El flujo de trabajo a ser implementado para el desarrollo del proyecto se basará en el modelo propuesto por Vincent Driessen en "A successful Git branching model".

Estructura de branches (Ramas):

1. Main branch (Rama principal): Esta rama servirá como la principal para la aplicación, alojando versiones estables y finales del desarrollo. Únicamente se aceptarán cambios que hayan sido previamente probados y verificados en los features y de ahí en Developer.
2. Develop branch (Rama de desarrollo): El propósito de esta rama es facilitar los avances del proyecto en equipo y mantener los archivos centrales del desarrollo continuo.
3. Feature branch(Ramas de funcionalidad): Cada capitulo desarrollado por el equipo, o separada del enfoque actual del desarrollo, tendrá su propia rama. Una vez que una funcionalidad esté completamente trabajada, se fusionará con la rama de desarrollo del proyecto. Las convenciones para nombrar las ramas de funcionalidad seguirán un patrón descriptivo y único, por ejemplo, "feature/chapter-#".
