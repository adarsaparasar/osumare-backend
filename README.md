# osumare-backend
Building a RESTful API for an assignment.



## Overview

This project is a simple Task Manager application consisting of a backend RESTful API built with Node.js and Express, and a frontend built with React.js.

### Backend

The backend provides an API for managing tasks, including creating, retrieving, updating, and deleting tasks. It uses in-memory storage, meaning the tasks will be lost when the server restarts.



## Setup

### Prerequisites

- Node.js and npm installed
- Git installed

### Installation

1. Clone the repository:
   `
   git clone https://github.com/adarsaparasar/osumare-backend.git
   cd osumare-backend `

2. Setup the backend:
`cd backend
npm install
node server.js`

3. Usage
   
  -Backend: Runs on http://localhost:8080

## API Endpoints

1. GET /tasks

-Retrieves a list of all tasks.
-Response: `[{ id: 1, Title: "Task Title", Description: "Task Description" }, ...]`

2.  GET /tasks/id

-Retrieves a specific task by ID.
-Response: `{ id: 1, Title: "Task Title", Description: "Task Description" }`

3. POST /tasks

-Creates a new task.
-Request Body:` { Title: "Task Title", Description: "Task Description" }`
-Response: `{ id: 1, Title: "Task Title", Description: "Task Description" }`

4. PUT /tasks/

-Updates an existing task by ID.
-Request Body:`{ Title: "Updated Title", Description: "Updated Description" }`
-Response: `{ id: 1, Title: "Updated Title", Description: "Updated Description" }`

5. DELETE /tasks/

-Deletes a task by ID.
-Response: `[{ id: 1, Title: "Deleted Title", Description: "Deleted Description" }]`


## API CHECKING WITH CURL

1. Create a Task:
- `curl -X POST http://localhost:3000/tasks -H "Content-Type: application/json" -d '{"title": "Sample Task", "description": "This is a sample task."}'`

2. Get All Tasks:
-`curl http://localhost:3000/tasks`

3. Get a Task by ID:
-`curl http://localhost:3000/tasks/1`

4. Update a Task:
-`curl -X PUT http://localhost:3000/tasks/1 -H "Content-Type: application/json" -d '{"title": "Updated Task", "description": "This is an updated task."}'`

5. Delete a Task:
-`curl -X DELETE http://localhost:3000/tasks/1`