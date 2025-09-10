# lab-auth-api

A simple authentication API built with Node.js and Express. This project is intended for learning and demonstration purposes, focusing on implementing basic authentication workflows such as user registration, login, and token-based authentication.

## Features

- **User Registration:** New users can sign up with a username and password.
- **User Login:** Existing users can log in with their credentials.
- **Token-Based Authentication:** Uses JWT (JSON Web Tokens) for protected routes.
- **Password Hashing:** Secure password storage using bcrypt.
- **RESTful API Endpoints:** Follows REST principles for all routes.

## Technologies Used

- Node.js
- Express
- MongoDB (via Mongoose)
- JWT (jsonwebtoken)
- bcrypt

## Getting Started

### Prerequisites

- Node.js (v14 or above)
- npm
- MongoDB (local or cloud)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ethanangeles-gab/lab-auth-api.git
   cd lab-auth-api
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory and add:
   ```
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   PORT=3000
   ```

4. **Start the server:**
   ```bash
   npm start
   ```

## API Endpoints

| Method | Endpoint         | Description              | Auth Required |
|--------|------------------|-------------------------|--------------|
| POST   | /signup        | Register a new user     | No           |
| POST   | /login           | User login              | No           |
| GET    | /profile         | Get user profile        | Yes          |

> More endpoints and features can be added as needed.

## Usage Example

### Signup
```http
POST /signup
Content-Type: application/json

{
  "username": "testuser",
  "password": "password123"
}
```

### Login
```http
POST /login
Content-Type: application/json

{
  "username": "testuser",
  "password": "password123"
}
```

### Access protected route
```http
GET /profile
Authorization: Bearer <your_jwt_token>
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for improvements or bug fixes.

## License

This project is licensed under the MIT License.

---

**Author:** [ethanangeles-gab](https://github.com/ethanangeles-gab)
