# PHP-SQL-Connectivity


This project implements a basic user registration system with a registration form connected to a MySQL database. Users can input their username, password, and email to register, and the data will be stored securely in a MySQL database.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [Additional Notes](#additional-notes)
- [License](#license)

## Prerequisites

Before you begin, ensure you have the following installed:

- PHP on your server
- MySQL database server
- Web server (e.g., Apache, Nginx) configured to handle PHP files

## Setup

1. **Database Setup:**

   - Create a MySQL database and a table to store user information. You can use tools like phpMyAdmin or the MySQL command line.

   ```sql
   CREATE DATABASE mydatabase;
   USE mydatabase;

   CREATE TABLE users (
       id INT PRIMARY KEY AUTO_INCREMENT,
       username VARCHAR(50) NOT NULL,
       password VARCHAR(255) NOT NULL,
       email VARCHAR(100) NOT NULL
   );

2. **Files:**
   - Download or clone this repository on your web server.
3. **Database Configuration:**
   - Open **register.php** in text editor. 
   - Modify database parameter according to your setup.
   
     ```php
     $conn = new mysqli("localhost", "username", "password", "mydatabase");

## Usage
1. **Access the Registration Form:**
    - Open your web browser and navigate to the registration form URL, e.g., http://localhost/register.html.

2. **Fill out the Registration Form:**
    - Enter your desired username, a secure password, and a valid email address into the registration form.
  
      <img width="960" alt="Screenshot 2023-11-23 130606" src="https://github.com/parthkhajgiwale/PHP-SQL-Connectivity/assets/90266917/aa0f6ba2-1a5e-48ba-83c3-2e24d220c534">

3. **Submit the Form:**
    - Click the "Register" button to submit the form.
  
4. **Check Registration Result:**
    - If the registration is successful, you will see a message indicating success.
    - If there's an error, an error message will be displayed with details.
  <img width="960" alt="Screenshot 2023-11-23 130557" src="https://github.com/parthkhajgiwale/PHP-SQL-Connectivity/assets/90266917/24e67433-6410-4a33-9dfe-b52be694d59e">

      

5. **Review the Database:**
    - Check your MySQL database to confirm that the user information has been stored in the users table.
<img width="960" alt="Screenshot 2023-11-23 131047" src="https://github.com/parthkhajgiwale/PHP-SQL-Connectivity/assets/90266917/356b357f-a0dd-49c5-9778-bd4ae3602ac0">



## Additional Notes

- The provided code is a basic example. In a production environment, consider implementing additional security measures, such as input validation, error handling, and using prepared statements to prevent SQL injection.

- The password is hashed using password_hash() for security. Ensure your server supports this function (PHP 5.5.0 and above).

- Styling for the registration form is provided in style.css. You can modify it to fit your design preferences.

  ## LICENSE
  This project is licensed under the MIT License - see the LICENSE file for details.
