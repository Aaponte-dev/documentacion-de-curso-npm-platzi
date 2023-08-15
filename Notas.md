# [*Curso de NPM: Gestión de Paquetes y Dependencias en JavaScript(**Platzi**)*](https://platzi.com/cursos/npm/)

NPM es el gestor de paquetes y dependencias más usado para desarrollar con JavaScript. Con NPM podrás administrar módulos, distribuir paquetes y agregar dependencias a tus proyectos. Crea tus propias librerías y domina una de las herramientas más importantes en el desarrollo con JavaScript. Tu profesor, Oscar Barajas te enseña a:

* Versionar paquetes en NPM.
* Publicar paquetes en NPM.
* Crear paquetes para NPM.
* Actualizar y eliminar dependencias.

> Instructor: **Oscar Barajas Tavares**

## Temario

1.- Bienvenido(a) a NPM

Te damos la bienvenida al Curso de NPM: Gestión de Paquetes y Dependencias en JavaScript.

En este curso aprenderás a:

* Qué es NPM, dependencias y paquetes
* Cómo instalar dependencias a un proyecto
* Cómo compartir y crear paquetes para la comunidad
* Cómo funcionan los paquetes públicos y privados en NPM

Herramientas que emplearás

* Visual Studio Code: es el editor de código que se recomienda utilizar para tus proyectos y ofrece varias características para mejorar tu experiencia en el desarrollo.
* Una terminal, ya sea en MacOS, Linux, o Windows Subsystem for Linux. Si no sabes qué es la terminal, toma el curso de: [Introducción a la Terminal y Línea de Comandos](https://platzi.com/cursos/terminal/).

Contribuciones del curso creadas por Andrés Guano (Platzi Contributor).

2.- Gestión de dependencias

Un módulo es un archivo (de JavaScript) que contiene una parte de la solución de un problema.

Un paquete o librería es el conjunto de módulos para resolver un problema.

Una dependencia, como su nombre lo indica, es un paquete que tu proyecto necesita para funcionar.

La gestión de dependencias es la forma de compartir recursos creados y validados por terceros entre la comunidad. Los gestores de dependencias permiten organizar, administrar y brindar herramientas para el manejo de paquetes. Esta es la importancia de NPM (Node Package Manager), el gestor de dependencias más popular en js.

Breve reseña histórica:

* En 1995, se crea JavaScript, uno de los lenguajes más populares y el único para la interactividad en páginas web.
* En 2009, se crea Nodejs, un entorno de ejecución de JavaScript en el lado del servidor. En este año también se crea NPM, el gestor de dependencias que nace junto a Nodejs.

Importancia de los gestores de dependencias:

Los gestores de dependencias, por ejemplo NPM, permiten organizar, administrar y brindar herramientas para el manejo de paquetes. Esto permite a los desarrolladores trabajar sobre sus propios problemas, sin preocuparse de solucionar otros problemas ya resueltos.

Según sea el caso, puedes utilizar paquetes y módulos en tu proyecto. Sin embargo, el abuso de estos puede generar problemas en tu proyecto, desde la inclusión de bugs, problemas de seguridad, o que el paquete deje de ser mantenido y validado.

La página oficial de NPM permite conocer toda la información de un paquete. Por ejemplo, React es un paquete para construir interfaces gráficas, en la página del paquete de React tendrás información de instalación, participantes, versiones, documentación y posibles soluciones de errores.

Existen otros gestores de dependencias, como Yarn o PNPM. No obstante, en este curso se tratará sobre NPM, ya que es el más popular. Aunque estos gestores comparten funcionalidades en común.

Contribución creada por Andrés Guano (Platzi Contributor).

3.- Instalación de NPM en MacOS

4.- Instalación de NPM en Windows

5.- Primeros pasos en NPM

Desde una terminal o línea de comandos, crea un directorio con el nombre de tu proyecto. Después, como buena práctica, inicia un repositorio local de Git dentro de la carpeta creada.

El símbolo $ representa la línea de entrada para los comandos en la terminal.

```bash
Terminal

$ mkdir npm
$ cd npm
$ git init //Initialized empty Git repository in /pruebas/.git/
```

Una vez creado el espacio correspondiente al proyecto de JavaScript. Deberás tener un archivo de configuración llamado `package.json.`

### Cómo estructurar un archivo de configuración package.json

El archivo `package.json` es un archivo de configuración que contiene la información más importante de tu proyecto como: datos específicos, dependencias, dependencias de desarrollo y archivos de ejecución.

Este archivo, como su extensión lo indica, está estructurado en formato JSON (JavaScript Object Notation) que sirve para una mejor lectura e interpretación para los usuarios y las máquinas.

### Datos específicos del archivo package.json

Los datos específicos ayudan a identificar el proyecto y actúan como una base para que los usuarios y los contribuidores obtengan información sobre el proyecto.

El archivo `package.json` estaría estructurado inicialmente por las siguientes propiedades:

```bash
"name": Indica el nombre del proyecto.
"version": Indica la versión del proyecto.
"description": Indica una breve descripción del proyecto.
"main": Indica el archivo principal del proyecto.
"scripts": Indica los comandos a ejecutar del proyecto (no te preocupes por el comando test por ahora).
"keywords": Indica las palabras clave del proyecto.
"author": Indica el nombre y dirección de correo electrónico del propietario del proyecto.
"license": Indica la licencia del proyecto.
```

El archivo package.json estaría estructurado de la siguiente manera:

``` bash
{
    "name": "npm",
    "version": "1.0.0",
    "description": "Constuir un paquete para node",
    "main": "src/index.js",
    "scripts": {
        "test": "echo \"Error no test specified\" && exit 1"
    },
    "keywords": [ "javascript", "node", "package" ],
    "author": "TuNombre tucorreo@gmail.com",
    "license": "MIT"
}
```

### Cómo utilizar el comando npm init

Aunque puedes crear el archivo de configuración manualmente, NPM te ayuda a crearlo rápidamente mediante el comando npm init. Este comando te permite ingresar los datos específicos del proyecto y genera el archivo package.json en tu directorio.

```bash
# This utility will walk you through creating a package.json file. It only covers the most common items, and tries to guess sensible defaults.
$ npm init

# See npm help init for definitive documentation on these fields and exactly what they do.

# Use npm install <pkg> afterwards to install a package and save it as a dependency in the package.json file.

Press ^C at any time to quit. package name: (npm)
```

Puedes ingresar tus propios datos, o utilizar la recomendación de NPM (lo que está entre paréntesis) y solamente dar enter. Al final, te preguntará si la configuración del package.json es correcta para generar el archivo.

```bash
version: (1.0.0)
description: Constuir un paquete para node
entry point: (index.js) src/index.js
test command: npm test git
repository:
keywords: javascript, node, package author: TuNombre tucorreo@gmail.com license: (MIT) About to write to /npm/package.json:

{
    "name": "npm",
    "version": "1.0.0",
    "description": "Constuir un paquete para node",
    "main": "src/index.js",
    "scripts": {
        "test": "echo \"Error no test specified\" && exit 1"
    },
    "keywords": [ "javascript", "node", "package" ],
    "author": "TuNombre tucorreo@gmail.com", "license": "MIT"
}

Is this OK? (yes)
```

### Cómo utilizar el comando npm init --yes

El comando npm init --yes o npm init -y te ayudará a crear un archivo package.json de manera rápida con una configuración por defecto, sin la necesidad de ingresar los datos.

Para establecer esta configuración por defecto, necesitarás utilizar el comando npm config set init-`atributo`. Te comparto algunas de las configuraciones por defecto más comunes:

```bash
Terminal
$ npm config set init-author-name "Tu Nombre"
$ npm config set init-author-email "<TuEmail@email.com>"
$ npm config set init-author-url "<https://tuWeb.com>"
$ npm config set init-license "MIT"
$ npm config set init-version "0.0.1"
```

De esta manera ya estás listo para gestionar dependencias de tu proyecto con NPM.

Contribución creada por Andrés Guano (Platzi Contributor).

### Documentación asociada

[Comandos npm](https://docs.npmjs.com/cli/v9/commands)

[Comando npm init](<https://docs.npmjs.com/cli/v9/commands/npm-init>)
