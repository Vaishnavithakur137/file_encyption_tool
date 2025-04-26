# file_encyption_tool

## Overview
The **File Encryption Tool** is a Java-based application designed to enhance file security by encrypting sensitive files and managing user authentication through email verification. This project utilizes MySQL as the database to store user information and encrypted file data.

## Features
- **File Encryption**: Secure sensitive files by encrypting them before storage.
- **Email Authentication**: Users can sign up and log in using their email addresses, ensuring that only authorized users can access the tool.
- **User  Management**: The application allows users to register, log in, and manage their files securely.
- **Database Integration**: Utilizes MySQL to store user credentials and encrypted file data.

## Technologies Used
- **Java**: The primary programming language for developing the application.
- **MySQL**: Database management system for storing user data and file information.
- **JavaMail API**: For sending email notifications and OTPs for user authentication.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/FileEncryptionTool.git
   ```
2. Navigate to the project directory:
   ```bash
   cd FileEncryptionTool
   ```
3. Ensure you have MySQL installed and create a database named `ytproject`.
4. Update the database connection details in `MyConnection.java`.
5. Compile and run the project using your preferred IDE or command line.

## Usage
1. **Run the Application**: Start the application by executing the `Main` class.
2. **User  Registration**:
   - Choose the signup option.
   - Enter your name and email.
   - An OTP will be sent to your email for verification.
3. **User  Login**:
   - Enter your registered email to log in.
   - An OTP will be sent to your email for verification.
4. **File Management**:
   - After logging in, you can:
     - View hidden files.
     - Hide new files by providing their path.
     - Unhide files by selecting their ID.

## Project Structure
- **src**: Contains all the Java source files.
  - **dao**: Data Access Objects for interacting with the database.
  - **model**: Contains data models like `User ` and `Data`.
  - **service**: Business logic for user management and OTP generation.
  - **views**: User interface classes for interaction.
  - **db**: Database connection management.
- **pom.xml**: Maven configuration file for managing dependencies.

## Explanation of the Project
The File Encryption Tool is designed to provide a secure way for users to manage sensitive files. Here’s a breakdown of the key components:

### User Registration and Authentication:
- Users can register by providing their name and email. An OTP is generated and sent to their email for verification.
- Upon successful registration, users can log in using their email, and again, an OTP is sent for authentication.

### File Management:
- Users can hide files, which involves encrypting the file and storing it in the database along with its metadata (name, path, email).
- The application allows users to view their hidden files and unhide them by decrypting the file and restoring it to its original location.

### Database Interaction:
- The application uses MySQL to store user credentials and file data. The `MyConnection` class manages the database connection, while the `User DAO` and `DataDAO` classes handle data operations.

### Email Notifications:
- The `SendOTPService` class is responsible for sending OTPs to users via email, ensuring secure access to the application.

## Conclusion
The File Encryption Tool is a comprehensive solution for users looking to secure their sensitive files. With features like email authentication and file encryption, it provides a robust framework for managing file security.


