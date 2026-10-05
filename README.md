# Expert Decision Replay Platform

A backend system for managing, reviewing, comparing, and tracking expert decisions in an organized and auditable way.

## Overview

The **Expert Decision Replay Platform** allows organizations to record decisions, review alternatives, add comments and tags, manage approvals, and maintain an audit history.

The platform helps users understand **how and why a decision was made** by preserving its complete decision journey.

## Features

* User registration and login
* JWT-based authentication
* Role-based access control
* Decision creation and management
* Alternative management
* Decision comparison
* Comments and tags
* Approval workflow
* Audit and activity logs
* Search functionality
* Dashboard and analytics
* Reports generation
* Risk-level classification
* PDF and Excel reports

## User Roles

The system supports four roles:

* **Employee** – Create and view decisions
* **Reviewer** – Review decisions and provide feedback
* **Manager** – Manage approvals and review decisions
* **Administrator** – Manage and monitor the system

## Technology Stack

* **Python**
* **FastAPI**
* **SQLAlchemy**
* **PostgreSQL**
* **Pydantic**
* **JWT Authentication**
* **Alembic**

## Project Structure

```text
Backend/
│
├── app/
│   ├── main.py
│   ├── models/
│   ├── schemas/
│   ├── routers/
│   ├── database/
│   └── ...
│
├── alembic/
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/d65462721-code/Backend.git
cd Backend
```

Create a virtual environment:

```bash
py -m venv venv
```

Activate the virtual environment:

### Windows

```powershell
.\venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
py -m pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file and add the required database and authentication configuration.

Example:

```env
DATABASE_URL=your_database_url
SECRET_KEY=your_secret_key
ALGORITHM=HS256
```

> Do not upload the `.env` file to GitHub.

## Running the Backend

Start the FastAPI server:

```bash
py -m uvicorn app.main:app --reload
```

The API will run at:

```text
http://127.0.0.1:8000
```

## API Documentation

FastAPI automatically provides interactive API documentation.

Swagger UI:

```text
http://127.0.0.1:8000/docs
```

ReDoc:

```text
http://127.0.0.1:8000/redoc
```

## Database

The project uses **PostgreSQL** as the database and **SQLAlchemy** for database operations.

Alembic is used for database migrations.

## Authentication

The platform uses **JWT-based authentication**.

Users log in using their credentials and receive an authentication token that is used to access protected API endpoints.

## Decision Replay

The main purpose of the platform is to preserve the complete decision journey.

A decision can contain:

```text
Decision
   │
   ├── Alternatives
   ├── Comments
   ├── Tags
   ├── Approvals
   └── Audit History
```

This allows users to review what decision was made, what alternatives were considered, who reviewed it, and what activities occurred throughout the process.

## Reports

The backend supports generating reports in:

* PDF
* Excel

Reports can be used for decision analysis, tracking, and auditing.

## Future Enhancements

* AI-assisted decision analysis
* Advanced recommendation system
* More analytics and visualizations
* Notification system
* Cloud deployment
* Advanced search and filtering

## License

This project is licensed under the MIT License.
