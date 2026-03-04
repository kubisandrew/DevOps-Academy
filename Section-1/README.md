# Section 1 – Dockerized Flask Application

## Description
This section contains a simple Flask web application packaged into a Docker image and managed using docker-compose.

## Architecture
User → Nginx (optional) → Flask App (Docker container)

The Flask application runs on port 5000 inside the container.
The host maps port 8000 to 5000.

## How to run

docker compose up --build

Open:
http://localhost:8000

## Notes
- The app runs on 0.0.0.0 to allow external access from Docker.
- Ports are mapped from host 8000 to container 5000.
