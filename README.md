# airbnb-clone-project
**About the Project**
- The Airbnb Clone Project is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security. This project enables the developers to understand complex architectures, workflows, and collaborative team dynamics while building a scalable web application.

**Team Roles**
- **Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.
- **Database Administrator**: Manages database design, indexing, and optimizations.
- **DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.
- **QA Engineer**: Ensures the backend functionalities are thoroughly tested and meet quality standards.

**Technology Stack**
- **Django**: A high-level Python web framework used for building the RESTful API.
- **Django REST Framework**: Provides tools for creating and managing RESTful APIs.
- **PostgreSQL**: A powerful relational database used for data storage.
- **GraphQL**: Allows for flexible and efficient querying of data.
- **Celery**: For handling asynchronous tasks such as sending notifications or processing payments.
- **Redis**: Used for caching and session management.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

**Database Design**
**Users**: Fields for this entity are Id (primary key), Username, Contact, RoomId, BookingTime
**Properties**: Id(Primary key), Propertyname, price, status, UserId(User foreign Key)
**Bookings**: Id(Primary key), UserId(Foreign key from Users), PaymentId (Foreign Key from Payments table), Timestamp
**Reviews**: Id (Primary key), UserId (Foreign key from Users), PropertyId (Foreign key from Properties table), ReviewCount, Rating
**Payments**: Id (Primary key), PropertyId (foreign key from Properties table), UserId (Foreign Key from Users table), Timestamp

**Feature Breakdown**
- **1. API Documentation**
- **OpenAPI Standar**d: The backend APIs are documented using the OpenAPI standard to ensure clarity and ease of integration.
- **Django REST Framework**: Provides a comprehensive RESTful API for handling CRUD operations on user and property data.
- **GraphQL**: Offers a flexible and efficient query mechanism for interacting with the backend.
-**2. User Authentication**
**Endpoints**: /users/, /users/{user_id}/
**Features**: Register new users, authenticate, and manage user profiles.
-**3. Property Management**
**Endpoints**: /properties/, /properties/{property_id}/
**Features**: Create, update, retrieve, and delete property listings.
-**4. Booking System**
**Endpoints**: /bookings/, /bookings/{booking_id}/
**Features**: Make, update, and manage bookings, including check-in and check-out details.
-**5. Payment Processing**
**Endpoints**: /payments/
**Features**: Handle payment transactions related to bookings.
- 6. **Review System**
**Endpoints**: /reviews/, /reviews/{review_id}/
**Features**: Post and manage reviews for properties.
- 7. **Database Optimizations**
**Indexing**: Implement indexes for fast retrieval of frequently accessed data.
**Caching**: Use caching strategies to reduce database load and improve performance.

**API Security**
- **Authentication** - Verifying user identification before granting access, using secure session management. 
- Importance: This protects user accounts from unauthorized access and preventing attackers from impersonating legitimate users
- **Authorization** - This is to control access levels for the registered users by enforcing role-base access.
- **Purpose**: Prevents unauthorized actions, such as a guest editing someone else's property or a user viewing another’s payment history.
- **Secure payment**: Secure online transactions and payment data through using https in all transactions and encrypt data in transit
- Purpose: Protect users financial information and build trust with users
- **Secure  data sorage**: to safeguard user data at rest
- Purpose: prevent data leaks incase the database is compromised

**CI/CD Pipeline**
CI (Continuous Integration) - Automatically tests  and code sent to a respository e.g. Github, Linting
CD (Continuos Deployment) - Automatically deploys code to production after passing all the set tests e.g. Docker, which ensures consistent environment in staging and prodcution

