# Dockerized Python Microservice

## Project Description

This project contains:

- Python backend application
- Nginx reverse proxy
- Docker Compose setup

Architecture:

```text
Client
   ↓
Nginx (port 80)
   ↓
Backend Python app (port 8080)
```

Backend is available only inside Docker network.

---

## Technologies Used

- Docker
- Docker Compose
- Python 3
- Nginx

---

## Requirements

Before running the project, make sure the following tools are installed:

- Docker
- Docker Compose V2

Check installation:

```bash
docker --version
docker compose version
```

Docker Engine installation guide on Linux (terminal only):
https://docs.docker.com/engine/install/

Docker installation guide on Windows, Linux, MacOS:
https://docs.docker.com/get-docker/

## How to Run

### 1. Clone repository

```bash
git clone https://github.com/Xenon1359/dockerized-python-microservice
cd dockerized-python-microservice
```

### 2. Start containers

```bash
docker-compose up --build
```

or

```bash
docker compose up --build
```

---

## How to Check

Open another terminal.

Run:

```bash
curl http://localhost
```

Expected result:

```text
Powered by Docker and poor life choices...
```

---

## Services

### Backend

- Python HTTP server
- Internal port: 8080
- Not exposed to host

### Nginx

- Reverse proxy
- External port: 80
- Proxies requests to backend
