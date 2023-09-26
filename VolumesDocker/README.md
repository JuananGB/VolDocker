# Volumenes Docker

### 1. Descargar la imagen 'httpd' y comprobar que está en tu equipo:

+ docker pull httpd:2.4 (Con este comando descargamos la imagen de apache)
+ docker images (Con este comando vereficamos si la imagen se ha descargado correctamente).

### 2. Crear un contenedor con el nombre 'dam_web1':

+ docker run -d --name dam_web1 -p 8000:80 httpd:2.4 (Con este comando creamos un contenedor llamado "dam_web1" y lo expondrá en el puerto 8000 de mi máquina virtual).

### 3. Permitir acceso desde el navegador de tu equipo:

+ Accedemos desde el navegador y desde él, visitamos "http://localhost:8000" y vemos si Apache se encuentra en funcionamiento.

### 4. Utilizar bind mount para el directorio 'htdocs':

+ mkdir htdocs (Creamos este directorio para guardar los archivos HTML)

### 5. Montamos el directorio creado en el contenedor Apache: 

+ docker run -d --name dam_web1 -p 8000:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd:2.4

### 6. Crear un archivo HTML de "Hola Mundo":

+ Creo un archivo HTML llamado index.html en el directorio htdocs .

### 7. Comprobar el acceso desde el navegador:

+ Visitamos http://localhost:8000 en el navegador. Debería ver el  "Hola Mundo" que creé.







