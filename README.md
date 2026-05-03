# Login Application with MongoDB

A modern login form with Node.js backend and MongoDB database integration.

## Features
- User registration (sign up)
- User login with password validation
- Password encryption with bcryptjs
- MongoDB database integration
- Responsive UI with gradient design
- Show/Hide password toggle
- Real-time error messages

## Prerequisites
- Node.js installed
- MongoDB installed and running (or MongoDB Atlas connection string)
- npm package manager

## Installation

1. **Install MongoDB** (if not already installed)
   - Download from: https://www.mongodb.com/try/download/community
   - Or use MongoDB Atlas (cloud): https://www.mongodb.com/cloud/atlas

2. **Install Node Dependencies**
   ```bash
   npm install
   ```

3. **Configure MongoDB Connection**
   - Edit `.env` file and update `MONGODB_URI`
   - Default: `mongodb://localhost:27017/loginapp`
   - If using MongoDB Atlas, replace with your connection string

## Running the Application

1. **Start MongoDB Service**
   - Windows: MongoDB should auto-start after installation
   - Mac/Linux: `mongod` command in terminal

2. **Start the Server**
   ```bash
   npm start
   ```
   OR for development with auto-reload:
   ```bash
   npm run dev
   ```
   Server runs on: `http://localhost:3000`

3. **Open in Browser**
   - Open `http://localhost:3000/loginform.html` in your browser
   - Or directly use the HTML file

## Usage

### Sign Up
1. Click "Sign up" link
2. Enter email and password (min 6 characters)
3. Click "CREATE ACCOUNT"
4. Account is saved in MongoDB

### Login
1. Enter your email and password
2. Click "SIGN IN"
3. Success message appears if credentials are correct

## API Endpoints

### Login
- **POST** `/api/login`
- Body: `{ "email": "user@example.com", "password": "password123" }`

### Sign Up
- **POST** `/api/signup`
- Body: `{ "email": "user@example.com", "password": "password123" }`

## File Structure
```
april2026/
├── loginform.html     (Frontend)
├── style1.css         (Styling)
├── server.js          (Backend)
├── package.json       (Dependencies)
├── .env               (Configuration)
└── .gitignore         (Git ignore rules)
```

## Troubleshooting

**Error: "Connection error"**
- Make sure MongoDB is running
- Make sure server is running (`npm start`)
- Check if port 3000 is available

**Error: "User not found"**
- Create an account first using Sign Up
- Verify email is correct

**Password doesn't match**
- Passwords must be at least 6 characters
- Password is case-sensitive

