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

6.- Instalación de dependencias

Las dependencias son paquetes que vamos a utilizar en nuestro proyecto. Un paquete es el conjunto de módulos para resolver un problema. Saber manejar las dependencias en un proyecto permite desarrollar la aplicación más rápido sin partir desde cero.

Existen tres tipos de dependencias: locales, desarrollo y globales.

### Qué son las dependencias locales

Las dependencias locales son aquellas que son obligatorias para el proyecto, es decir, son las necesarias para que la aplicación funcione en producción. Producción significa que tu aplicación está disponible para usarse.

### Cómo instalar dependencias locales

Para instalar una dependencia local, utiliza uno de los siguientes comandos, donde es el nombre del paquete.

```bash
Cónsola:

$ npm install <paquete> 
$ npm install --save <paquete>
$ npm install -S <paquete>
```

Las dependencias locales se encuentran en el package.json en la propiedad "dependencies", seguido de la versión que fue instalada.

``` shell
{
    ... "dependencies":{
            "paquete": "1.0.0"
        }
}
```

### Qué son las dependencias de desarrollo

Las dependencias de desarrollo son aquellas que no son obligatorias para el proyecto, es decir, sin estas la aplicación servirá. Estas dependencias ofrecen una ayuda para construir código de forma óptima, por ejemplo, formatear el código, agregar estilos, levantar un servidor para observar los cambios.

#### Cómo instalar dependencias de desarrollo

Para instalar una dependencia de desarrollo, utiliza el siguiente comando, donde es el nombre del paquete.

```bash
Cónsola:

$ npm install --save-dev <paquete>
$ npm install -D <paquete>
```

Las dependencias de desarrollo se encuentran en el package.json en la propiedad "dev-dependencies", seguido de la versión que fue instalada.

```shell
{
    ... "dev-dependencies":{
            "paquete": "1.0.0"
        }
}
```

### Qué son las dependencias globales

Las dependencias globales son aquellas que están disponibles para todos los proyectos en tu computador, pero no aparecen el archivo de configuración package.json.

#### Cómo instalar dependencias globales

Para instalar una dependencia global, utiliza el siguiente comando, donde es el nombre del paquete.

```bash
Cónsola:

$ npm install --global <paquete>
$ npm install -g <paquete>
```

`Ten en cuenta que para instalar dependencias globales requiera permisos elevados`, esto se soluciona con la palabra reservada sudo en terminales basadas en Unix, o en Windows ejecutando la terminal como administrador. Puedes revisar este artículo: `Resolving EACCES permissions errors when installing packages globally` para evitar dar permisos cada vez que instalas una dependencia global.

`Las dependencias globales no se encuentran en el package.json`, por esta razón recomiendo no abusar de esta herramienta, ya que el archivo de configuración es muy importante para que otros desarrolladores tengan toda la información pertinente al proyecto, incluyendo las dependencias a utilizar.

### Cómo visualizar los paquetes instalados

Para ver qué dependencias locales están instaladas, ejecuta el siguiente comando:

```bash
Cónsola:

$ npm list
```

Para ver qué dependencias globales están instaladas, ejecuta uno de los siguientes comandos:

```bash
Cónsola:

$ npm list -g
$ npm list -g --depth 0
```

Puedes utilizar el flag --depth para indicar la profundidad de dependencias, esto mostrará los paquetes que contiene cada paquete.

```bash
Cónsola:

$ npm list --depth 2
```

7.- Instalación de dependencias de versiones específicas

En ciertas situaciones es necesario instalar una versión específica de un paquete, ya sea porque el proyecto no puede actualizarse a versiones recientes, o porque el equipo necesita trabajar sobre una misma versión. Saber instalar cualquier versión de un paquete es fundamental para la gestión de dependencias de tu proyecto.

### Cómo instalar una versión específica de un paquete

Para instalar una versión exacta de una dependencia, utiliza el siguiente comando, donde es el nombre del paquete y es la versión exacta.

```bash
Cónsola:

$ npm install <paquete>@<versión>
```

También puedes usar la versión latest para asegurarte que está instalando la última versión disponible del paquete.

```bash
Cónsola:

$ npm install <paquete>@latest
```

Este comando instalará la versión exacta del paquete desde el repositorio de NPM. Esto sirve para manejar diferentes versiones del paquete instalado donde sea compatible con el proyecto actual y no provoque errores.

Por ejemplo:

```bash
Cónsola:

$ npm install json-server@0.15.0
```

### Cómo instalar dependencias opcionales

Para instalar una dependencia opcional, utiliza el siguiente comando, donde es el nombre del paquete.

```bash
Cónsola:

$ npm install --save-optional <paquete>
$ npm install -O <paquete>
```

