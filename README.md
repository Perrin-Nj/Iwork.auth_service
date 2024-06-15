# iwork.auth-service

[Auth Service](https://drive.google.com/file/d/1-lyg4c9pjCEnadINvOXXGMIhGzbC3xqV/view?usp=sharing)

## Overview

The `auth-service` is responsible for handling authentication and authorization within the **Iwork** system. It verifies client credentials and grants access to protected resources based on predefined roles and permissions.

## Features

- **Authentication**:
  - Verify client credentials (username/password or token-based).
  - Issue and validate access tokens.

- **Authorization**:
  - Determine access rights based on user roles (super admin, employer, employee).

- **Security**:
  - Ensure secure communication using HTTPS.
  - Implement best practices for password storage and authentication flows.

- **Integration**:
  - Integrate with Firebase for user management.
  - Communicate with other microservices for centralized authentication and authorization.

## Technologies Used

- Spring Boot
- Spring Security
- Firebase Authentication
- JWT (JSON Web Tokens)
- HTTPS
- Docker (for containerization)

## Prerequisites

- Java 21 or higher
- Maven 3.6.3 or higher
- Firebase Admin SDK credentials (for Firebase integration)

## Getting Started

### Clone the repository

```bash
git clone https://github.com/yourusername/iwork-auth-service.git
cd iwork-auth-service
```

### Configuration

1. **Firebase Setup**:
   - Create a Firebase project and enable Firebase Authentication.
   - Obtain Firebase Admin SDK credentials and configure in the application.

2. **Application Configuration**:
   - Update `application.yaml` with Firebase configuration and other necessary settings.

### Build and Run

```bash
mvn clean install
java -jar target/iwork-auth-service-1.0.jar
```

### Usage

- The `auth-service` provides endpoints for:
  - User authentication (`/api/auth/login`, `/api/auth/logout`)
  - Token validation (`/api/auth/validate`)
  - User role management (integration with user management services)

### API Documentation

- Swagger/OpenAPI documentation: `http://localhost:8080/swagger-ui.html`

### Security Considerations

- Ensure Firebase Admin SDK credentials are kept secure and not exposed in public repositories.
- Implement HTTPS to protect data during transit.
- Validate and sanitize inputs to prevent security vulnerabilities (XSS, SQL injection, etc.).

## Contributing

Contributions are welcome! Fork the repository and submit a pull request.

## License

BSD 3-Clause License with Commercial Use Contact Requirement - see the [LICENSE](https://joinup.ec.europa.eu/licence/bsd-3-clause-new-or-revised-license) file for details.

## Acknowledgments

- Inspired by the need for robust authentication and authorization in the **Iwork** system.
- Thanks to the Spring Boot and open-source community for their invaluable tools and frameworks.
