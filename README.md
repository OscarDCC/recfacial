# recfacial
Proyecto de seguridad para chapa eléctrica con un reconocimiento facial integrado

Para el funcionamiento correcto se tiene que crear 3 carpetas dentro de la que contiene el proyecto

-dataset

-trainer

-FacialRecognition

Se debe mover el archivo "trainer.yml" dentro de la carpeta "trainer", mientras que las otras 2 tienen que estar vacías

#------------------------------PASOS---------------------------------------------------------

1.- Entrar en la siguiente liga para la conexion de la camara https://descubrearduino.com/conectar-camara-raspberry-pi/

2.- Instalar open cv con los siguientes comandos:

wget -O opencv.zip https://github.com/opencv/opencv/archive/4.0.0.zip

wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.0.0.zip

unzip opencv.zip

unzip opencv_contrib.zip

sudo apt-get update && sudo apt-get upgrade
sudo apt-get install build-essential cmake pkg-config
sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt-get install libxvidcore-dev libx264-dev
sudo apt-get install libgtk2.0-dev libgtk-3-dev
sudo apt-get install libfontconfig1-dev libcairo2-dev
sudo apt-get install libgdk-pixbuf2.0-dev libpango1.0-dev
sudo apt-get install libhdf5-dev libhdf5-serial-dev libhdf5-103
sudo apt-get install libqtgui4 libqtwebkit4 libqt4-test python3-pyqt5
sudo apt-get install libatlas-base-dev gfortran
sudo apt-get install python2.7-dev python3-dev
sudo apt-get install python3-pil.imagetk

wget https://bootstrap.pypa.io/get-pip.py
sudo python3 get-pip.py
sudo pip3 install numpy

4.- Primero se tendra que hacer la prueba de la camara y de la deteccion del rostro con:

python Test.py

python Detec.py

5.- Para guardar una base de datos de rostros ejecuta:

python save.py

6.- Entrenamos al progarama con:

python Trainer.py

7.- Por ultimo conectamos el circuito de la chapa electrica al puerto 12 de la raspberry y ejecutamos el programa

python RecFacial.py
