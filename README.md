# Real-time Chat Application 🚀

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Node.js](https://img.shields.io/badge/Node.js-18.0.0-blue.svg)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-5.0.0-green.svg)](https://www.mongodb.com/)

A real-time chat application built with modern technologies, providing seamless communication and secure user management.

## 📋 Features

- 📱 Real-time messaging with WebSocket
- 🔐 Secure user authentication (JWT)
- 🏠 Multiple chat rooms
- 💾 Persistent message storage
- 📱 RESTful API endpoints
- 🔐 Secure password hashing
- 📱 Cross-platform compatibility

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Real-time**: Socket.IO
- **Authentication**: JWT
- **Security**: bcrypt

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ZBS-1910/Chat-Appliaction.git
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file with the following variables:
```
PORT=3000
MONGODB_URI=mongodb://localhost:27017/chat-app
JWT_SECRET=your-secure-secret-key
```

4. Start MongoDB server

5. Start the application:
```bash
npm start
```

## 📖 API Documentation

### Base URL
All API endpoints are available at: `http://localhost:3000/api`

### Authentication API

#### Register User
- **Endpoint**: POST `/api/auth/register`
- **Request**:
```json
{
    "username": "string",
    "password": "string"
}
```
- **Response**:
```json
{
    "success": true,
    "message": "Registered user Successfully",
    "user": {
        "username": "string",
        "password": "hashed_password"
    },
    "token": "JWT_TOKEN"
}
```
- **Example**:
```bash
curl -X POST http://localhost:3000/api/auth/register \
     -H "Content-Type: application/json" \
     -d '{"username": "john_doe", "password": "password123"}'
```

#### Login User
- **Endpoint**: POST `/api/auth/login`
- **Request**:
```json
{
    "username": "string",
    "password": "string"
}
```
- **Response**:
```json
{
    "success": true,
    "message": "User Login Successfully",
    "token": "JWT_TOKEN"
}
```
- **Example**:
```bash
curl -X POST http://localhost:3000/api/auth/login \
     -H "Content-Type: application/json" \
     -d '{"username": "john_doe", "password": "password123"}'
```

#### Get User Profile
- **Endpoint**: GET `/api/auth/user`

