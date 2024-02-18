# Interlup Application

## Description

This application allows users to create and manage tasks with various status types to organize their demands and to-dos. 

Note: This application is available only for local access.

## Technologies Used

### Front-end

- React TypeScript
- Tailwind CSS
- Ant Design
- React DnD (Drag and Drop)

### Back-end

- Python
- Flask
- SQLAlchemy
- Pydantic
- Werkzeug
- Swagger UI

## Objectives

### Front-end

- User registration
- User login
- Displaying a list of tasks with title and description
- Editing an existing task (title and description)
- Marking a task as completed
- Deleting a task

### Back-end

- User registration
- User login
- Retrieving task(s)
- Task creation
- Task deletion
- Retrieving, creating, deleting, and updating column(s)
- Restricting CRUD operations on tasks/columns without authentication
- Documentation using Swagger UI

## Docker

- Dockerfile to containerize the application
- docker-compose.yml to orchestrate the containers

### Plus

- Column sorting
- Creating new columns
- Removing columns
- Utilization of SQLAlchemy for object-relational mapping
- Adherence to PEP 8 coding style

## Design Pattern

- Utilization of the Repository pattern

## Installation

1. Download the `dsf-interlup-api` and `dsf-interlup-front` repositories.

2. Configure the `.env` file inside the `dsf-interlup-api` repository with the following information:

```plaintext
DEBUG=True # True or False
SECRET_KEY=1231238901823901383iikajsdoajsdasd # your secret key
DATABASE_URL=postgresql://postgres:1234@your_host:5432/postgres # your PostgreSQL database connection
```

3. Execute `docker-compose up` inside the `dsf-interlup-api` repository and obtain the IP provided by the WSGI by running the command:

```bash
docker port API-INTERLUP-DSF
```

4. Access the `dsf-interlup-front` repository and configure the `.env` file with the following information:

```plaintext
REACT_APP_API_URL=http://your_host:port_wsgi
```

5. After configuring the `.env`, execute `docker-compose up front-dev` or `docker-compose up front-prod` inside the `dsf-interlup-front` repository.

6. Access `http://your_host:3000` to use the application.