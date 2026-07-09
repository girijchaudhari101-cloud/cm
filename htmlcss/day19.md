# Python Backend Setup Completed

Python is a high-level programming language used for backend development. A Python backend project was created and configured successfully. The required project structure, virtual environment, and project files were set up for developing APIs and connecting with a database.

Work Completed:-

1.Created a new folder for the Python backend project.

2.Created a virtual environment using:-
    python -m venv venv

3.Activated the virtual environment.

4.Installed the required Python packages and dependencies using pip.

5.Generated the `requirements.txt` file to store all the installed project dependencies.

6.Created the main application file:-
    main.py

7.Created the database configuration file:-
    database.py

8.Created the models file:-
    models.py

9.Created the schemas file:-
    schemas.py

10.Verified that the project structure was created successfully.

11.The `__pycache__` folder was generated automatically to store compiled Python bytecode files.

12.The Python backend setup was completed successfully and is now ready for API development and database integration.

Project Structure:-

    backend/
    │
    ├── __pycache__/
    ├── venv/
    ├── database.py
    ├── main.py
    ├── models.py
    ├── schemas.py
    └── requirements.txt

Files Description:-

1.__pycache__
    - Stores compiled Python bytecode files.
    - Created automatically by Python to improve execution speed.

2.venv
    - Virtual environment for the project.
    - Contains project-specific Python packages and dependencies.

3.database.py
    - Contains the database connection and configuration code.
    - Used to connect the backend with the database.

4.main.py
    - Main entry point of the backend application.
    - Used to start the server and define API endpoints.

5.models.py
    - Defines the database models (tables).
    - Represents the structure of data stored in the database.

6.schemas.py
    - Defines request and response data schemas.
    - Used for data validation and serialization.

7.requirements.txt
    - Lists all the Python packages required for the project.
    - Used to install dependencies using:
      `pip install -r requirements.txt`


# PostgreSQL Setup Completed

PostgreSQL is an open-source Relational Database Management System (RDBMS) used to store, retrieve, and manage application data. PostgreSQL and pgAdmin 4 were installed successfully and configured for backend database development.

Work Completed:-

1.Downloaded and installed PostgreSQL 18.

2.Installed pgAdmin 4 for managing PostgreSQL databases through a graphical interface.

3.Configured the PostgreSQL server during installation.

4.Set the password for the PostgreSQL superuser (postgres).

5.Connected to the PostgreSQL server using pgAdmin 4.

6.Created a new database named:-
    todo

7.Created a table named:-
    todos

8.Created the following columns in the `todos` table:-
    - id
    - title
    - description
    - completed

9.Opened the Query Tool to execute SQL queries.

10.Executed the following query to display all records from the table:-

    SELECT * FROM public.todos
    ORDER BY id ASC;

11.Verified that the table data was displayed successfully.

12.The PostgreSQL database setup was completed successfully and is ready for backend integration.

Project Structure:-

    PostgreSQL 18
    │
    ├── Database
    │     └── todo
    │
    ├── Schema
    │     └── public
    │
    └── Table
          └── todos

Components Description:-

1.PostgreSQL Server
    - Stores and manages the application database.

2.pgAdmin 4
    - Graphical interface used to create and manage databases, tables, and execute SQL queries.

3.Database (todo)
    - Stores all the data related to the Todo application.

4.Table (todos)
    - Stores the task information in the database.

5.Query Tool
    - Used to write and execute SQL commands.

6.Columns
    - id : Unique identifier for each task.
    - title : Stores the task title.
    - description : Stores the task description.
    - completed : Stores the task completion status (True/False).

Outcome:-
Successfully completed the PostgreSQL installation and database setup. Created the `todo` database and `todos` table, executed SQL queries using the Query Tool, and verified that the data was stored and retrieved successfully.

