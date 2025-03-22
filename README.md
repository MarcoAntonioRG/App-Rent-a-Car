# Aplicación Rent a Car

Una aplicación de escritorio para arrendar o alquilar vehículos.

## Como ejecutar

1. Para utilizar la aplicación se debe tener instalado el JDK desde la versión 21 y Maven.

2. Se utiliza una base de datos en MySQL mediante un contenedor, basta con correrlo desde la carpeta raíz mediante `docker-compose up`. La otra alternativa sería utilizar una base de datos local.

3. La base de datos y las tablas necesarias se crean manualmente mediante los comandos en el archivo `ComandosSQL.txt`.

4. Instalar el paquete de la aplicación desde la carpeta raíz con `mvn clean install`.

5. Buscar el archivo `.jar` en la carpeta `target` y ejecutar con:

            java -jar [nombre del archivo.jar]