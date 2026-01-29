CC Lab-2: Event Management System
Student Roll Number: PES1UG23CS715

Overview
A FastAPI-based web application for event management with user registration, event booking, and checkout functionality. Includes load testing capabilities using Locust.

Features
User Authentication: Register and login functionality
Event Management: Browse and register for events
Checkout System: Event registration checkout process
Database: SQLite database for storing users, events, and registrations
Load Testing: Locust test suites for performance testing
Project Structure
CC Lab-2/
├── main.py                  # Main FastAPI application
├── database.py              # Database connection and utilities
├── insert_events.py         # Script to populate event database
├── requirements.txt         # Python dependencies
├── checkout/                # Checkout module
├── locust/                  # Load testing files
│   ├── checkout_locustfile.py
│   ├── events_locustfile.py
│   ├── myevents_locustfile.py
│   └── journey_locustfile.py
└── templates/               # HTML templates
    ├── base.html
    ├── login.html
    ├── register.html
    ├── events.html
    ├── checkout.html
    ├── my_events.html
    └── error.html
Installation
Clone the repository:
git clone https://github.com/Yashas-199/CC_LAB2.git
cd CC_LAB2/CC\ Lab-2
Install dependencies:
pip install -r requirements.txt
Populate the database with sample events:
python insert_events.py
Usage
Running the Application
uvicorn main:app --reload
The application will be available at http://localhost:8000

Running Load Tests
# Navigate to locust directory
cd locust

# Run a specific test
locust -f events_locustfile.py
Access Locust web interface at http://localhost:8089

API Endpoints
GET /register - User registration page
POST /register - Register a new user
GET /login - Login page
POST /login - User login
GET /events - View all events
GET /my_events - View registered events
POST /checkout - Checkout and register for an event
Technologies Used
FastAPI - Modern web framework for building APIs
Jinja2 - Template engine for HTML rendering
SQLite - Lightweight database
Locust - Load testing framework
Uvicorn - ASGI server
Author
Yashas Krishna (PES1UG23CS715)

License
This is an academic project for Cloud Computing Lab.
