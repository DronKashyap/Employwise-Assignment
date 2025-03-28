# EmployWise User Management App

## Overview
This is a React-based user management application that integrates with the Reqres API to handle authentication, list users with pagination, and allow editing and deleting users.

## Features
### Level 1: Authentication
- Login with credentials:
  - Email: `eve.holt@reqres.in`
  - Password: `cityslicka`
- Token is stored in local storage upon successful login.
- Redirects to the Users List page after authentication.

### Level 2: User Listing
- Fetch users from the Reqres API using pagination (`GET /api/users?page=1`).
- Display users with their first name, last name, and avatar.
- Implement pagination for navigating between pages.

### Level 3: Edit, Delete, and Update Users
- **Edit:** Users can edit their details via a pre-filled form.
  - Updates are sent via `PUT /api/users/{id}`.
- **Delete:** Users can be deleted from the list.
  - Uses `DELETE /api/users/{id}`.
- Displays appropriate success/error messages.

## Technologies Used
- React.js
- Axios for API requests
- React Router for navigation
- Tailwind CSS for styling
- Local Storage for token persistence

## Installation and Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/DronKashyap/employwise-user-management.git
2. Navigate to the project directory:

cd employwise-user-management
3. Install dependencies:

npm install
Start the development server:

npm run dev

Usage
Open the application in the browser at http://localhost:5173.

Login using the provided credentials.

Navigate through the user list.

Edit or delete users as needed.

Project Structure

📦 employwise-user-management
 ┣ 📂 src
 ┃ ┣ 📂 components
 ┃ ┃ ┣ 📜 LoginForm.js
 ┃ ┃ ┣ 📜 UserList.js
 ┃ ┃ ┣ 📜 UserCard.js
 ┃ ┃ ┣ 📜 EditUser.js
 ┃ ┃ ┗ 📜 Pagination.js
 ┃ ┣ 📂 pages
 ┃ ┃ ┣ 📜 LoginPage.js
 ┃ ┃ ┣ 📜 UsersPage.js
 ┃ ┃ ┗ 📜 EditUserPage.js
 ┃ ┣ 📜 App.js
 ┃ ┣ 📜 index.js
 ┃ ┣ 📜 api.js
 ┃ ┗ 📜 styles.css
 ┣ 📜 .gitignore
 ┣ 📜 package.json
 ┣ 📜 README.md
 ┗ 📜 public
API Endpoints Used
POST /api/login - Authenticate user

GET /api/users?page=1 - Fetch paginated users

PUT /api/users/{id} - Update user details

DELETE /api/users/{id} - Delete a user

Error Handling
Displays error messages for failed login attempts.

Handles API request failures gracefully.

Form validation for login and edit user forms.

Bonus Features
✅ React Router for navigation
✅ Client-side search and filtering for users
✅ Deployed on https://employwise-assignment-rust.vercel.app/login