# Library Management System

A robust Library Management System designed to manage books, members, staff, and transactions efficiently. This project demonstrates the use of Oracle SQL and PL/SQL to handle various library operations, including book borrowing, returning, and fine management.

## Features

- **Book Management**: Add, update, and manage books with details like title, author, genre, publisher, and publication date.
- **Member Management**: Track member information, including name, contact details, and membership status.
- **Staff Management**: Manage staff details and roles.
- **Transaction Management**: Handle book borrowing and returning with automated due date and late charge calculations.
- **Fine Management**: Calculate, track, and process fines for overdue books.
- **Triggers and Stored Procedures**: Ensure data consistency and automate operations.

## Technologies Used

- **Database**: Oracle SQL
- **Languages**: PL/SQL
- **Tools**: SQL Developer, ER Diagram Tools

## Project Structure

- **SQL Scripts**: Contains scripts for creating tables, stored procedures, triggers, and sample data.
- **Documentation**: Includes this README file and diagrams for understanding the database structure and workflows.

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/LibraryManagementSystem.git
   ```
2. Import the SQL scripts into your Oracle database using SQL Developer or any preferred tool.
3. Execute the scripts in the following order:
   - Table creation scripts
   - Trigger scripts
   - Stored procedure scripts
   - Sample data population scripts
4. Use SQL queries or applications to interact with the system.

## Database Schema Overview

### Tables

1. **Books**: Stores book information.
2. **Authors**: Details about authors.
3. **Members**: Member information and membership status.
4. **Staffs**: Details of library staff.
5. **Transactions**: Tracks book borrowing and returning.

### Key Columns

- **Books Table**: `book_id`, `title`, `author_id`, `genre`, `publisher`
- **Members Table**: `member_id`, `first_name`, `last_name`, `email`, `membership_status`
- **Transactions Table**: `transaction_id`, `book_due_date`, `late_charge_due`, `payment_mode`

### Relationships

- **Books** are associated with **Authors** via `author_id`.
- **Transactions** link **Books**, **Members**, and optionally **Staffs**.

## Example Queries

- **View all overdue books**:
  ```sql
  SELECT *
  FROM Transactions
  WHERE book_due_date < SYSDATE AND status = 'borrowed';
  ```

## Screenshots and Diagrams

![ER Diagram](path/to/er-diagram.png)

## License

This project is open-source.

## Contact

For queries or suggestions, reach out to me at:

- Email: saurav.com23456@gmail.com
- GitHub: [Sorvi007](https://github.com/Sorvi007)

