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