Ten en cuenta la O mayúscula, si utilizas la o minúscula, el paquete se instalará como dependencia local.

Las dependencias de desarrollo se encuentran en el package.json en la propiedad "optionalDependencies", seguido de la versión que fue instalada.

``` bash
{
    ... "optionalDependencies": {
        "paquete": "1.0.0"
    }

}
```

### Simular la instalación de una dependencia

Para simular la instalación de una dependencia, utiliza el siguiente comando, donde es el nombre del paquete.

```bash
Cónsola:

$ npm install --dry-run <paquete>
```

Este comando mostrará el resultado de instalación sin instalarlo en el proyecto.

Por ejemplo:

```bash
Cónsola:

$ npm i react --dry-run

added 4 packages in 2s

23 packages are looking for funding run npm fund for details
```

### Cómo funciona el comando npm install

El archivo `package.json` contiene la información de las dependencias del proyecto, pero si no tienes instaladas esas dependencias, la manera para instalarlas todas en un solo comando es `npm install` o la forma corta `npm i`. De este modo, instalarás cada paquete con su respectiva versión indicada en el `package.json`.

Si únicamente tenías el archivo `package.json` después de ejecutar el comando, aparte de instalar todas las dependencias, se generará un archivo package-lock.json y un directorio llamado `node_modules`.

El archivo `package-lock.json` muestra todo el árbol de dependencias de tu proyecto. ¿Qué significa esto? Cada dependencia instalada también tiene sus respectivas dependencias, a estas se las denomina sub-dependencias. El árbol de dependencias muestra todas las sub-dependencias como si de ramas se tratasen.

El directorio `node_modules` contiene todos los archivos ejecutables de Nodejs y los módulos que contiene cada dependencia. Este directorio es ignorado por los repositorios de Git, por eso es importante el archivo `package.json`, ya que te permitirá instalar las dependencias con npm install cuando realices un fork de cualquier repositorio.

8.- Comandos en NPM (Scripts)

El apartado de `"scripts"` en el `package.json` es el que indica los comandos a ejecutar del proyecto. Esta sección es la que utilizarás para crear comandos que optimicen el desarrollo de tu aplicación.

### Cómo crear un comando en tu proyecto

Para crear un comando en tu proyecto, utiliza la siguiente estructura, donde es el nombre del comando que debería ser muy descriptivo y es el comando que utilizarías en la terminal.

```bash
{
    "scripts": {
        "<nombre>": "<comando>"
    }
}
```

Una vez hayas escrito el comando en el archivo `package.json`, la manera de ejecutarlo en la terminal será con el comando `npm run <nombre>`.

### Creemos algunos comandos comunes

Creemos tres comandos comunes: para iniciar el proyecto (start), crear un archivo para producción (build) y combinarlos (deploy). Que no te preocupe si no entiendes cada comando, solo entiende cómo ejecuta `NPM el script`.

```bash
{
    "scripts": {
        "start": "webpack-dev-server --open --mode development",
        "build": "webpack --mode production",
        "deploy": "npm run format && npm run build"
    }
}
```

Y para ejecutarlos, es necesario utilizar el comando respectivo en la terminal:

```bash
Cónsola:

$ npm run start || npm start
$ npm run build || npm build
$ npm run deploy || npm deploy
```

`NPM` provee algunos alias, como `npm start` que ejecuta lo mismo que `npm run start`.

### Cómo ejecutar un paquete de manera directa

`NPM` te permite instalar paquetes en tu proyecto, sin embargo, NPX (Node Package Execute) permite ejecutar un comando de NPM remotamente.

Ejemplos de este comportamiento son los paquetes React y Nextjs, para iniciar un proyecto en estos se puede ejecutar los siguientes comandos, donde es el nombre del proyecto:

```bash
Cónsola:

$ npx create-react-app <nombre>
$ npx create-next-app <nombre>
```

9.- Actualización de dependencias

Conocer cómo actualizar dependencias es muy importante para mantener tus proyectos actualizados y libres de vulnerabilidades de seguridad.

El comando ``npm outdate`` mostrará los paquetes que están desactualizados. Con el comando ``npm outdate --dd`` verás de manera más detallada esta información.

### Cómo actualizar dependencias

Para actualizar todas las dependencias utiliza el siguiente comando:

```bash
Cónsola:

$ npm update
```

Ten en cuenta que actualizar varios paquetes no es recomendable, solamente deberías actualizar un paquete si estás muy seguro de que no afectará al proyecto y que realizaste los cambios pertinentes.

```bash
Cónsola:

$ npm update <paquete>
```

Utiliza el siguiente comando para actualizar a la última versión (latest) de la dependencia, donde es el nombre del paquete.

```bash
Cónsola:

$ npm install <paquete>@latest
```
