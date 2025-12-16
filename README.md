# Backend Web Development

A Node.js REST API for user authentication and post management built with Express and MongoDB.

## Overview

This project provides a backend API with user registration/login and post creation/management features. It uses MongoDB for data persistence and bcrypt for secure password handling.

## Tech Stack

- **Runtime**: Node.js (ES Modules)
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose
- **Authentication**: bcrypt for password hashing
- **Environment**: dotenv for configuration
- **Development**: nodemon for auto-reload

## Project Structure

```
backend/src/
├── app.js                 # Express app setup
├── index.js              # Entry point
├── config/
│   ├── constants.js      # App constants
│   └── database.js       # MongoDB connection
├── controllers/
│   ├── user.controller.js    # User logic (register, login, logout)
│   └── post.controller.js    # Post logic (CRUD operations)
├── models/
│   ├── user.model.js     # User schema with bcrypt
│   └── post.model.js     # Post schema
└── routes/
    ├── user.route.js     # User endpoints
    └── post.route.js     # Post endpoints
```

## Installation

```bash
npm install
```

## Environment Setup

Create a `.env` file in the root directory:

```env
MONGODB_URI=your_mongodb_connection_string
PORT=4000
```

## Scripts

- **Start**: `npm start` - Run production server
- **Dev**: `npm run dev` - Run with hot reload (nodemon)

## API Endpoints

### Users (`/api/v1/users`)

- `POST /register` - Register new user
- `POST /login` - Login user
- `POST /logout` - Logout user

### Posts (`/api/v1/posts`)

- `POST /create` - Create new post
- `GET /` - Get all posts
- `GET /:id` - Get post by ID
- `PUT /:id` - Update post
- `DELETE /:id` - Delete post

## Features

✅ User authentication with bcrypt password hashing  
✅ JWT-ready architecture  
✅ Mongoose schema validation  
✅ Error handling middleware  
✅ Async/await support  
✅ MongoDB timestamps (createdAt, updatedAt)

## Author

Carvalho
