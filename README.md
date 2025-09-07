* Project overview
* Features
* Tech stack
* Installation & setup instructions
* Database setup
* Usage guide
* Folder structure
* Contribution guidelines


# Webknot Event Reporting

##  Overview

The **Webknot Event Reporting System** is a web-based platform designed to manage, track, and report events efficiently. It provides separate portals for students and administrators to streamline event participation, reporting, and management.

This project is structured for scalability, maintainability, and ease of deployment.

---

##  Features

 **User Authentication** (via environment-based secrets)
 **Student Portal** – register and view events
 **Admin Portal** – create, update, and manage events
 **Reports Module** – generate SQL-based event reports
 **Database Integration** with schema migrations
 **Clean UI Wireframes** for Student & Admin workflows

---

## Tech Stack

* **Backend:** Python (Flask / FastAPI – based on `app.py`)
* **Database:** SQLite / PostgreSQL (configurable)
* **Frontend:** HTML/CSS/JS (basic templates)
* **Other:** SQL scripts for schema & reporting

---

##  Installation & Setup

### Clone the Repository

```bash
git clone http://github.com/Rakshithagowda123/webknot-event-reporting.git
cd webknot_event_reporting
```

###  Create Virtual Environment & Install Dependencies

```bash
python -m venv venv
source venv/bin/activate   # for Linux/Mac
venv\Scripts\activate      # for Windows

pip install -r requirements.txt
```

### Configure Environment Variables

Copy `.env.example` to `.env` and update values:

```bash
cp .env.example .env
```

Update database URL, secret keys, etc.

###  Initialize Database

```bash
python db_init.py
```

or run:

```bash
sqlite3 database.db < schema.sql
```

###  Run the Application

```bash
python app.py
```

Now visit: `http://127.0.0.1:5000/`

---

## Folder Structure

```
webknot_event_reporting/
│── app.py                  # Main application
│── models.py               # Database models
│── db_init.py              # DB initialization
│── schema.sql              # Database schema
│── reports.sql             # SQL queries for reporting
│── requirements.txt        # Python dependencies
│── .env.example            # Env variables template
│
├── design/
│   └── Design_Document.md  # System design document
│
├── mockups/
│   ├── Student_App_Wireframe.md
│   └── Admin_Portal_Wireframe.md
│
├── README.md               # Project documentation
└── QUICKSTART.md           # Quick setup guide
```



##  Database

* The schema is defined in **schema.sql**
* Example reports available in **reports.sql**
* Supports migration for relational databases



##  Contribution

1. Fork the repository
2. Create a new branch (`feature/new-module`)
3. Commit changes (`git commit -m "Add new module"`)
4. Push to branch (`git push origin feature/new-module`)
5. Open a Pull Request
