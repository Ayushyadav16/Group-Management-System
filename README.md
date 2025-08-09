# Group Management System

A simple Node.js-based web application for user authentication and password management using MySQL.

## Features

- User login with email and password
- Change password functionality
- Home page with navigation
- Styled with CSS and Handlebars templates

## Project Structure

```
.env
.gitignore
db.js
index.js
package.json
FrontEnd/
  LogIn/
    LogIn.html
public/
  style.css
queries/
  authQuery.js
Routes/
  auth.js
  pages.js
Schemas/
  login.sql
views/
  ChangePassword.hbs
  Home.hbs
  LogIn.hbs
```

## Setup Instructions

1. **Clone the repository**

2. **Install dependencies**

   ```sh
   npm install
   ```

3. **Configure environment variables**

   Edit `.env` file with your MySQL credentials:
   ```
   SDATABASE = project
   SUSER = root
   SPASSWORD = password
   SHOST = localhost
   ```

4. **Set up the database**

   - Create a MySQL database named `project`.
   - Run the SQL script in [`Schemas/login.sql`](Schemas/login.sql) to create the `LogIn` table and insert sample users.

5. **Start the server**

   ```sh
   npm start
   ```

   The server runs on port 5000 by default.

## Usage

- Visit `http://localhost:5000/` to access the login page.
- After logging in, you will be redirected to the home page.
- Use the "Change Password" link to update your password.

## Main Files

- [`index.js`](index.js): Entry point, sets up Express server and routes.
- [`db.js`](db.js): MySQL database connection.
- [`Routes/auth.js`](Routes/auth.js): Authentication and password change routes.
- [`Routes/pages.js`](Routes/pages.js): Page rendering routes.
- [`queries/authQuery.js`](queries/authQuery.js): Database queries for authentication.
- [`views/`](views/): Handlebars templates for UI.
- [`public/style.css`](public/style.css): CSS styles.