# Task Manager API

A Java Spring Boot REST API for managing tasks with features such as CRUD operations, tagging, due dates, and status tracking.
Designed with scalability and clarity in mind, this project serves as a foundation for real-world task or project management systems.

---

## Features
- Task creation, update, retrieval, and deletion
- Status management: PENDING, IN_PROGRESS, COMPLETED
- Due date and tagging support
- RESTful design with JSON-based API responses
- Integrated Swagger/OpenAPI documentation
- In-memory (H2) or persistent database support (MySQL/PostgreSQL ready)

---

## Tech Stack
- Java 17+
- Spring Boot 3+
- Spring Data JPA
- Hibernate
- H2/MySQL/PostgreSQL (configurable)
- Maven for dependency management

---

## Getting Started

### Prerequisites
- Java 17+
- Maven 3+
- (Optional) Docker for containerized deployment

### Clone the Repository
git clone https://github.com/dimazbtw/task-manager-api.git
cd task-manager-api

### Build and Run
#### Using Maven:
mvn clean install
mvn spring-boot:run

#### Using Docker:
docker build -t task-manager-api .
docker run -p 8080:8080 task-manager-api

---

## API Usage

### Base URL
http://localhost:8080/api/v1/tasks

### Swagger Documentation
http://localhost:8080/swagger-ui.html

### Example Endpoints
- GET /tasks – Get all tasks
- POST /tasks – Create a new task
- GET /tasks/{id} – Get a task by ID
- PUT /tasks/{id} – Update a task
- DELETE /tasks/{id} – Delete a task

#### Example JSON for Creating a Task
{
  "title": "Build Task Manager API",
  "description": "Implement CRUD and Swagger documentation",
  "status": "PENDING",
  "dueDate": "2025-09-15",
  "tags": ["springboot", "backend"]
}

---

## Configuration
Modify application.properties to switch databases:
spring.datasource.url=jdbc:mysql://localhost:3306/task_manager
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update

---

## Testing
Run all tests:
mvn test

---

## Deployment
- Docker-ready
- Can be deployed to AWS, Azure, GCP, or Heroku
- Supports externalized configuration using environment variables:
SPRING_PROFILES_ACTIVE=prod
DB_URL=jdbc:mysql://your-db-host:3306/task_manager
DB_USER=your-username
DB_PASSWORD=your-password

---

## License
Licensed under the MIT License.
See the LICENSE file for details.

---

## Contributing
1. Fork this repository
2. Create a new branch: git checkout -b feature/your-feature
3. Commit your changes: git commit -m "Add new feature"
4. Push your branch: git push origin feature/your-feature
5. Open a Pull Request
