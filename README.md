# Job Portal Application

This project is a job portal application built with Node.js, Express, MongoDB, React, and JWT authentication. It allows users to sign up, log in, and access job listings. Additionally, it implements an OTP (One-Time Password) login system via email for enhanced security.

## Features

- **User Authentication**: Sign up, login, and secure session handling with JWT tokens.
- **OTP Login**: Secure login using OTP sent to the user's email.
- **Job Listings**: Users can view job listings (admin or user roles can be added for job posting).
- **Responsive UI**: Built with React to provide a smooth user experience on both desktop and mobile.

## Tech Stack

- **Frontend**: React.js
- **Backend**: Node.js with Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Token)
- **OTP Verification**: Nodemailer (for sending OTP emails)
- **Password Hashing**: Bcrypt.js
- **Environment Variables**: dotenv for configuration

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v14 or higher)
- npm (v6 or higher)
- MongoDB (local setup or MongoDB Atlas)

## Setup Instructions

### Backend Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/job-portal.git
    cd job-portal
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Create a `.env` file in the root of the project and add the following environment variables:
    ```bash
    JWT_SECRET=your_jwt_secret_key
    MONGO_URI=your_mongodb_connection_string
    EMAIL_USER=your_email@example.com
    EMAIL_PASS=your_email_password
    ```

4. Start the backend server:
    ```bash
    npm start
    ```

### Frontend Setup

1. Navigate to the frontend directory:
    ```bash
    cd client
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Start the React development server:
    ```bash
    npm start
    ```

### Nodemailer Configuration

In the `.env` file, set up the email configurations for sending OTPs:
```bash
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
