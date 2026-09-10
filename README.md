# User Authentication System

A simple and secure **User Authentication System** built using **Node.js, Express.js, MongoDB, HTML, CSS, and JavaScript**. The application provides basic user registration and login functionality while securely storing passwords using **bcrypt hashing**.

## Features

* User Registration
* User Login
* Password Hashing using bcrypt
* MongoDB Atlas Integration
* Secure storage of user credentials
* Simple and user-friendly interface

## Technologies Used

* **Node.js** – JavaScript runtime environment
* **Express.js** – Backend web framework
* **MongoDB** – Database for storing user information
* **MongoDB Atlas** – Cloud database service
* **HTML** – Web page structure
* **CSS** – Styling and layout
* **JavaScript** – Application functionality
* **bcrypt** – Password hashing

## How It Works

### User Registration

1. The user enters their registration details.
2. The application receives the submitted information.
3. The password is hashed using bcrypt.
4. The user details are stored in MongoDB.
5. The plain-text password is never stored in the database.

### User Login

1. The user enters their login credentials.
2. The application checks the entered details against the database.
3. bcrypt verifies the entered password against the stored password hash.
4. If the credentials are valid, the user is successfully logged in.

## Password Security

Passwords are protected using **bcrypt hashing** before being stored in MongoDB.

```text
Plain Password
      ↓
  bcrypt Hashing
      ↓
Password Hash
      ↓
    MongoDB
```

This provides better security than storing passwords as plain text.

## Project Structure

```text
user-auth-system/
│
├── public/
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── style.css
│   └── script.js
│
├── server.js
├── package.json
├── package-lock.json
├── .env
├── .gitignore
└── README.md
```

> The project structure may vary depending on the implementation.

## Prerequisites

Make sure the following are installed before running the project:

* Node.js
* npm
* MongoDB Atlas account or local MongoDB

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Shalini-d-13/user-auth-system.git
```

### 2. Navigate to the Project

```bash
cd user-auth-system
```

### 3. Install Dependencies

```bash
npm install
```

## Environment Variables

Create a `.env` file in the root directory and add your MongoDB connection string:

```env
MONGODB_URI=your_mongodb_connection_string
```

Example:

```env
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/database
```

For security, do not upload the `.env` file to GitHub.

Add the following to `.gitignore`:

```text
.env
node_modules/
```

## Running the Project

Start the application using:

```bash
npm start
```

Or, if the application is configured to run directly with Node.js:

```bash
node server.js
```

Open the local URL provided by the server in your browser. For example:

```text
http://localhost:3000
```

## Authentication Flow

```text
        User
         │
         ▼
 ┌─────────────────┐
 │ Register / Login│
 └────────┬────────┘
          │
          ▼
 ┌─────────────────┐
 │ Express Server  │
 └────────┬────────┘
          │
          ▼
 ┌─────────────────┐
 │ bcrypt Password │
 │ Hashing/Checking│
 └────────┬────────┘
          │
          ▼
 ┌─────────────────┐
 │     MongoDB     │
 └─────────────────┘
```

## Security

The application implements basic security practices:

* Passwords are hashed using bcrypt.
* Plain-text passwords are not stored in the database.
* MongoDB credentials are stored using environment variables.
* Sensitive configuration files are excluded from version control.

For a production-ready authentication system, additional security features such as JWT or session-based authentication, input validation, rate limiting, HTTPS, and secure cookies can be implemented.

## Future Enhancements

* JWT-based authentication
* Logout functionality
* Forgot and reset password
* Email verification
* User profile management
* Role-based access control
* Input validation
* Authentication middleware
* Rate limiting
* Responsive UI improvements

## License

This project is intended for **educational and learning purposes**.
