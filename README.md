# Authentication System with JWT and OTP via Nodemailer

This project implements a user authentication system with JWT (JSON Web Tokens) and OTP (One-Time Password) login via email. It is built with **Node.js**, **Express.js**, **MongoDB**, and uses **Nodemailer** to send OTPs for login verification.

---

## ✨ Features

- **User Authentication**: User signup and login using JWT tokens.
- **OTP Authentication**: Secure login using OTP sent to user's email.
- **JWT Token Management**: Tokens are used to manage sessions after successful login.
- **Password Hashing**: Bcrypt.js is used for securely hashing passwords.
- **Secure OTP Expiry**: OTPs expire after 10 minutes for security.
  
---

## 🛠 Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Token)
- **OTP Verification**: Nodemailer
- **Password Hashing**: Bcrypt.js
- **Environment Variables**: dotenv

---

## 🚀 Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)
- MongoDB (local setup or MongoDB Atlas)

---

## 🛠 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Bhavinsachaniya/Auth-with-nodemailer.git
```

---

### 2. Backend Setup

#### Install Dependencies

```bash
npm install
```

---

#### Create a `.env` File

Create a `.env` file at the root of your project and add the following:

```env
JWT_SECRET=your_jwt_secret_key
MONGO_URI=your_mongodb_connection_string
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
```

> **Note:**
> - **JWT_SECRET** → Secret key for signing JWT tokens.
> - **MONGO_URI** → MongoDB connection URI.
> - **EMAIL_USER** and **EMAIL_PASS** → Your email credentials for sending OTPs.

---

#### Setting Up Nodemailer with Gmail (Optional)

If you use Gmail:

```env
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_gmail_app_password
```

⚡ **Important**:  
If you're using Gmail, enable "Less Secure App Access" or create an App Password if 2FA is enabled.

---

### 3. MongoDB Setup

#### Local MongoDB:

Make sure MongoDB is installed and running locally.

```bash
mongod
```

#### MongoDB Atlas:

Use a connection string like this:

```env
MONGO_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/<database-name>
```

---

### 4. Start the Backend Server

```bash
npm start
```

The server will start at:

```bash
http://localhost:5000
```

---

## 📡 API Endpoints

### 1. **Sign Up**

- **Method**: POST
- **Endpoint**: `/api/auth/signup`

**Request Body:**

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

**Response:**

```json
{
  "token": "<JWT_Token>",
  "user": {
    "id": "<User_ID>",
    "name": "John Doe",
    "email": "john@example.com"
  }
}
```

---

### 2. **Login**

- **Method**: POST
- **Endpoint**: `/api/auth/login`

**Request Body:**

```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

**Response:**

```json
{
  "token": "<JWT_Token>",
  "user": {
    "id": "<User_ID>",
    "name": "John Doe",
    "email": "john@example.com"
  }
}
```

---

### 3. **Send OTP for Login**

- **Method**: POST
- **Endpoint**: `/api/auth/send-otp`

**Request Body:**

```json
{
  "email": "john@example.com"
}
```

**Response:**

```json
{
  "message": "OTP sent to your email"
}
```

---

### 4. **Verify OTP and Login**

- **Method**: POST
- **Endpoint**: `/api/auth/verify-otp`

**Request Body:**

```json
{
  "email": "john@example.com",
  "otp": "123456"
}
```

**Response:**

```json
{
  "token": "<JWT_Token>",
  "user": {
    "id": "<User_ID>",
    "name": "John Doe",
    "email": "john@example.com"
  }
}
```

---

## 🧪 Testing the API Using Postman

You can test the APIs with Postman:

1. **Sign Up**: `POST /api/auth/signup`
2. **Login**: `POST /api/auth/login`
3. **Send OTP**: `POST /api/auth/send-otp`
4. **Verify OTP**: `POST /api/auth/verify-otp`

> ✅ Always set the body type to `raw` → `JSON` when sending requests!

---

## ⚡ Conclusion

This project offers a secure, scalable user authentication system with OTP email verification and JWT tokens for session management.  

Perfect for integrating into bigger SaaS projects, e-commerce systems, and more! 🚀

---

## 🧡 If you find this useful, don't forget to leave a ⭐ on GitHub!

---
