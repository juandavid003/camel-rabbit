# camel-rabbit-lab

Integración de Apache Camel con RabbitMQ  
*Ejemplo práctico de mensajería asincrónica con Java, Spring Boot, Camel y RabbitMQ.*

## Objetivo

Demostrar el **desacoplamiento** entre productores y consumidores usando el patrón de mensajería asincrónica.  
Productores y consumidores se comunican mediante RabbitMQ usando Apache Camel.

---

## Requisitos Previos

- **Java 11+**  
- **Maven**  
- **Docker** (para levantar RabbitMQ rápidamente)  
- **Git** (opcional, para clonar el repo)

---

## 1. Levantar RabbitMQ con Docker

1. Descarga la imagen oficial:
    ```bash
    docker pull rabbitmq:3-management
    ```

2. Inicia el contenedor:
    ```bash
    docker run -d --hostname my-rabbit --name rabbitmq \
      -p 5672:5672 -p 15672:15672 rabbitmq:3-management
    ```

3. Accede a la consola web en [http://localhost:15672](http://localhost:15672)  
   - Usuario: `guest`  
   - Contraseña: `guest`  

---

## 2. Crear la Cola en RabbitMQ

1. Ingresa a la consola web.
2. Ve al menú **Queues**.
3. Crea una nueva cola llamada:  test.camel.queue
(Deja las opciones por defecto.)

---

## 3. Configurar y Ejecutar el Proyecto Camel

mvn clean package
mvn spring-boot:run


