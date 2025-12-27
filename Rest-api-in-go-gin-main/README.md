# Go High-Performance REST API Engine

A production-ready REST API skeleton built with **Go (Golang)** and **Gin**, designed for high-throughput microservices. This project implements a scalable architecture separating routing, business logic, and database layers.

## 🚀 Tech Stack

* **Core:** Go 1.23, Gin Framework (High-performance HTTP web framework)
* **Database:** SQLite (embedded) with SQL Migrations
* **Authentication:** JWT (JSON Web Tokens) with middleware protection
* **Documentation:** Swagger / OpenAPI 3.0 auto-generation
* **Infrastructure:** Docker & Air (Hot Reload)

## ⚡ Key Features

* **Modular Architecture:** Clean separation of concerns (Handlers, Models, Middleware).
* **Secure Auth:** Stateless JWT authentication flow with bcrypt password hashing.
* **Robust Middleware:** Custom middleware for Error Handling, CORS, and Auth Validation.
* **Database Migrations:** Versioned SQL migrations using `golang-migrate`.
* **API Documentation:** Fully documented endpoints accessible via Swagger UI.

## 🛠️ Installation & Setup

### Prerequisites
* Go 1.23+
* Docker (Optional)

### Quick Start (Local)

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/elvand-lie/rest-api-go.git](https://github.com/elvand-lie/rest-api-go.git)
    cd rest-api-go
    ```

2.  **Install Dependencies**
    ```bash
    go mod download
    ```

3.  **Run Migrations** (Initialize the DB)
    ```bash
    go run cmd/migrate/main.go up
    ```

4.  **Start the Server**
    ```bash
    go run cmd/api/main.go
    ```

The API will be available at `http://localhost:8080`.

### 🐳 Docker Deployment

Build and run the containerized application:

```bash
docker build -t go-api-engine .
docker run -p 8080:8080 go-api-engine
