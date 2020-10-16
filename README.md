# devcircle2020

# Tutorial paso a paso sobre como crear un sitio web dinámico utilizando Docusaurus versión 1.14.6 
![Docusaurus_logo](https://docusaurus.io/img/docusaurus_keytar.svg)

*  ## _Preparar el entorno de trabajo._

1. Verificar que tienes **Node** instalado en tu equipo de trabajo. Si no lo tienes instalado, puedes descargarlo del sitio web de [Nodejs](https://nodejs.org/en/download/). Una vez en el sitio, asegurate de obtener una versión superior a la **10.9**
2. Verificar que tienes **Yarn** instalado en tu equipo de trabajo. Si no lo tienes instalado, puedes descargarlo del sitio web de [Yarn](https://classic.yarnpkg.com/en/docs/install/#windows-stable). Una vez en el sitio, asegurate de seleccionar la versión de tu sistema operativo. Para este tutorial estaremos trabjando con Windows 10, por lo que vamos a descargar el instalador contenido en un **.msi**
3. Verifica que tienes **Gitbash** instalado en tu equipo de trabajo. Si no lo tienes instalado, puedes descargarlo del sitio web de [Gitbash](https://gitforwindows.org/). En nuestro caso, estaremos usando windows 10.

***


*  ## _Instalación de Docusaurus._
1. Ejecutamos consola de **Gitbash** y procedemos a crear un directorio con el comando **mkdir** y **ELEGIR_NOMBRE_DEL_DIRECTORIO**

![prueba](https://github.com/dochavez/devcircle2020/blob/main/creacion%20de%20carpeta.jpg)

2. Una vez que se creo el directorio, ejecutamos la instrucción **yarn global add docusaurus-init** , también se puede escoger la opción **npm install --global docusaurus-init**

![Ejecucion de comando](https://github.com/dochavez/devcircle2020/blob/main/ejecucion%20de%20docusaurus.jpg)

3. El resultado de la ejecución anterior nos creará dos carpetas. Una que lleva el nombre de **docs** y otra que se llama **website**.

![Resultado de Instalacion](https://github.com/dochavez/devcircle2020/blob/main/resultado%20de%20instalacion.jpg)

4. Después de que se descarguen e instalen las dependencias, nos hubicamos dentro de la carpeta que lleva por nombre **website** mediante la instruccion **cd website**. Una vez dentro de la carpte ejecutamos el comando **docusaurus-init**  para terminar de instalar las dependencias.

![Despliegue](https://github.com/dochavez/devcircle2020/blob/main/despliegue%20de%20docusaurus.jpg)

5. Finalmente, ejecutaremos el comando **npm start** para correr docusaurus en el navegador. Se desplegara una ventana con la plantilla que trae por defecto, ejecutándose en la dirección web **localhost:3000** de nuestro navegador.

**NOTA:** Para obtener más informacion, puedes ingresar al sitio oficial de docusaurus que lo encontraras en el siguiente enlace: https://docusaurus.io/docs/en/installation

![despliegue en navegador](https://github.com/dochavez/devcircle2020/blob/main/despliegue%20en%20navegador.jpg)
***



*  ## _Comprendiendo la Estructura de nuestro sitio._

1. El archivo **footer.js** que se encuentra en la ruta **website/core/Footer.js** es la parte final de nuestra página principal. El archivo puede ser editado por el usuario.
2. El archivo **siteConfig.js** que se encuentra en la ruta **website/siteConfig.js** contiene las principales configuraciones que utiliza Docusaurus en nuestro sitio web.
3. El archivo **sidebars.json** que se encuentra dentro la carpeta **website** (ubicado en la raíz de la misma), contiene el orden en que se presentan nuestros archivos dentro del sitio web.
4. El archivo **index.js** que se encuentra en la ruta **website/pages/en** es el principal archivo donde se invocan todas las clases definidas. Este archivo es el que busca por defecto el buscador web para desplegar la página principal que se le presenta al usuario.
5. El archivo **main.css** que se encuentra en la ruta **website/node_modules/docusaurus/lib/static/css** es el principal archivo que contiene las hojas de estilo para nuestro sitio web. 
6. En la carpeta **img** que se encuentra en la ruta **website/static/img** es donde se almacenan todas nuestras imagenes que vamos a utilizar para nuestro sitio web.

**NOTA:** Para obtener más informacion sobre esta sección, puedes ingresar al sitio oficial de docusaurus que lo encontraras en el siguiente enlace: https://docusaurus.io/docs/en/site-preparation

***


*  ## Reemplazando líneas de códigos.
1. En el archivo **siteConfig.js** agrega un titulo a tu sitio web o reemplaza el titulo que presenta por defecto la plantilla de Docusaurus. Esto lo encontraras con la directiva que lleva por nombre **`title`** abajo de **`const siteConfig = {...}`**

![siteConfig](https://github.com/dochavez/devcircle2020/blob/main/sideConfig.jpg)

2. En el mismo archivo, ubicate en la seccion **`copyright: `Copyright © ${new Date().getFullYear()} PONER EL NOMBRE DEL DESARROLLADOR`**, para que aparezca en la parte del **footer** de tu pagina web.
3. En el archivo **index.js** identifica la seccion **`const LearnHow = () => (`**, luego ubica la etiqueta **`image: `${baseUrl}img/PONER TU NOMBRE DE LA IMAGEN AQUI`**. Por ejemplo, sería **`image: `${baseUrl}img/variedad_maiz.jpg`**
4. Repite el paso anterior para el caso para la sección **`const Features = () => (`**, **`const Description = () => (`**.
5. Siempre en el mismo archivo, debajo de la etiqueta **`content`**, agrega cualquier contenido que sirva como descripcion. Este contenido se ubicara a la par de la imagen que agregues. Recuerda que esas imagenes deben de estar dentro de la carpeta que ubicada en **website/static/img**
6. Ubicate dentro del archivo que se llama **footer.js**. 
7. Vamos agregar un poco de contenido para alimentar nuestro sitio web con información. Para eso pondremos un poco de información relacionada al Maíz y el Trigo. Para eso, deberas agregar el siguiente código tal como aparece en la imagen. El código fuente va debajo de **`conts FeatureCallout`**

![Contenido](https://github.com/dochavez/devcircle2020/blob/main/Contenido.jpg)

8. **RECUERDA**: **`<h5></h5>`** se usa para los titulos y subtitulos, **`<a href="">`** sirve para agregar la direccion web donde nos redirige nuestro enlace, **`target=_blank`** se usa para que la informacion de nuestro enlace se abra en una nueva pestaña
9. Puedes agregar un banner al footer, debajo de los `<DIV>` que ya tienes colocado. Para eso, deberas de colocar una imagen. Tu archivo final debe de parecerse a esta manera.

![Final Footer](https://github.com/dochavez/devcircle2020/blob/main/Final_Footer.jpg)

***
*  ## Pasando de localhost a github para publicar tu sitio en internet.
1. En la terminal de Github ejecuta el comando **`yarn build`**. Este comando creara una carpeta que lleva por nombre **build**. Basicamente es la que contiene todo tu sitio web.
2. Una vez ejecutado el comando, verifica que tienes el directorio creado dento de **website**.

![de local host a github](https://github.com/dochavez/devcircle2020/blob/main/publicacion.jpg)

3.Finalmente, deberas ejecutar la siguiente instruccion en la misma terminal: **GIT_USER=USERNAME CURRENT_BRANCH=master USE_SSH=true npm run publish-gh-pages** en caso que vayas acceder usando **SSH** o puede usar **GIT_USER=USERNAME CURRENT_BRANCH=master npm run publish-gh-pages** si quieres usar el protocolo **HTTPS**.
4. Toma en cuenta que la palabra **USERNAME** debera de ser reemplazada por el usuario que usas para ingresar a tu cuenta de **github**.
