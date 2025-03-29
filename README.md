  # 📚 LIBRARY MANAGEMENT SYSTEM

                This is a simple Java application to help manage library tasks like adding books, managing students, and tracking borrowed books.

## 🚀 Features

            Login for admin and users

            Add, edit, delete, and view books

            Manage student information

            Track book borrowing and returns

## 🛠️ Tools Used

            Java (For coding)

            MySQL (For storing data)

            JDBC (To connect Java and MySQL)

            Git and GitHub (For version control)


## 🗂️ Database Tables

***login:*** Stores user details

***books:*** Stores book information

***students:*** Stores student data

***booking_details:*** Tracks borrowed books

### 📌 Login Table
| Column Name    | Data Type      | Constraints            |
|-----------------|----------------|------------------------|
| id              | MEDIUMINT(8)   | PRIMARY KEY, AUTO_INCREMENT |
| user_name       | VARCHAR(255)   | NOT NULL               |
| user_password   | VARCHAR(100)   | NOT NULL               |
| user_type       | VARCHAR(100)   | NOT NULL               |

### 📌 Books Table
| Column Name    | Data Type      | Constraints            |
|-----------------|----------------|------------------------|
| id              | MEDIUMINT(8)   | PRIMARY KEY, AUTO_INCREMENT |
| sr_no           | INT(10)        | NOT NULL               |
| name            | VARCHAR(100)   | NOT NULL               |
| author_name     | VARCHAR(100)   | NOT NULL               |
| qty             | INT(2)         |                        |

### 📌 Students Table
| Column Name    | Data Type      | Constraints            |
|-----------------|----------------|------------------------|
| student_id      | INT(8)         | PRIMARY KEY            |
| name            | VARCHAR(100)   | NOT NULL               |
| branch          | VARCHAR(50)    | NOT NULL               |
| year            | INT(1)         | NOT NULL               |

### 📌 Booking Details Table
| Column Name    | Data Type      | Constraints            |
|-----------------|----------------|------------------------|
| booking_id      | INT(8)         | PRIMARY KEY, AUTO_INCREMENT |
| student_id      | INT(8)         | FOREIGN KEY REFERENCES students(student_id) |
| book_id         | INT(8)         | FOREIGN KEY REFERENCES books(id) |
| issue_date      | DATE           | NOT NULL               |
| return_date     | DATE           |                         |
