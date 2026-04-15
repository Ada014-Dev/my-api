# Personal API

A simple REST API built with Python (Flask), deployed on an AWS EC2 Ubuntu server with Nginx as a reverse proxy and systemd for process management.

## Project Overview

This project is part of the HNG DevOps Stage 1 task. The goal was to build a minimal REST API, deploy it on a cloud server, configure Nginx to proxy public traffic to the app, and keep the service persistently running without manual restarts.

## How It Was Built

### 1. Server Setup
- Provisioned an Ubuntu EC2 instance on AWS
- Connected via SSH using a .pem key pair

### 2. API Development
- Wrote a Flask API in Python with three endpoints
- Tested locally before deploying

### 3. Deployment
- Created a Python virtual environment and installed dependencies
- Configured systemd to keep the app running persistently
- Installed and configured Nginx as a reverse proxy to forward public traffic on port 80 to the Flask app on port 5000

### 4. Code & Version Control
- Pushed all code to a public GitHub repository

## How to Run Locally

git clone https://github.com/Ada014-Dev/my-api.git
cd my-api
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py

The API will be available at http://localhost:5000

## Endpoints

GET /
Returns: {"message": "API is running"}

GET /health
Returns: {"message": "healthy"}

GET /me
Returns: {"name": "Blessing Uche", "email": "ucheblessing332@gmail.com", "github": "https://github.com/Ada014-Dev"}

All endpoints return Content-Type: application/json and HTTP status 200.

## Live Deployment

Public URL: http://51.20.117.133

Nginx proxies all public traffic on port 80 to the Flask app running on port 5000.
The service is managed by systemd and restarts automatically on failure.
