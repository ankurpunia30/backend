Here's an updated README.md for your project, reflecting the progress you've made and the features you've implemented:

---

# Blood Bank User Portal

## Project Overview

The Blood Bank User Portal is a web application designed to connect users with hospitals for blood donation and receiving services. It allows users to register, view hospital details, request blood, and track their donation and receiving history. The application also includes features for hospital registration, approval by admins, and user authentication.

## Features

- **User Registration and Login**: Users can create an account and log in to the system securely.
- **Hospital Registration**: Hospitals can register for access to the platform, pending admin approval.
- **Admin Dashboard**: Admins can view and manage hospital registration requests.
- **Blood Request Functionality**: Users can request blood from registered hospitals.
- **Donation and Receiving History**: Users can view their history of blood donations and receptions.
- **Email Notifications**: Users and hospitals receive email notifications for registration approvals and other important updates.
  
## API Endpoints

### User Endpoints

- **POST `/api/user/register`**: Register a new user.
- **POST `/api/user/login`**: Log in a user and receive a JWT token.
- **GET `/api/user/profile`**: Get details of the authenticated user, including donation and receiving history.

### Hospital Endpoints

- **POST `/api/hospital/register`**: Register a new hospital (pending admin approval).
- **GET `/api/hospital/pending-requests`**: Retrieve all pending hospital registration requests.
- **POST `/api/hospital/pending-requests/:id`**: Approve or deny a pending hospital request.

### Admin Endpoints

- **POST `/api/admin/login`**: Admin login to manage the portal.
- **GET `/api/admin/pending-requests`**: Get a list of pending hospital requests.

## Technologies Used

- **Backend**: Node.js, Express.js
- **Database**: MongoDB (using Mongoose)
- **Authentication**: JWT (JSON Web Tokens)
- **Email Service**: Nodemailer
- **Environment Variables**: dotenv for managing sensitive information
- **Frontend**: React (optional for future implementation)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd blood-bank-portal
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Create a `.env` file in the root directory and set the following variables:
   ```plaintext
   PORT=3000
   TOKEN_KEY=your_jwt_secret_key
   EMAIL_USER=your_email@example.com
   EMAIL_PASS=your_email_password
   ```
5. Start the server:
   ```bash
   npm start
   ```

## Testing

Use tools like Postman to test the API endpoints. Ensure to include the `Authorization` header with the JWT token for protected routes.

## Future Enhancements

- **Frontend Development**: Build a user-friendly frontend using React.
- **Improved Error Handling**: Implement more granular error handling for better user experience.
- **User Interface for Admins and Hospitals**: Create dashboards for admins and hospitals to manage their functionalities more efficiently.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any feature requests or bugs.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to customize this further or let me know if there are any specific sections you’d like to add!