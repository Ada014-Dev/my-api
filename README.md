# Personal API

A simple REST API built with Python and Flask, deployed on a Linux VPS with Nginx.

## How to Run Locally

git clone https://github.com/Ada014-Dev/my-api.git
cd my-api
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py

## Endpoints

GET /
{"message": "API is running"}

GET /health
{"message": "healthy"}

GET /me
{"name": "Blessing Uche", "email": "ucheblessing332@gmail.com", "github": "https://github.com/Ada014-Dev"}

## Live URL

http://51.20.117.133
