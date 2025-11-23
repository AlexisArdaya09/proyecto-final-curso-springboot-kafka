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

Servicio encargado de la gestión del catálogo de productos. Proporciona operaciones CRUD para productos y publica eventos relacionados con cambios en el catálogo.

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

## 👤 Autor

**Alexis Ardaya**

## 📄 Licencia

Este proyecto es parte de un curso educativo.

---

⭐ Si este proyecto te resulta útil, considera darle una estrella en GitHub.
