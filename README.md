# TicketMaster Replica Project

A full-stack web application replicating the core functionalities of TicketMaster, built with modern technologies to demonstrate scalable architecture, real-time features, and robust security practices.

## Technologies

- **Backend**: Java, Spring Boot, Maven, Lombok, JUnit
- **Frontend**: JavaScript, React, HTML, CSS, Vite
- **Database**: MongoDB, Redis (for seat holds)
- **Deployment**: Docker Compose
- **Other**: Gradle (mentioned in build), FASTAPI (if applicable)

## Features

- **User Management**: Registration, login, role-based access (Admin, Organizer, User)
- **Event Creation**: Organizers can create and manage events with custom venue layouts
- **Ticket Purchasing**: Real-time seat selection and booking with hold logic
- **Ticket Resale**: Secure ticket resale and ownership transfer
- **Venue Builder**: Dynamic seating layout generation using design patterns
- **Admin Dashboard**: Event and user management tools
- **Real-time Updates**: Asynchronous API communication for seamless UI updates

## Architecture

The application follows a layered architecture pattern:
- **Controller Layer**: REST API endpoints
- **Service Layer**: Business logic and validations
- **Repository Layer**: Data access with Spring Data MongoDB
- **Domain Layer**: Core business models and entities

Key design patterns implemented:
- Builder Pattern for venue layout construction
- Template Pattern for flexible venue types
- Strategy Pattern for authentication methods

## Getting Started

### Prerequisites
- Java 17 or higher
- Node.js 16 or higher
- Docker and Docker Compose

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Ticketing-Site
   ```

2. **Start the database**
   ```bash
   docker-compose up -d
   ```

3. **Backend Setup**
   ```bash
   cd backend
   ./mvnw clean install
   ./mvnw spring-boot:run
   ```

4. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

5. **Access the application**
   - Frontend: http://localhost:5173 (default Vite port)
   - Backend API: http://localhost:8080

### Running Tests
```bash
cd backend
./mvnw test
```

## API Documentation

The backend provides RESTful APIs for:
- Authentication (`/api/auth`)
- Events (`/api/events`)
- Bookings (`/api/bookings`)
- Users (`/api/users`)
- Admin operations (`/api/admin`)

Detailed API documentation can be found in the controller classes with JavaDoc comments.

## Successes

- Designed and developed a full-stack ticketing platform enabling users to create events, purchase tickets, resell tickets, and transfer ownership of tickets.
- Implemented a layered architecture (Controller, Service, Repository, Domain) using Spring Boot, MongoDB, and REST APIs to ensure maintainable and scalable code.
- Applied object-oriented design principles including abstraction, inheritance, polymorphism, and encapsulation across core models such as User, Event, Booking, and Ticket.
- Created a visual venue layout builder using the Builder design pattern to dynamically generate seating layouts and sections for events.
- Built a React frontend with asynchronous API communication, enabling real-time UI updates without page reloads.
- Implemented testing of features through test-cases stored through JavaDocs

## Challenges

- Created a UI and UX friendly website through research and implementing logic and functions through JavaScript and JSX.
- Prevented double-booking of seats by implementing seat hold logic with expiration timers and validation checks, ensuring accurate seat allocation for simultaneous users.
- Managed ticket resale and ownership changes by creating service-layer validations to verify ticket ownership, resale eligibility, and event status before allowing transfers or resale.
- Designed a flexible venue layout system by building a Venue Builder module using Builder and Template patterns to dynamically generate seats, rows, and sections for multiple venue types.
- Enhanced authentication security by migrating to hashed passwords (BCrypt) and implementing token-based sessions, while maintaining support for legacy plaintext passwords during migration.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
