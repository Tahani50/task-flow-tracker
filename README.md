# TaskFlow – Full-Stack Task Tracker

## Project Description

**TaskFlow** is a simple full-stack web application for organizing personal and team tasks.
Users can create tasks, set due dates and priorities, mark tasks as done, and filter their list
to see what needs attention today.

**Who it's for:** students and junior developers who juggle study, work, and side projects and
want one clean place to track what's next, without the complexity of large project-management tools.

**Purpose:** to practice building a complete full-stack app from scratch (front end, back end,
database, and version control) while producing a useful tool for daily planning.

---

## Front-End Plan

- **Technology:** HTML, CSS, and JavaScript (may upgrade to React or Blazor in a later module)
- **Pages / Views:**
  - Login and Sign-up page
  - Dashboard: task list with filters and sort options
  - Add / Edit Task form
- **Responsibilities:**
  - Display tasks returned by the API
  - Validate form input before sending (e.g., title is required)
  - Call the back-end REST API using `fetch`
  - Responsive layout that works on mobile and desktop

---

## Back-End Plan

- **Technology:** C# with ASP.NET Core Web API
- **Database:** SQL Server (or SQLite for local development) using Entity Framework Core
- **Data Models:**
  - `User`: Id, Name, Email, PasswordHash
  - `TaskItem`: Id, Title, Description, DueDate, Priority, Status, UserId
- **API Endpoints:**

| Method | Endpoint            | Description            |
|--------|---------------------|------------------------|
| POST   | `/api/auth/register`| Create a new user      |
| POST   | `/api/auth/login`   | Log in and get a token |
| GET    | `/api/tasks`        | Get the user's tasks   |
| GET    | `/api/tasks/{id}`   | Get one task           |
| POST   | `/api/tasks`        | Create a task          |
| PUT    | `/api/tasks/{id}`   | Update a task          |
| DELETE | `/api/tasks/{id}`   | Delete a task          |

