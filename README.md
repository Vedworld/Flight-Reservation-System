Flight Reservation System
Table of Contents
Project Overview
Technologies Used
Features
System Architecture
Database Schema
Installation
Usage
API Documentation
Future Enhancements
Contributing
License
Project Overview
The Flight Reservation System is a full-stack web application that allows users to search, book, and manage flight reservations. It provides separate functionalities for users and administrators. Users can book flights, manage their reservations, and make secure payments. Administrators can manage flights, airports, and scheduled flights.

The project follows a microservices architecture, where the user-side backend is powered by Java with Spring Boot and the admin-side backend by ASP.NET Core. The frontend is developed using React.js, with MySQL serving as the database. Additional features like PDF ticket generation and real-time email and SMS notifications are integrated into the system.


Technologies Used
Frontend:
React.js
HTML, CSS, Bootstrap
Backend:
Java with Spring Boot (User functionality)
ASP.NET Core (Admin functionality)
Hibernate (ORM for Java)
Database:
MySQL
Other Technologies:
RESTful APIs
JWT (JSON Web Tokens) for authentication
PDF generation for tickets
Email and SMS notifications (e.g., via Twilio or SMTP)
GitHub for version control
Docker for containerization
Features
User Features:

Flight search and booking
User registration and login
View and manage bookings
Receive notifications for booking status via email/SMS
Secure payments with confirmation
Admin Features:

Add, update, or delete flights and schedules
Manage airports and flight data
View all users and bookings
Generate reports
Additional Features:

PDF ticket generation post-booking
Real-time notifications for booking confirmations or cancellations
Role-based access control (Users vs Admins)
API documentation using OpenAPI for easy integration
System Architecture
The system is divided into two main backend components:

User Service (Java, Spring Boot): Responsible for flight bookings, user management, and payments.
Admin Service (ASP.NET Core): Admins manage flight schedules, user accounts, and bookings.
Key Components:
React Frontend communicates with both backend services via REST APIs.
MySQL Database stores user data, booking information, flight schedules, and payment details.
Spring Boot & ASP.NET Core handle business logic and expose RESTful APIs for communication with the frontend.
Database Schema
The database includes the following main entities:

User: Stores user details such as user_id, name, email, and role (User/Admin).
Flight: Stores flight details such as flight_id, departure_time, arrival_time, and airline_name.
Airport: Stores airport information such as airport_code, city, and country.
Booking: Stores booking details for users such as booking_id, flight_id, user_id, status, and payment_status.
Scheduled Flight: Tracks scheduled flights for specific dates.
Payment: Stores transaction details for each booking.
