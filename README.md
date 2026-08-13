# Booking System API

REST API for a booking/reservation system, built as the integrator project for the Ada School backend course. Each course module adds a new layer on top of this base project.

## Tech Stack

- Java 17
- Spring Boot 4.1.0
- Spring Web (MVC)
- Maven

## Prerequisites

- JDK 17+
- Maven 3.9+ (or use the included `mvnw` / `mvnw.cmd` wrapper)

## Getting Started

Clone the repository and run the application:

```bash
git clone https://github.com/AnderssonProgramming/booking-system-api.git
cd booking-system-api

# using the Maven wrapper
./mvnw spring-boot:run

# or with a local Maven install
mvn spring-boot:run
```

The application starts on **http://localhost:8080**.

## API Endpoints

| Method | Endpoint  | Description                          |
|--------|-----------|---------------------------------------|
| GET    | `/health` | Health check — confirms the API is up |

Example:

```bash
curl http://localhost:8080/health
```

Response:

```html
<h1>The API is working ok!</h1>
```

## Project Structure

```
src/main/java/com/andersson/bookingsystemapi/
├── BookingSystemApiApplication.java   # Spring Boot entry point
└── controller/
    └── health/
        └── HealthController.java      # GET /health
```

## Building

```bash
./mvnw clean package
```

The packaged jar is generated at `target/booking-system-api-0.0.1-SNAPSHOT.jar` and can be run with:

```bash
java -jar target/booking-system-api-0.0.1-SNAPSHOT.jar
```
