# Transaction Management System

## Overview
The Transaction Management System is a web application designed for managing financial transactions. Users can register, log in, and perform actions such as deposits and withdrawals. The application provides a user-friendly interface, displays transaction history, and calculates the user's balance. It uses React for the frontend, Node.js with Express for the backend, MongoDB for data storage, and JSON Web Tokens (JWT) for authentication.

---

## Features

### User Registration
- Users can create an account with a username, email, and password.

### User Login
- Secure login using email and password with JWT authentication.

### Transaction Management
- Add, view, and filter transactions.
- Two types of transactions: deposits and withdrawals.

### Balance Calculation
- Displays the user's current balance based on their transaction history.

### Transaction Status Update
- Update transaction statuses (e.g., Pending, Completed, Failed).

### Logout Functionality
- Removes the authentication token to securely log out the user.

---

## Technologies Used

### Frontend
- **React**: For building a dynamic and responsive user interface.
- **React Router**: For managing navigation and routing.
- **Axios**: For making HTTP requests to the backend.
- **Cookies**: For securely managing JWT tokens.

### Backend
- **Node.js**: As the runtime environment.
- **Express.js**: For creating RESTful APIs.
- **MongoDB**: As the database, managed with **Mongoose**.
- **JWT**: For secure user authentication.
- **Bcrypt**: For hashing user passwords.

---

## Getting Started

### Prerequisites
1. Install **Node.js** and **npm**.
2. Set up a MongoDB database (local or cloud).

### Installation

#### 1. Clone the repository
```bash
git clone <repository-url>
cd <repository-name>
```

#### 2. Install backend dependencies
```bash
cd backend
npm install
```

#### 3. Install frontend dependencies
```bash
cd frontend
npm install
```

#### 4. Set up environment variables
Create a `.env` file in the `backend` directory with the following details:
```env
MONGO_URI=<your-mongodb-connection-string>
JWT_SECRET=<your-jwt-secret>
```

#### 5. Run the backend server
```bash
cd backend
node index.js
```

#### 6. Run the frontend application
```bash
cd frontend
npm start
```

---

## API Endpoints

### User Routes
- **POST /api/users/register**: Register a new user.
- **POST /api/users/login**: Log in a user.

### Transaction Routes
- **POST /api/transactions**: Create a new transaction (authentication required).
- **GET /api/transactions**: Retrieve all transactions for the logged-in user (authentication required).
- **PUT /api/transactions/:transaction_id**: Update the status of a transaction (authentication required).

---

## Directory Structure
```
/project-root
├── /backend
│   ├── /models         # Mongoose models for User and Transaction
│   ├── /routes         # Express routes for user and transaction management
│   ├── index.js        # Entry point for the backend server
│   └── .env            # Environment variables
└── /frontend
    ├── /src
    │   ├── /components  # React components for Register, Login, and Transaction pages
    │   ├── App.js       # Main application component
    │   └── index.js     # Entry point for the frontend application
    └── package.json      # Frontend dependencies
```

---

## Troubleshooting

### Common Issues

#### Cannot GET /api/transactions
- Ensure the backend server is running and accessible.
- Verify the user is authenticated before accessing the transactions endpoint.
- Check that the correct API URL is being used in the frontend.

#### JWT Authentication Errors
- Ensure the JWT secret in the `.env` file matches the one used to sign tokens.
- Verify that the token is not expired and correctly stored in cookies.

---

## Conclusion
This project provides a solid foundation for managing financial transactions. It can be extended with features such as:
- Categorizing transactions.
- Adding user roles (e.g., admin, user).
- Generating detailed transaction reports.

Feel free to contribute or adapt the application to suit your needs!

