# React Native

El siguiente tutorial tutorial está pensado para ser usado en Ubuntu 18.04 o 19.10. En particular el tutorial ha sido probado en Ubuntu 19.10.

## Instalación de pre requisitos

Se necesita tener instalado NVM, NodeJS y Yarn, si ya están instalados entonces puedes omitir los siguentes pasos. Por terminal se deben ingresar los siguentes comandos:

- `sudo apt install curl` -> Para instalar curl
- `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash` -> Instala NVM
- `nvm install stable` -> Instala la última versión de NodeJS
- `curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -`
- `echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list`
- `sudo apt-get update && sudo apt-get install yarn` -> Instala yarn

Se puede comprobar que la instalación fue correcta con los comandos

- `nvm --version`
- `node --version`
- `yarn --version`

Donde se debería obtener la versión correspondiente de cada uno al escribir el comando.

## Instalando JDK

Para instalar JDK primero se debe descargar un archivo `tar.gz` con la versión que requieras de jdk

- <https://adoptopenjdk.net/>

Luego abrir una terminal en tu carpeta Descargas o Downloads y ejecutar los siguientes comandos (estos para la version 11.0.6.10 HotSpot):

- ```bash
  tar -xf OpenJDK11U-jdk_x64_linux_hotspot_11.0.6_10.tar.gz
  ```

La carpeta extraída debe moverse a la ruta `/opt/`

- ```bash
  sudo mv jdk-11.0.6+10/ /opt/
  ```

Añadimos la ruta a nuestro `PATH` usando el archivo de configuración de `Bash` que más nos acomode.

- ```bash
  sudo nano ~/.bashrc
  ```

  - ```bash
    export PATH=$PWD/jdk-11.0.6+10/bin:$PATH # Al final del archivo
    ```

- ```bash
  source ~/.bashrc
  ```

Comprobamos que Java se instaló de manera correcta con el comando `java -version`

## Instalando Android Studio

Descargar el android studio del siguente link: <https://developer.android.com/studio/>

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

Links externos:

- <https://medium.com/swlh/react-native-and-android-studio-everything-you-need-to-get-started-in-linux-b47154e78f9e>
- <https://facebook.github.io/react-native/docs/getting-started>
