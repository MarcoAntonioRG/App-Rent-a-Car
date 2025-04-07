# 🚘 **Aplicación Rent a Car**

Una aplicación de escritorio para arrendar o alquilar vehículos.

## **Tecnologías Usadas**
- Java para la creación de la aplicación
- Maven para la construcción del proyecto
- MySQL para la base de datos
- Docker para la contenerización de la base de datos

## **Requisitos Técnicos**

Para ejecutar la aplicación son necesarios tener instalados los siguientes requisitos en tu máquina local:

- JDK 21 para ejecutar y visualizar la GUI de la aplicación.
- Docker para la ejecución de la base de datos que se utilizará.

## **Descripción**

Esta aplicación permite ingresar a ésta mediante un login donde se introduzen las credenciales que se encuentren almacenadas en la tabla `admin` de la base de datos, para luego mostrar la interfaz gráfica en donde se podrá seleccionar la ventana para arrendar vehículos que se encuentren disponibles rellenando todos los datos necesarios, y una ventana para cuando el cliente quiera devolver el vehículo prestado.

## **Pasos para ejecutar**

1. **Clonar el repositorio** del proyecto en tu máquina local:
   ```bash
   git clone https://github.com/MarcoAntonioRG/App-Rent-a-Car.git
   cd App-Rent-a-Car

2. **Construir y desplegar el contenedor con Docker Compose**:
   ```bash
   docker-compose up -d

3. **Verifica que los contenedores estén corriendo**
   ```bash
   docker ps
   
4. **Accede al servicio de la base de datos con**:
   ```bash
   docker exec -it mysql-db sh
   mysql -u root -proot
   
5. **Copia y pega los comandos** para crear la base de datos `apprentacar_db` y crear e insertar valores en las tablas `admin`, `vehículo`, y para crear la tabla `cliente`. Estos comandos se encuentran en el archivo `ComandosSQL.txt`.

7. **Instalar el paquete de la aplicación desde la carpeta raíz con**:
   ```bash
   exit
   exit
   mvn clean install

9. **Buscar el archivo `.jar` que se crea automáticamente en la carpeta `target` y ejecutar**:
   ```bash
   cd target
   java -jar apprentacar-1.0.jar
