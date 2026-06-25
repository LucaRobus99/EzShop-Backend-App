# EzShop - Backend Application 🛒

**Politecnico di Torino - Software Engineering 1 (SE1)**

EzShop is a comprehensive backend application designed to manage retail store operations. It provides a RESTful API for handling users, inventory (products), sales, returns, customer loyalty cards, and orders.

This repository contains the complete artifact of the project, including all the software engineering documentation produced during the different phases of the lifecycle, the source code, and the test reports.

---

## 📈 Implementation Phases & Documentation

The project followed a structured software engineering lifecycle. Below are the key phases and their corresponding documentation:

### 1. Requirements Engineering
In this phase, we analyzed the stakeholder needs, defined the use cases, and produced the conceptual models (Class Diagrams, State Diagrams).
- 📄 **[Requirements Document](doc/Requirements.md)**: Detailed use cases, scenarios, and UML diagrams (context diagram, class diagrams, etc.).

### 2. GUI Design
Even though this is a backend application, the graphical user interfaces were designed to understand the user flow and properly map the frontend interactions to the backend API endpoints.
- 📄 **[GUI Mockups & Design](doc/GraphicalUserInterface.md)**: Interface designs and wireframes.

### 3. Project Estimation & Planning
Before the implementation, we estimated the effort, time, and cost of the project using standard software engineering metrics (e.g., Function Points, LOC, COCOMO).
- 📄 **[Estimation Part 1](doc/Estimation.md)**
- 📄 **[Estimation Part 2](doc/EstimationPart2.md)**
- 📄 **[TimeSheet](doc/TimeSheet.md)**: Log of the actual time spent on different activities.

### 4. Implementation
The system was implemented using a modern Python stack following the MVC (Model-View-Controller) architectural pattern. The codebase is organized into domain-driven modules:
- **Controllers** (`app/controllers`): Business logic.
- **Routes** (`app/routes`): FastAPI endpoints mapping.
- **Models & DAOs** (`app/database` / `app/models`): SQLAlchemy ORM models and Data Access Objects.

### 5. Testing & Quality Assurance
We applied rigorous testing practices, including Unit, Integration, and System testing using `pytest`. Test coverage was monitored to ensure system reliability.
- 📄 **[Test Report](doc/TestReport.md)**: Traceability matrix, coverage metrics, and detailed results of the test suites.

---

## 🛠 Tech Stack

- **Framework**: [FastAPI](https://fastapi.tiangolo.com/) (Asynchronous, fast, and robust Python web framework)
- **Database**: SQLite with `aiosqlite` for asynchronous DB operations.
- **ORM**: [SQLAlchemy](https://www.sqlalchemy.org/)
- **Authentication**: JWT (`PyJWT`) for secure stateless sessions.
- **Testing**: `pytest`, `pytest-asyncio`, `pytest-cov`

---

## 🚀 Setup & Installation

### Prerequisites
- Python 3.9+
- Git

### Installation Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/LucaRobus99/EzShop-Backend-App.git
   cd EzShop-Backend-App
   ```

2. **Create a virtual environment and activate it**:
   ```bash
   python -m venv .venv
   
   # On Windows:
   .venv\Scripts\activate
   
   # On Linux/macOS (or WSL):
   source .venv/bin/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Initialize the Database**:
   ```bash
   python init_db.py
   ```

---

## 💻 Running the Application

To start the development server, run:
```bash
uvicorn main:app --reload
```
The server will be available at `http://127.0.0.1:8000`.

### 📚 API Documentation
FastAPI automatically generates an interactive API documentation interface (Swagger UI). 
- **OpenAPI / Swagger**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- *(An exported version of the Swagger configuration is also available in [`doc/EZshopBackEndApplication_swagger.yaml`](doc/EZshopBackEndApplication_swagger.yaml))*

---

## 🧪 Running Tests

To run the full test suite (Unit, Integration, and System tests):
```bash
pytest
```

To run tests with a coverage report:
```bash
pytest --cov=app tests/
```