# Library Management Database

A SQL-based library management system built with SQLite and Jupyter Notebook to organize library resources, manage borrowing records, track fines, and coordinate library events.

## Overview

This project demonstrates how a relational database can be designed and populated to support the operations of a library. It uses SQL to define database tables, establish relationships between entities, and insert sample records for testing and demonstration.

## Features

* **Item Management:** Store library resources, including books, movies, CDs, and magazines, along with their authors, genres, formats, and availability status.
* **User Management:** Maintain user records and contact information.
* **Borrowing Records:** Track borrowed items, borrowing dates, due dates, return dates, and fines.
* **Event Management:** Store library events, descriptions, schedules, and target audiences.
* **Personnel Management:** Maintain staff records and associate personnel with organized events.
* **Event Invitations:** Record which users are invited to library events.
* **Collection Proposals:** Store suggestions for new library materials and resources.

## Database Schema

The database contains the following tables:

| Table          | Purpose                                              |
| -------------- | ---------------------------------------------------- |
| `Item`         | Stores library resources and availability.           |
| `User`         | Stores library user information.                     |
| `Borrowing`    | Tracks item loans, due dates, returns, and fines.    |
| `Event`        | Stores library events and their details.             |
| `Personnel`    | Stores staff information.                            |
| `Organised`    | Links personnel to the events they organize.         |
| `Invited`      | Links users to events they are invited to.           |
| `ProposedItem` | Stores proposed additions to the library collection. |

Primary keys identify individual records, while foreign keys establish relationships between related tables.

## Technologies Used

* **SQL** – Database definition and data manipulation.
* **SQLite** – Relational database engine.
* **Python** – Notebook environment for executing SQL commands.
* **Jupyter Notebook** – Interactive development environment.
* **ipython-sql** – Executes SQL directly within notebook cells.

## Getting Started

### Prerequisites

Install Python 3 and ensure that `pip` is available.

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

Replace the placeholders with your GitHub repository URL and folder name.

### 2. Create a virtual environment (recommended)

**Windows:**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS/Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install jupyter ipython-sql sqlalchemy
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `MiniProj.ipynb` in the Jupyter interface.

### 5. Run the notebook

Execute the cells in order to initialize the SQL extension, connect to the SQLite database, create the tables, and populate them with sample data.

The notebook creates a local database file named `library.db`.

## Project Structure

```text
.
├── MiniProj.ipynb   # Database schema and sample data
├── library.db      # SQLite database generated at runtime
└── README.md       # Project documentation
```

`library.db` is generated when the notebook is executed and does not need to be committed if you prefer to keep generated database files out of version control.

## Future Improvements

* Add SQL queries for searching and filtering library resources.
* Implement reports for overdue items and outstanding fines.
* Add validation for borrowing and returning items.
* Develop a user interface for library staff and members.
* Expand the database with additional constraints and automated business rules.

## Learning Objectives

This project provides practical experience with relational database design, SQL table creation, primary and foreign keys, data insertion, and managing relationships between multiple entities.
