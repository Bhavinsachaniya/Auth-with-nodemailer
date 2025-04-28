# Authentication System with JWT and OTP via Nodemailer

This project implements a user authentication system with JWT (JSON Web Tokens) and OTP (One-Time Password) login via email. It is built with Node.js, Express.js, MongoDB, and uses **Nodemailer** to send OTPs for login verification. 

## Features

- **User Authentication**: User sign up and login using JWT tokens.
- **OTP Authentication**: Secure login using OTP sent to the user's email.
- **JWT Token Management**: Tokens are used for managing sessions after successful login.
- **Password Hashing**: Bcrypt.js is used for securely hashing passwords.
  
## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Token)
- **OTP Verification**: Nodemailer (for sending OTPs to users' emails)
- **Password Hashing**: Bcrypt.js
- **Environment Variables**: dotenv for configuration management

## Prerequisites

Make sure you have the following installed before running the project:

- Node.js (v14 or higher)
- npm (v6 or higher)
- MongoDB (local or MongoDB Atlas for cloud)

## Setup Instructions

### 1. Clone the Repository

First, clone the repository:

```bash
git clone https://github.com/yourusername/authentication-jwt-otp.git
cd authentication-jwt-otp
