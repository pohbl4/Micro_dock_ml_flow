# Microservice Architecture Project

This project demonstrates a microservices architecture using Docker, Docker Compose, and RabbitMQ for communication between services.

## Prerequisites

To run this project, you need the following tools installed on your machine:

- Docker
- Docker Compose

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repository-link>
   cd microservice_architecture
   
2. Build and start all containers with Docker Compose:
   ```bash
   docker-compose up --build

3. The RabbitMQ interface will be available at:
   ```bash
   http://localhost:15672

4. Use the following credentials to log in:
   ```bash
   Username: user
   Password: password
   Logs and prediction statistics are collected in the ./logs directory.



How It Works
Microservices
features.py: Handles feature processing tasks received from RabbitMQ queues.

metrics.py: Generates and records metrics in metric_log.csv.

model.py: Uses a pre-trained machine learning model (myfile.pkl) to make predictions. Communicates with other services via RabbitMQ.

plot.py: Creates visualizations based on the recorded metrics.

RabbitMQ
RabbitMQ is used as a message broker for inter-service communication. Each microservice connects to specific RabbitMQ queues to exchange tasks.

Log File
The logs/metric_log.csv file stores data processed by the microservices. Ensure that this file exists in the root directory before starting the project.


