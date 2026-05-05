# Effective Mobile ToR

## Project Description

This project contains:

- Python backend application
- Nginx reverse proxy
- Docker Compose setup


Architecture:


Client
   ↓
Nginx (port 80)
   ↓
Backend Python app (port 8080)


Backend is available only inside Docker network.

------

## Technologies Used

- Docker
- Docker Compose
- Python 3
- Nginx

------

## How to Run

### 1. Clone repository


git clone https://github.com/Xenon1359/effective-mobile-test.git

cd effective-mobile-test


### 2. Start containers


docker-compose up --build


------

## How to Check

Run:


curl http://localhost


Expected result:


'Hello from Effective Mobile!'


------

## Services

### Backend

- Python HTTP server
- Internal port: 8080
- Not exposed to host

### Nginx

- Reverse proxy
- External port: 80
- Proxies requests to backend
