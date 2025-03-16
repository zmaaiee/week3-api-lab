Week 3 API Lab: API Development & Microservices

This project implements a simple RESTful API with user authentication and testing using Postman.

Setup Instructions

1. Clone the Repository
git clone [repository-url]

2. Install Dependencies
cd week3-api-lab
npm install express jsonwebtoken bcryptjs body-parser nodemon

3. Run the Server
node server.js

The server runs on http://localhost:3000.

API Endpoints

1. Register a User
- POST /api/register
- Request Body:
  {
  "username": "testuser",
  "password": "password123"
  }

2. Login
- POST /api/login
- Request Body:
  {
  "username": "testuser",
  "password": "password123"
  }
- Response:
  {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRlc3R1c2VyIiwiaWF0IjoxNzQyMTAwMjU0LCJleHAiOjE3NDIxMDM4NTR9.YDYRIVrq-cPBSp-3KHR_XsFJhkOyoBNY3G1v4BIjWfA"
  } 

3. Access Protected Route
- GET /api/protected
- Authorization: Bearer token from login response.

Testing with Postman

1. Register a user with POST /api/register.
2. Login and receive a JWT token with POST /api/login.
3. Access the protected route with GET /api/protected and the JWT token.

