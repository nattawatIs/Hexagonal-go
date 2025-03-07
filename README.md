# Hexagonal Architecture in Go

## Overview

This project follows the Hexagonal Architecture (Ports and Adapters) pattern in Go, focusing on decoupling business logic from external dependencies.

## Project Structure

```
├── adapters          # Implementations of external interfaces
│   ├── gorm_adapter.go  # Database adapter using GORM
│   └── http_adapter.go  # HTTP adapter for handling API requests
├── core              # Core business logic and domain entities
│   ├── order.go          # Order entity definition
│   ├── order_repository.go # Repository interface for orders
│   └── order_service.go   # Order service implementing business logic
├── docker-compose.yml  # Docker configuration (if applicable)
├── go.mod             # Go module file
├── go.sum             # Go module dependencies
└── main.go            # Application entry point
```

## Getting Started

### Prerequisites

- Go 1.18+
- Docker (if using `docker-compose.yml`)

### Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/hexagonal-go.git
   cd hexagonal-go
   ```
2. Install dependencies:
   ```sh
   go mod tidy
   ```
3. Run the application:
   ```sh
   go run main.go
   ```

## Hexagonal Architecture Explanation

- **Core**: Contains the domain entities, repository interfaces, and business logic.
- **Adapters**: Implement the interfaces defined in the core, such as database and API handling.
- **Main Application**: Initializes dependencies and starts the application.

## Configuration

Modify `docker-compose.yml` and other configurations as needed for database and service connections.

