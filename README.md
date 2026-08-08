# Gibberish 

Gibberish is a full-stack real-time chatting application built using the MERN stack. It uses Socket.IO for real-time communication and MongoDB to store user and chat data.

## Tech Stack

### Client

* React.js
* Chakra UI
* Axios
* Socket.IO Client

### Server

* Node.js
* Express.js
* Socket.IO
* JWT Authentication

### Database

* MongoDB
* Mongoose

## Features

* User registration and login
* JWT-based authentication
* Real-time messaging using Socket.IO
* One-to-one chat
* Group chat
* Search users by name or email
* User profile management
* Real-time message notifications
* Responsive chat interface

## Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/DhanushT7/Gibberish.git
```

### 2. Go to the project directory

```bash
cd Gibberish
```

### 3. Install backend dependencies

```bash
npm install
```

### 4. Install frontend dependencies

```bash
cd frontend
npm install
```

### 5. Configure environment variables

Create a `.env` file in the project root:

```env
PORT=5001
MONGO_URI=mongodb://localhost:27017/chatapp
JWT_SECRET=your_jwt_secret
```

Replace `your_jwt_secret` with your own secret key.

### 6. Start the backend

From the project root:

```bash
npm start
```

The backend will run on:

`http://localhost:5001`

### 7. Start the frontend

Open a new terminal:

```bash
cd Gibberish/frontend
npm start
```

The frontend will run on:

`http://localhost:3000`

## Application Flow

```text
React Frontend
      |
      | HTTP Requests
      v
Node.js + Express
      |
      +---- JWT Authentication
      |
      +---- REST APIs
      |
      +---- Socket.IO
                 |
                 v
          Real-time Messages
                 |
                 v
              MongoDB
```

## Security

* Passwords are securely hashed before being stored in MongoDB.
* JWT is used for authentication.
* Protected API routes require a valid JWT token.
* Sensitive configuration is stored using environment variables.

## Notes

Make sure MongoDB is running locally before starting the backend.

Do not commit your `.env` file to GitHub. Add the following to `.gitignore`:

```text
.env
```

