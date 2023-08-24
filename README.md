# gestion-de-la-configuracion
(Estas instrucciones son para ser ejecutadas en un windows 10 ó 11)

   
2. Debemos clonar el repositorio que aloja el codigo de la aplicacion, para esto tendremos que tener instalado Git.
   
   2.1. Ejecuta en el cmd el comando: git --version, esto debería mostarte la version de Git instalada en tu computador pero, sí
       obtienes un error quiere decir que es necesario que instales Git.
         -Aquí puedes descargarlo: https://git-scm.com/download/win, puedes escoger la version de 64 bit o de 32 bit dependiendo de tu version de windows.
         -Se generará un ejecutable en tu escritorio donde deberás darle click para hacer la respectiva intalacion de Git.
   
   2.2. Para clonar el repositorio debes ejecutar los siguientes comandos en la terminal de VS code:
         - cd Desktop      (Nos situamos en el escritorio)
         - mkdir Proyecto  (Creamos una carpeta en el escritorio con nombre Proyecto)
         - git init        (Inicializamos un repositorio)
         - git clone https://github.com/Juan6410/gestion-de-la-configuracion.git  ( Clonamos el repositorio )
         -  (Este paso solo en caso de que le pidan asociar una cuenta para clonar el repositorio)   git config --global user.email "Su correo Electronico" 
         - cd gestion-de-la-configuracion  (Nos ubicamos en el repositorio clonado)
         - git pull origin Juan_Jose_Cordoba_Marin_Luis_Felipe_Gomez_Giraldo (Jalamos los archivos alojados en el repositorio en la rama especificada)
   
4. Ahora ejecutaremos en la terminal tanto el client como el server, Para hacer estas cosas necesitaremos Node.js y npm, para verificar si se encuentran instalados en tu pc en la terminal puedes poner
   node -v  para Node.js y npm -v para npm si alguno de estos te muestra error deberas instalarlo.
   
   -Puedes instalar Node.js en https://nodejs.org/en/download y escoger la version LTS para windows, despues de esto abre el archivo descargado y completa la instalación.
   -Para la instalación de npm basta con poner el siguiente comando en consola: npm install -g npm
   -Debemos pararnos en la carpeta raiz de la aplicacion en este caso AppDelivery y ejecutar el comando npm install (esto instalará todas librerias y dependencias usadas en el proyecto, las cuales se encuentran en un          archivo llamado package.json)
   
    3.1.  Necesitamos iniciar dos terminales, ya tenemos una que es la que hemos venido ejecuando los pasos anteriores y abriremos una nueva, esto lo podemos hacer con el comando Ctrl + Shift + ñ.
         - En la terminal que ya teniamos abierta estamos ubicados en el repositorio clonado gestion-de-la-configuracion, ahora nos situaremos en la carpeta client que se encuentra dentro de AppDelivery.
         - cd AppDelivery (Nos ubicamos en esa carpeta)
         - cd client (Nos ubicamos en esa carpeta)
         - npm start (Esto inicializa el front-end de la aplicacion,)
         Nota: si te aparece un aviso de alerta de seguridad de windos deberas permiri el acceso

    3.2. En la segunda terminal que abrimos vamos a correr nuestro server, para esto deberemos estar situados en la carpeta server.
         -Por defecto deberiamos estar situados en la carpeta que creamos llamada Proyecto asi que haremos lo siguiente:
         - cd gestion-de-la-configuracion
         - cd AppDelivery
         - cd server
         - npm run dev (Esto inicializa la parte del back-end)

5. Para generar el build del front no ubicamos en la carpeta client dentro de nuestro proyecto y desde la teminal, ejecutamos el comando npm run build. Este comamdo lo encontramos dentro de el archivo package.json que especifica el comando para llevar acabo esta operacion.
