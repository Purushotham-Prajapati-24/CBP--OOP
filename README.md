# Console-based Personal Expense Tracker

A Java-based command-line application for tracking personal expenses with user authentication, category management, and comprehensive reporting features.

## Project Overview

This Expense Tracker application is designed to help users manage their personal finances by tracking expenses, organizing them by categories, and generating detailed reports. The application uses a database backend to persist user and expense data securely.

## Features

- **User Authentication**: User login and account management
- **Expense Management**: Add, view, and manage personal expenses
- **Category Management**: Organize expenses by custom categories
- **Database Integration**: Persistent storage of user and expense data
- **Reporting**: Generate expense reports and view totals by category
- **Console Interface**: Easy-to-use command-line interface for all operations

## Architecture

### Core Components

#### Model Classes
- **`User.class`**: Represents user entities with authentication credentials
- **`Expense.class`**: Represents individual expense records
- **`Category.class`**: Represents expense categories for organization
- **`Report.class`**: Represents generated expense reports
- **`TotalByReport.class`**: Aggregates total expenses for reporting

#### Data Access Objects (DAO)
- **`UserDAO.class`**: Handles user data persistence and retrieval
- **`ExpenseDAO.class`**: Manages expense data operations
- **`CategoryDAO.class`**: Manages category data operations

#### Database & View
- **`DBConnection.class`**: Manages database connectivity and connections
- **`ExpenseView.class`**: Handles user interface and console interactions

#### Main Entry Point
- **`Main.class`**: Application entry point and main control flow

## Technical Stack

- **Language**: Java
- **Database**: SQL-based (configured via DBConnection)
- **Architecture Pattern**: DAO (Data Access Object) Pattern
- **User Interface**: Console-based CLI

## Getting Started

### Prerequisites
- Java Runtime Environment (JRE) 8 or higher
- Database server (MySQL, PostgreSQL, or similar as configured)
- Database credentials and connection parameters

### Installation

1. Clone the repository:
   ```
   git clone <repository-url>
   cd ExpenseTracker
   ```

2. Compile the Java source files (if source is available):
   ```
   javac *.java
   ```

3. Configure your database connection in `DBConnection.class`

4. Run the application:
   ```
   java Main
   ```

## Usage

### Main Menu Options
1. **User Management**: Register or login to your account
2. **Manage Expenses**: Add new expenses or view existing ones
3. **Manage Categories**: Create and organize expense categories
4. **View Reports**: Generate and view expense reports
5. **Exit**: Close the application

### Example Workflow
```
1. Launch the application
2. Login or create a new user account
3. Create expense categories (e.g., Food, Transport, Entertainment)
4. Add expenses under appropriate categories
5. Generate reports to view spending patterns
```

## Database Schema

The application uses the following main entities:

- **Users Table**: Stores user credentials and authentication information
- **Expenses Table**: Records individual transactions with amount, date, and category
- **Categories Table**: Manages expense categories for organization
- **Reports Table**: Stores generated report summaries

## Class Relationships

```
Main
 ├── ExpenseView (UI/Console Interface)
 ├── User + UserDAO
 ├── Expense + ExpenseDAO
 ├── Category + CategoryDAO
 ├── Report + TotalByReport
 └── DBConnection (Database Management)
```

## Code Structure

- **DAO Pattern**: Each entity (User, Expense, Category) has a corresponding DAO class for database operations
- **Separation of Concerns**: Model classes handle data, DAO classes handle persistence, View class handles UI
- **Database Abstraction**: DBConnection class centralizes all database operations

## Future Enhancements

- Graphical User Interface (GUI) using Swing or JavaFX
- Data export functionality (CSV, PDF)
- Advanced filtering and search capabilities
- Multi-currency support
- Budget tracking and alerts
- Data visualization and charts

