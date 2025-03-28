# Microservices with Docker and Docker Compose

This project contains four microservices: **user-service**, **product-service**, **order-service**, and **gateway-service**. Each service is Dockerized using a Dockerfile, and they are orchestrated using Docker Compose. This setup allows for easy deployment and management of the services.

## Services Overview

- **User Service**: Manages user-related operations.
- **Product Service**: Handles product-related operations.
- **Order Service**: Manages order processing.
- **Gateway Service**: Acts as a gateway to route requests to the appropriate microservices.

## Prerequisites

Before proceeding, ensure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)


Each service has its corresponding Dockerfile that sets up the environment, installs dependencies, and runs the service on the respective port.

## 1. Dockerizing the Microservices

Each microservice has a Dockerfile located inside its respective directory:

- **user-service/Dockerfile**
- **product-service/Dockerfile**
- **order-service/Dockerfile**
- **gateway-service/Dockerfile**

These Dockerfiles are set up to:

- Set up a Node.js environment
- Install the necessary dependencies
- Run each service on its respective port (3000 for User Service, 3001 for Product Service, 3002 for Order Service, and 3003 for Gateway Service)

## 2. Build the Docker Images

To build the Docker images for all services, follow these steps:

1. Navigate to the root directory where the `docker-compose.yml` file is located.

2. Run the following command to build the images:

   ```bash
   docker-compose build

This will:Read the docker-compose.yml file
Build the Docker images for each service based on their respective Dockerfiles
Prepare the services for running

## 3. Start the Services Using Docker Compose
   
    docker-compose up

This will start all the services defined in docker-compose.yml. The services will be accessible via the following ports:  
User Service: http://localhost:3000  
Product Service: http://localhost:3001  
Order Service: http://localhost:3002  
Gateway Service: http://localhost:3003  

All services will be running in the background.

## Testing the Endpoints

Once the services are up and running, you can test them using tools like curl, Postman, or a web browser.  
http://localhost:3000/users  
http://localhost:3001/products  
http://localhost:3002/orders  
http://localhost:3003/users  


## Screenshots
Docker-compose output:

![image](https://github.com/user-attachments/assets/a1d9b625-7cdc-49e2-9601-6fb070c3d462)  

Here are some example screenshots of the application running:
User Service Endpoints:

![image](https://github.com/user-attachments/assets/3ecbf48d-10d9-4da2-a385-39f4a4b7d49e)  


Product Service Endpoint

![image-1](https://github.com/user-attachments/assets/52dae3fc-7b4e-4265-9046-3e3f8a940ed0)  


Order Service Endpoint

![image-2](https://github.com/user-attachments/assets/6cac5eba-441f-4f2e-bd44-542556978ea6)  


Gateway Service Routing Request to User Service

![image-3](https://github.com/user-attachments/assets/27413d22-f6f9-40aa-9e3d-ed993e50a143)  








