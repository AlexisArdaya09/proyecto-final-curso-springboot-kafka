# Proyecto Final - Curso Spring Boot Kafka

Proyecto final del curso de Spring Boot y Kafka que implementa una arquitectura de microservicios para un sistema de gestión de pedidos, productos e inventario.

## 📋 Descripción

Este proyecto consiste en una arquitectura de microservicios distribuida que utiliza Apache Kafka como sistema de mensajería para la comunicación asíncrona entre servicios. El sistema permite gestionar productos, inventario y pedidos de manera desacoplada y escalable.

## 🏗️ Arquitectura

El proyecto está compuesto por tres microservicios principales que se comunican mediante eventos a través de Apache Kafka:

- **Product Service**: Gestiona el catálogo de productos
- **Order Service**: Maneja la creación y gestión de pedidos
- **Inventory Service**: Controla el inventario y disponibilidad de productos

## 🔗 Microservicios

### 1. Product Service
**Repositorio**: [final-project-product-service](https://github.com/AlexisArdaya09/final-project-product-service)

Servicio encargado de la gestión del catálogo de productos. Proporciona operaciones CRUD para productos y categorías, y publica eventos relacionados con cambios en el catálogo.

### 2. Order Service
**Repositorio**: [final-project-order-service](https://github.com/AlexisArdaya09/final-project-order-service)

Servicio que gestiona el ciclo de vida de los pedidos. Crea pedidos, valida disponibilidad de productos y coordina con otros servicios mediante eventos de Kafka.

### 3. Inventory Service
**Repositorio**: [final-project-inventory-service](https://github.com/AlexisArdaya09/final-project-inventory-service)

Servicio responsable del control de inventario. Gestiona el stock de productos, actualiza disponibilidad.

## 🛠️ Stack Tecnológico

- **Java** - Lenguaje de programación
- **Spring Boot** - Framework de desarrollo
- **Apache Kafka** - Sistema de mensajería y streaming
- **Spring Cloud** - Herramientas para microservicios (opcional)
- **Maven/Gradle** - Gestión de dependencias
- **Docker** - Containerización (opcional)

## 📦 Prerrequisitos

Antes de comenzar, asegúrate de tener instalado:

- Java 17.0.9
- Maven 3.9.11
- IDE: IntelliJ IDEA Ultimate
- Git
- Docker Desktop

## 🚀 Inicio del Proyecto

Sigue estos pasos para configurar y ejecutar el proyecto correctamente:

### 1. Levantar Infraestructura con Docker Compose

Desde este repositorio principal, ejecuta Docker Compose para levantar PostgreSQL y Kafka:

```bash
docker-compose up -d
```

Esto iniciará:
- **PostgreSQL**: Base de datos para los microservicios
- **Apache Kafka**: Sistema de mensajería para comunicación entre servicios

### 2. Crear las Bases de Datos

Una vez que los contenedores estén en ejecución, crea las bases de datos necesarias:

```sql
-- Conectarse a PostgreSQL (puedes usar pgAdmin, DBeaver o psql)
-- O ejecutar desde el contenedor de PostgreSQL

-- Base de datos para Product Service
CREATE DATABASE ecommerce;

-- Base de datos para Order Service
CREATE DATABASE ecommerce_orders;

-- Base de datos para Inventory Service
CREATE DATABASE ecommerce_inventory;
```

**Nota**: Puedes ejecutar estos comandos SQL desde tu cliente de PostgreSQL preferido o desde el contenedor:

```bash
docker exec -it <nombre_contenedor_postgres> psql -U <usuario> -c "CREATE DATABASE ecommerce;"
docker exec -it <nombre_contenedor_postgres> psql -U <usuario> -c "CREATE DATABASE ecommerce_orders;"
docker exec -it <nombre_contenedor_postgres> psql -U <usuario> -c "CREATE DATABASE ecommerce_inventory;"
```

O tambien puedes hacerlo desde  IDE: IntelliJ IDEA Ultimate, sigue los siguientes pasos:

- En la parte derecha ubica el icono de las bases de datos
   ![img.jpg](screenshots/icono-db.jpg)

- Luego click en query console
    ![img.jpg](screenshots/query-console.jpg)

- Ejecuta los siguientes comandos para crear las bases de datos
```sql
-- Conectarse a PostgreSQL (puedes usar pgAdmin, DBeaver o psql)
-- O ejecutar desde el contenedor de PostgreSQL

-- Base de datos para Product Service
CREATE DATABASE ecommerce;

-- Base de datos para Order Service
CREATE DATABASE ecommerce_orders;

-- Base de datos para Inventory Service
CREATE DATABASE ecommerce_inventory;
```
### 3. Ejecutar los Microservicios

Para poder levantar correctamente los microservicios, iniciaremos con **Product Service** y luego seguiremos con los demás servicios en orden. Cada microservicio tiene su propio README con instrucciones detalladas.

#### 3.1. Product Service

- Ve al repositorio de [Product Service](https://github.com/AlexisArdaya09/final-project-product-service)
- Allí encontrarás las instrucciones específicas para levantar el servicio
- Sigue los pasos indicados en su README

#### 3.2. Inventory Service

- Ve al repositorio de [Inventory Service](https://github.com/AlexisArdaya09/final-project-inventory-service)
- Allí encontrarás las instrucciones específicas para levantar el servicio
- Sigue los pasos indicados en su README

#### 3.3. Order Service

- Ve al repositorio de [Order Service](https://github.com/AlexisArdaya09/final-project-order-service)
- Allí encontrarás las instrucciones específicas para levantar el servicio
- Sigue los pasos indicados en su README

## 👤 Autor

**Alexis Ardaya**

## 📄 Licencia

Este proyecto es parte de un curso educativo.
