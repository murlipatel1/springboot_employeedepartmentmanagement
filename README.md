# springboot_employeedepartmentmanagement

# Employee and Department CRUD REST API

This repository contains a Spring Boot application that provides a RESTful API for performing CRUD (Create, Read, Update, Delete) operations on employee and department resources.

## Prerequisites

Before running the application, ensure that you have the following installed:

- Java Development Kit (JDK) 11 or higher
- Apache Maven

## Setup

1. Clone the repository:

   ```
   git clone https://github.com/your-username/employee-department-api.git
   ```

2. Navigate to the project directory:

   ```
   cd employee-department-api
   ```

3. Build the application using Maven:

   ```
   mvn clean package
   ```

4. Run the application:

   ```
   java -jar target/employee-department-api.jar
   ```

The API will be accessible at `http://localhost:8081`.

## API Endpoints

The following endpoints are available:

### Employee

- `GET /employees` - Retrieve all employees.
- `GET /employees/{id}` - Retrieve an employee by ID.
- `POST /employees` - Create a new employee.
- `PUT /employees/{id}` - Update an existing employee.
- `DELETE /employees/{id}` - Delete an employee.

### Department

- `GET /departments` - Retrieve all departments.
- `GET /departments/{id}` - Retrieve a department by ID.
- `POST /departments` - Create a new department.
- `PUT /departments/{id}` - Update an existing department.
- `DELETE /departments/{id}` - Delete a department.

## Request and Response Examples

### Employee

#### GET /employees

Response:
```json
[
    {
        "id": 1,
        "name": "John Doe",
        "email": "john.doe@example.com",
        "departmentId": 2
    },
    {
        "id": 2,
        "name": "Jane Smith",
        "email": "jane.smith@example.com",
        "departmentId": 1
    }
]
```

#### GET /employees/{id}

Response:
```json
{
    "id": 1,
    "name": "John Doe",
    "email": "john.doe@example.com",
    "departmentId": 2
}
```

#### POST /employees

Request:
```json
{
    "name": "Alice Johnson",
    "email": "alice.johnson@example.com",
    "departmentId": 1
}
```

Response:
```json
{
    "id": 3,
    "name": "Alice Johnson",
    "email": "alice.johnson@example.com",
    "departmentId": 1
}
```

#### PUT /employees/{id}

Request:
```json
{
    "name": "Alice Johnson",
    "email": "alice.johnson@example.com",
    "departmentId": 2
}
```

Response:
```json
{
    "id": 3,
    "name": "Alice Johnson",
    "email": "alice.johnson@example.com",
    "departmentId": 2
}
```

#### DELETE /employees/{id}

Response:
```
Employee with ID 3 deleted successfully.
```

### Department

#### GET /departments

Response:
```json
[
    {
        "id": 1,
        "name": "IT"
    },
    {
        "id": 2,
        "name": "HR"
    }
]
```

#### GET /departments/{id}

Response:
```json
{
    "id": 1,
    "name": "IT"
}
```

#### POST /departments

Request:
```json
{
    "name": "Finance"
}
```

Response:
```json
{
    "id": 3,
    "name": "Finance"
}
```

#### PUT /departments/{id}

Request:
```json
{
    "name": "Human Resources"
}
```

Response:
```json
{
    "id": 2,
    "name": "Human Resources"
}
```

#### DELETE /departments/{id}

Response:
```
Department with ID 3 deleted successfully.
```

## Database Configuration

The application is configured to MySql database.
You have to modify the database settings in the `application.properties` file.

