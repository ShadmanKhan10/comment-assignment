# Comments System with User Authentication

This project features a real-time commenting system built with Next.js for the front-end and Node.js for the back-end. It enables users to log in using a username, submit comments, and view updates in real-time via Socket.IO. Comments are stored in a MySQL database, and the user interface is designed to be responsive, utilizing Material UI for styling.

## Features

- **Login** with username
- **Real-Time Comments**: All comments appear live across users’ screens
- **Responsive Design** with Material UI

## Technologies

- **Front-End**: Next.js, Material UI, Axios
- **Back-End**: Node.js, Express, MySQL, Socket.IO
- **Database**: MySQL for comments storage

## Setup

### Prerequisites

- Install Node.js and MySQL

### Steps

1. **Clone Repo**:

   ```bash
   git clone https://github.com/yourusername/your-repository-name.git
   cd your-repository-name
   ```

2. **Install Dependencies**:

   ```bash
   # Front-End
   cd frontend
   npm install

   # Back-End
   cd ../backend
   npm install
   ```

3. **MySQL Database Setup**:

   ```sql
   CREATE DATABASE comments_db;
   USE comments_db;
   CREATE TABLE comments (
     id INT AUTO_INCREMENT PRIMARY KEY,
     username VARCHAR(255),
     comment TEXT,
     timestamp DATETIME DEFAULT CURRENT_TIMESTAMP
   );
   ```

4. **Environment Variables**:

   - **Back-End** (`.env`):
     ```plaintext
     PORT=5000
     DB_HOST=localhost
     DB_USER=your_mysql_username
     DB_PASSWORD=your_mysql_password
     DB_NAME=comments_db
     ```

## Usage

1. **Start Servers**:
   - Back-End: `cd backend && npm start`
   - Front-End: `cd frontend && npm run dev`
2. **Access**: Open [http://localhost:3000](http://localhost:3000) in your browser.
3. **Test Comments**: Log in with a username, post comments, and see live updates across sessions.
