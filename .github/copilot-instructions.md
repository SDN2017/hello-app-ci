<!-- Use this file to provide workspace-specific custom instructions to Copilot. For more details, visit https://code.visualstudio.com/docs/copilot/copilot-customization#_use-a-githubcopilotinstructionsmd-file -->

# Spring Boot Hello App - Development Guidelines

## Project Overview
This is a Spring Boot REST API hello application with Maven build configuration. The application provides simple greeting endpoints for testing and demonstration purposes.

## Code Organization
- **Application Entry Point**: `src/main/java/com/example/springboot/HelloApplication.java`
- **REST Controllers**: `src/main/java/com/example/springboot/controller/`
- **Configuration**: `src/main/resources/application.properties`

## Build and Run

### Build
```bash
mvn clean install
```

### Run
```bash
mvn spring-boot:run
```

## Key Dependencies
- Spring Boot Starter Web 3.2.3
- Java 17
- Maven 3.6+

## Available Endpoints
- `GET /api/` - Welcome message
- `GET /api/hello` - Simple hello
- `GET /api/hello/{name}` - Hello with path variable
- `GET /api/greet?name=value` - Greet with query parameter
- `GET /api/api/health` - Health check

## Development Tips
- Changes to files in `src/main/java/` will be automatically reloaded when using `mvn spring-boot:run` (courtesy of Spring DevTools)
- Keep controllers lightweight; consider moving business logic to service classes
- Follow standard Spring Boot conventions for package naming and structure
