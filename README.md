# CST8915 Lab 5 – Containerizing the Algonquin Pet Store with Docker

**Student:** Kaveh Kheir Abadi  
**Course:** CST8915 – Full-stack Cloud-native Development  
**Semester:** Fall 2026

## Project Overview

In this lab, I containerized the Algonquin Pet Store application using Docker and Docker Compose.

The application consists of four services:

1. **Store Front:** Vue.js application served by Nginx.
2. **Order Service:** Node.js API for processing orders.
3. **Product Service:** Python Flask API for retrieving products.
4. **RabbitMQ:** Message broker for handling order messages.

## GitHub Service Repositories

- Order Service: https://github.com/kaveh-kheir-abadi/order-service-L4
- Product Service (Python): https://github.com/kaveh-kheir-abadi/product-service-python-L4
- Product Service (Rust): https://github.com/kaveh-kheir-abadi/product-service-rust-L4
- Store Front: https://github.com/kaveh-kheir-abadi/store-front-L4

## Docker Hub Images

- Order Service: https://hub.docker.com/r/kavehkhe/order-service
- Product Service: https://hub.docker.com/r/kavehkhe/product-service
- Store Front: https://hub.docker.com/r/kavehkhe/store-front

## Running the Application

1. Clone this submission repository.
2. Copy `.env.example` to `.env`.
3. Update the environment variables in `.env`.
4. Pull the Docker images:

   ```bash
   docker compose -f docker-compose.images.yaml pull
   ```

5. Start the application:

   ```bash
   docker compose -f docker-compose.images.yaml up -d --wait
   ```

6. Open the Store Front at http://localhost:8080.

## Testing

The following functionality was tested successfully:

- Docker images built successfully.
- All four services started using Docker Compose.
- Product Service returned the product list.
- Store Front displayed the products.
- Orders were submitted successfully.
- RabbitMQ received order messages.
- Images were pushed to Docker Hub.
- Image-only deployment was tested.

## Demo Video

**Video link:** To be added after recording.

## Conclusion

This lab demonstrated how Docker and Docker Compose simplify deploying a multi-service application. I also learned how to publish Docker images to Docker Hub and deploy the application using prebuilt images without rebuilding the source code.