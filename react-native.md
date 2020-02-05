El siguiente tutorial tutorial está pensado para ser usado en Ubuntu 18 o 19. En particular el tutorial ha sido probado en Ubuntu 19.10

## Instalación de pre requisitos

Se necesita tener instalado NVM, NodeJS y Yarn, si ya están instalados entonces puedes omitir los siguentes pasos. Por terminal se deben ingresar los siguentes comandos:

- `sudo apt install curl` -> Para instalar curl
- `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash` -> Instala NVM
-  `nvm install stable` -> Instala la última versión de NodeJS
- `curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -`
- `echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list`
- `sudo apt-get update && sudo apt-get install yarn` -> Instala yarn

Se puede comprobar que la instalación fue correcta con los comandos

- `nvm --version`
- `node --version`
- `yarn --version`
Donde se debería obtener la versión correspondiente de cada uno al escribir el comando.

## Instalando JDK

Para instalar JDK primero se debe descargar el siguente archivo para la versión Linux de 32 o 64 bits según tu computador y que termina en la extensión .deb:

-  https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html

Luego abrir una terminal en tu carpeta Descargas o Downloads y ejecutar el comando(Para este tutorial se instalará la versión 11.06 de JDK):

- `sudo dpkg -i NOMBRE-DEL-ARCHIVO-DESCARGADO`
- `sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-11.0.6/bin/java 2`
- `sudo update-alternatives --config java`
- `sudo nano ~/.profile`
- `sudo source ~/.profile`

Comprobar que Java se instaló de manera correcta con el comando `java --version`

## Instalando Android Studio

Descargar el android studio del siguente link: https://developer.android.com/studio/

Luego ejecutar los siguientes comandos:

- `sudo unzip nombre-zip-descargado /usr/local`
- `/usr/local/android-studio/bin/studio.sh`

Luego en instalación escoger: **_Custom instalation_** y asegurarse de marcar el Android Virtual Device.

## Instalando react native

Se instal ejecutando el comando

- `yarn global add react-native-cli`

## Creando un dispositivo virtual

Primero crear un proyecto:

- `react-native init Proyecto`

Luego abrir este proyecto con Android Studio, y dirigirse a AVD Manager donde se podrá crear un entorno virtual de desarrollo.

Finalmente para correr el proyecto se ejecuta

- `react-native start`
- `react-native run-android`


Tutorial original: https://medium.com/swlh/react-native-and-android-studio-everything-you-need-to-get-started-in-linux-b47154e78f9e
