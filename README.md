# recfacial
Proyecto de seguridad para chapa eléctrica con un reconocimiento facial integrado

Para el funcionamiento correcto se tiene que crear 3 carpetas dentro de la que contiene el proyecto

-dataset

-trainer

-FacialRecognition

#------------------------------PASOS---------------------------------------------------------

1.- Primero verificar si tienes instalado el opencv con lo siguiente

python

import cv2

cv2. __version__

2.- En caso de tener alguna versión instalada se recomienda volver a instalar el sistema operativo con el software recomendado(Raspberry Pi OS with desktop and recommended software) y continuar con la instalación

3.- En caso de no ser así y no tener ninguna versión instalada de opencv continuar con la instalación

4.- Entrar en la siguiente liga para la conexión de la cámara https://descubrearduino.com/conectar-camara-raspberry-pi/

5.- Instalar open cv con los siguientes comandos:

wget -O opencv.zip https://github.com/opencv/opencv/archive/4.0.0.zip

wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.0.0.zip

unzip opencv.zip

unzip opencv_contrib.zip

sudo apt-get update && sudo apt-get upgrade sudo apt-get install build-essential cmake pkg-config sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng-dev sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev sudo apt-get install libxvidcore-dev libx264-dev sudo apt-get install libgtk2.0-dev libgtk-3-dev sudo apt-get install libfontconfig1-dev libcairo2-dev sudo apt-get install libgdk-pixbuf2.0-dev libpango1.0-dev sudo apt-get install libhdf5-dev libhdf5-serial-dev libhdf5-103 sudo apt-get install libqtgui4 libqtwebkit4 libqt4-test python3-pyqt5 sudo apt-get install libatlas-base-dev gfortran sudo apt-get install python2.7-dev python3-dev sudo apt-get install python3-pil.imagetk

wget https://bootstrap.pypa.io/get-pip.py sudo python3 get-pip.py sudo pip3 install numpy

sudo pip install pillow

Si existe alguna duda sobre el procedimiento de instalación te puedes guiar con el siguiente enlace, con el detalle de que se tiene que comenzar desde el “Paso 3” y seguir paso a paso las indicaciones:

https://ninjatecnologia.com/raspberry-pi/como-hacer-un-proyecto-de-reconocimiento-facial-raspberry-pi/

6.- Primero se tendrá que hacer la prueba de la cámara y de la detección del rostro con:

python Test.py

python Detec.py

7.- Para guardar una base de datos de rostros ejecuta (El primer rostro se tiene que guardar como "0", el segundo como "1" y así sucesivamente):

python save.py

8.- Entrenamos al programa con:

python Trainer.py

9.- Por ultimo conectamos el circuito de la chapa eléctrica al puerto 12 de la raspberry y ejecutamos el programa(Para cambiar el nombre del usuario guardado 
como "0" tienes que modificar en la línea 17 e ingresar el nombre del usuario que desees):

python RecFacial.py

