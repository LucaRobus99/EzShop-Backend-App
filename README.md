# EzShop Backend App 🛒

EzShop is a backend application designed to manage retail store operations, built as a project for the Software Engineering 1 (SE1) course at Politecnico di Torino. 

It provides a comprehensive RESTful API for handling users, products, sales, returns, customer loyalty cards, and orders, following an MVC (Model-View-Controller) architectural pattern.

## 🌟 Features
- **User Management & Auth**: Roles, authentication with JWT, user balances.
- **Product & Inventory**: Catalog management, tracking quantities and physical positions.
- **Sales & Transactions**: Checkout process, line items, and payment processing.
- **Returns**: Managing product returns tied to specific sales.
- **Orders**: Purchasing new stock and updating inventory.
- **Customers & Loyalty Cards**: Customer tracking, loyalty points, and discounts.

## 🛠 Tech Stack
- **Framework**: [FastAPI](https://fastapi.tiangolo.com/)
- **Database**: SQLite (via `aiosqlite`) with [SQLAlchemy](https://www.sqlalchemy.org/) ORM
- **Authentication**: JWT (`PyJWT`)
- **Testing**: `pytest`, `pytest-asyncio`, `pytest-cov`

## 🚀 Setup & Installation

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
   
   # On Linux/macOS:
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

## 💻 Running the Application

To start the development server, run:
```bash
uvicorn main:app --reload
```
The server will be available at `http://127.0.0.1:8000`.

### 📚 API Documentation
FastAPI automatically generates interactive API documentation. Once the server is running, you can access:
- **Swagger UI**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- **ReDoc**: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

## 🧪 Running Tests

To run the full test suite (Unit, Integration, and System tests):
```bash
pytest
```

To run tests with a coverage report:
```bash
pytest --cov=app tests/
```