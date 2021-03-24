# Notas personales

##### Compresor de imagenes
```
http://compressor.io
```

##### Crear logotipos
```
http://crello.com
```

#### Encontrar imagenes en HD
```
http://unsplash.com
```

#### Combinacion de colores para proyectos
```
http://colorhunt.co
```

#### Api de localizacion 
```
http://ip-api.com/json
```

#### Api de PREFIJOS DE TELÉFONOS POR PAÍSES, código, bandera, y abrev 
```
https://restcountries.eu/ 
```



##### watcher
```
sudo sysctl -w fs.inotify.max_user_watches=100000
```

##### Nodemailer Production
```
https://accounts.google.com/b/0/displayunlockcaptcha
https://www.google.com/settings/security/lesssecureapps
https://g.co/allowaccess
```


# Instalaciones

##### Instalar nodejs y npm
```
curl -sL https://deb.nodesource.com/setup_[version].x | sudo -E bash -
sudo apt install nodejs
```

##### Instalar nvm
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
```

##### Instalar android studio
```
sudo apt-get install default-jre
sudo apt-get install android-tools-adb adb android-tools-fastboot fastboot
(sudo unzip ~/Downloads/android-studio-ide-173.4720617-linux.zip -d /opt
||
sudo tar -xvzf ~/Downloads/android-studio-ide-183.5452501-linux.tar.gz -C /opt)
cd /opt/android-studio/bin
./studio.sh
```

##### Instalar Docker

```
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get install docker-ce
sudo systemctl enable docker
whoami # Saber el nombre de tu usuario
sudo usermod -aG docker nombre_de_salida_en_whoami
docker run hello-world

sudo chmod 666 /var/run/docker.sock
```

##### Instalar Postgresql
```
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo apt install pgadmin3
sudo -u postgres psql
ALTER USER postgres PASSWORD 'password';
```

##### Instalar MySql
```
sudo apt update
sudo apt install mysql-server
sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
LUSH PRIVILEGES;
sudo apt install mysql-workbench
```

##### Config React Native 
```
- AVD config not permission
  sudo chown <username> /dev/kvm
  sudo chmod o+x /dev/kvm
- SDK Manager/Android SDK/SDK Tools
  Android SDK Build-Tools [30]
  Android Emulator
  Android SDK Platform-Tools
  Google Play APK Expansion Library
  Google Play Licensing Library
  
- Generar apk
  Cambiar nombre
  android/app/src/main/res/values/

  Iconos
  android/app/src/main/res/

  https://makeappicon.com/​

  http://romannurik.github.io/AndroidAs...​

  Construir APK
  1. keytool -genkey -v -keystore your_key_name.keystore -alias your_key_alias -keyalg RSA -keysize 2048 -validity 10000

  2. copiar el archivo generado (your_key_name.keystore) a la carpeta /android/app 

  3. Abrir el archivo /android/gradle.properties y agregar las siguientes lineas de codigo
  MYAPP_UPLOAD_STORE_FILE=my-upload-key.keystore
  MYAPP_UPLOAD_KEY_ALIAS=my-key-alias
  MYAPP_UPLOAD_STORE_PASSWORD=*****
  MYAPP_UPLOAD_KEY_PASSWORD=*****

  4. Abrir el archivo android\app\build.gradle 
  signingConfigs {
      release {
        storeFile file('your_key_name.keystore')
        storePassword 'your_key_store_password'
        keyAlias 'your_key_alias'
        keyPassword 'your_key_file_alias_password'
      }
  }

  buildTypes {
      release {
        ....
        signingConfig signingConfigs.release
      }
  }

  5. Entramos a la carpeta /android
  cd android

  6. Ejecutamos el comando para crear el apk
  ./gradlew assembleDebug

  7. Nuestra apk queda en el directorio
  /android/app/build/outputs/apk/debug/
```



##### Config Java
```
- update alternatives --config java
- sudo update-alternatives --install /usr/bin/java java /opt/java/[jdk_version]/bin/java 110
- variables de entorno 
   .bashrc /etc/profile
    - export JAVA_HOME=/opt/java/jdk1.8.0_212
    - export PATH=$PATH:$JAVA_HOME/bin




