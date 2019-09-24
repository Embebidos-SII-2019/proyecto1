Instituto Tecnologico de Costa Rica
CE-5303 Introducción a los Sistemas Embebidos
II Sem 2019

Ellioth Ramirez Trejos /2014057732
Cristian Roberto Castillo Mcquiddy / 2014061245

Depedencias
  #Distribucion de linux armado con yocto, para arm
  #gcc version 7.4.0
  #fswebcam
  #tener make en el computador que se hace la cross compilación.
 
Instalacion y ejecución
    Comandos para crosscompilar
    Establecer el ambiente
          #$ . /opt/poky/2.7.1/environment-setup-cortexa7t2hf-neon-vfpv4-poky-linux-gnueabi 
          
     #En la carpeta root del proyecto, hacer click derecho y escoger, arbir en terminal
     #ejecutar el comando  
          #$ make install
          
    Y en la carpeta usr ya tenemos los compilados que queremos para la rasp
    Ahora es necesario mover la carpeta bin dentro de la sd, la cual ya debe de tener la 
    imagen instalada,
    Dentro de la carpeta root, vamos a ejecutar el comando 
        #$ sudo cp -r * /media/myUser/idDeSd/
        
    Se desmonta la tarjeta de la computadora, se monta en la rasp, se enciende, una vez que haya terminado de cargar, 
    llegó a la terminal, va a pedir el usuario, se escribe el nombre 
        #$ root 

    deja pasar y se escribe el comando
        #$ cd /

    Esto va a hacer que el vaya a la carpeta root de la rasp, ahora se escribe el siguiente comando,
        #$ ./bin/ExeName

    En donde dice ExeName debe ser igual al que establecimos en el Makefile.am de la carpeta src.

    Cuando se usa una tercera biblioteca externa, es mejor, que al momento de llamarla, se copien 
    los archivos de las carpetas lib y src y sean copiadas en la carpeta principal luego se compila.
