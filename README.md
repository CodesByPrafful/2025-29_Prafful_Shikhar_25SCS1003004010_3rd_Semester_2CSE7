# 🎓 1-Month Java Developer Internship — CodecTechnologies

Repository containing the project deliverables, source code, presentation deck, and formal academic report for the **1-Month Java Developer Internship** undertaken at **CodecTechnologies** (June 1, 2026 – July 1, 2026).

---

## 👤 Student & Academic Information

- **Student Name:** Prafful Shikhar
- **Roll Number:** `25SCS1003004010`
- **Program:** B.Tech — Computer Science & Engineering (Specialization in AI & ML)
- **Batch:** 2025–2029
- **Institute:** School of Computer Science and Engineering, IILM University, Greater Noida, U.P.
- **Internship Domain:** Enterprise Java Development

---

## 🚀 Projects Overview

### 1. Employee Management System

An enterprise-oriented web application developed to manage employee records and organizational information.

**Architecture:** Model-View-Controller (MVC)

**Key Features:**
- Full CRUD operations for employee records
- Employee information management
- Department and role management
- Employee profile management
- Search and filtering functionality
- Salary and employee detail management

**Tech Stack:** Java, Spring MVC, Hibernate ORM, MySQL

---

### 2. Student Management System

A web-based academic management application designed to manage student records and subject-wise academic performance.

**Architecture:** Spring Boot Multi-Tier Architecture

**Key Features:**
- Add, view, edit, and delete student records
- Student personal and academic information management
- Subject-wise marks management
- Automatic total marks calculation
- Automatic percentage calculation
- Automatic grade calculation
- Pass/fail result generation
- Individual student performance reports
- Printable student performance reports
- Responsive and clean user interface

**Tech Stack:** Java, Spring Boot, Spring MVC, Spring Data JPA, Hibernate, MySQL, Thymeleaf, HTML5, CSS3

---

## 🛠️ Technology Stack & Tools

| Layer / Category | Technologies & Tools |
|---|---|
| **Programming Language** | Java |
| **Frameworks** | Spring Boot, Spring MVC |
| **Persistence / ORM** | Spring Data JPA, Hibernate |
| **Database** | MySQL |
| **Frontend / Templating** | Thymeleaf, HTML5, CSS3 |
| **Build & Dependency Management** | Apache Maven |
| **Version Control** | Git |
| **Repository Hosting** | GitHub |
| **Development Environment** | Java IDE / Visual Studio Code |

---

## 🏛️ System Architecture

The projects follow a layered application architecture in which the presentation layer communicates with the controller layer, business logic is processed by the application, and data is persisted through JPA/Hibernate into MySQL.

```text
┌───────────────────────────────────────────────────────────┐
│                  PRESENTATION / VIEW LAYER                │
│             Thymeleaf, HTML5, CSS3 UI                    │
└─────────────────────────────┬─────────────────────────────┘
                              │
                              │ HTTP Requests
                              ▼
┌───────────────────────────────────────────────────────────┐
│                  CONTROLLER LAYER                         │
│              Spring MVC / Spring Boot                    │
└─────────────────────────────┬─────────────────────────────┘
                              │
                              │ Application Logic
                              ▼
┌───────────────────────────────────────────────────────────┐
│                  BUSINESS / SERVICE LAYER                 │
│              Application & Business Logic                 │
└─────────────────────────────┬─────────────────────────────┘
                              │
                              │ Data Access
                              ▼
┌───────────────────────────────────────────────────────────┐
│              DATA ACCESS / PERSISTENCE LAYER              │
│          Spring Data JPA / Hibernate ORM                  │
└─────────────────────────────┬─────────────────────────────┘
                              │
                              │ SQL / JDBC
                              ▼
┌───────────────────────────────────────────────────────────┐
│                    DATABASE LAYER                         │
│                       MySQL                               │
└───────────────────────────────────────────────────────────┘
```

---

## 📅 Internship Milestone Breakdown

### Week 1 — Java & Environment Setup

- Core Java and Object-Oriented Programming concepts
- Collections and Generics
- Development environment setup
- Maven project configuration
- Introduction to Spring Framework
- Dependency Injection and basic Spring concepts

### Week 2 — Employee Management System

- Database and entity design
- Hibernate ORM configuration
- Entity mapping using JPA annotations
- Spring MVC controller development
- CRUD implementation
- MySQL database integration

### Week 3 — Student Management System

- Spring Boot project setup
- Spring Data JPA repository implementation
- Student and subject entity relationships
- CRUD functionality
- Subject-wise marks management
- Performance and grade calculation logic

### Week 4 — UI, Testing & Documentation

- Thymeleaf server-side UI integration
- HTML5 and CSS3 styling
- Responsive interface development
- Input handling and validation
- Git version control
- GitHub repository management
- Project documentation
- Internship report and presentation preparation

---

## 📂 Repository Structure

```text
├── documentation/
│   ├── Internship_Report.pdf
│   ├── Presentation_Deck.pdf
│   └── Completion_Certificate.pdf
│
└── README.md
```

---

## 👨‍🎓 Student Management System

The Student Management System provides complete functionality for maintaining student records and academic performance.

### Student Details

Each student record contains:

- Student ID
- Name
- Email
- Course

### Subject Marks

Each subject record contains:

- Subject ID
- Subject Name
- Marks
- Associated Student

### Entity Relationship

The application uses a **One-to-Many** relationship between `Student` and `SubjectMarks`.

```text
Student
   │
   ├── SubjectMarks
   ├── SubjectMarks
   └── SubjectMarks
```

The relationship is implemented using JPA annotations.

**Student.java**

```java
@OneToMany(
    mappedBy = "student",
    cascade = CascadeType.ALL,
    orphanRemoval = true
)
private List<SubjectMarks> subjects = new ArrayList<>();
```

**SubjectMarks.java**

```java
@ManyToOne
private Student student;
```

---

## 📊 Student Performance Calculation

The Student Management System automatically calculates academic performance from the marks entered for each subject.

### Total Marks

Total marks are calculated by adding the marks obtained in all subjects.

### Percentage

The percentage is calculated based on the average marks across all subjects.

For example:

```text
Mathematics: 85
Java:        90
Database:    80

Total Marks = 255 / 300
Percentage  = 85%
```

---

## 🏆 Grading System

| Percentage | Grade | Result | Performance |
|---|---|---|---|
| 90% and above | A+ | PASS | Outstanding |
| 80% – 89% | A | PASS | Excellent |
| 70% – 79% | B | PASS | Very Good |
| 60% – 69% | C | PASS | Good |
| 50% – 59% | D | PASS | Average |
| Below 50% | F | FAIL | Needs Improvement |

---

## 🔄 CRUD Operations

Both projects demonstrate CRUD-based application functionality.

### Create

Users can create new records by entering the required information.

### Read

The applications display stored records from the MySQL database.

### Update

Users can edit existing records and save the updated information.

### Delete

Users can remove existing records from the system.

---

## 📄 Student Performance Report

The Student Management System includes an individual performance report for each student.

The report displays:

- Student ID
- Full Name
- Email
- Course
- Subject-wise marks
- Total marks
- Percentage
- Grade
- Result
- Overall performance

The report also provides a **Print Report** option for generating a printable version of the performance report.

---

## 🗄️ Database Configuration

The applications use **MySQL** for persistent data storage.

Create the required database using:

```sql
CREATE DATABASE student_management;
```

Database configuration is stored in:

```text
src/main/resources/application.properties
```

Example configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_management
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

spring.thymeleaf.cache=false
```

Replace `YOUR_PASSWORD` with your local MySQL password.

> **Note:** Never commit real database passwords or other sensitive credentials to GitHub.

---

## ⚙️ How to Run Locally

### Prerequisites

Make sure the following are installed:

- Java JDK
- MySQL Server
- Git
- A Java IDE such as IntelliJ IDEA, Eclipse, Spring Tool Suite, or VS Code

Maven does not need to be installed separately if using the included Maven Wrapper.

---

### 1. Clone the Repository

```bash
git clone https://github.com/CodesByPrafful/Student-Management-System.git
```

Then enter the project directory:

```bash
cd Student-Management-System
```

---

### 2. Create the Database

Open MySQL and run:

```sql
CREATE DATABASE student_management;
```

---

### 3. Configure Database Credentials

Open:

```text
src/main/resources/application.properties
```

Update the following values according to your local MySQL configuration:

```properties
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
```

---

### 4. Run the Application

On Windows:

```powershell
.\mvnw.cmd spring-boot:run
```

On Linux/macOS:

```bash
./mvnw spring-boot:run
```

The application can also be started directly from the main Spring Boot application class in the IDE.

---

### 5. Open the Application

Once the application starts successfully, open:

```text
http://localhost:8080
```

---

## 🌐 Student Management System Pages

### Student Dashboard

Displays all registered students and provides options to:

- Edit student
- Delete student
- Generate performance report

### Add Student

Allows users to create a new student record.

### Edit Student

Allows users to update an existing student's information.

### Student Report

Displays detailed academic performance for an individual student.

---

## 🎨 User Interface

The applications use server-side rendered Thymeleaf templates along with HTML5 and CSS3.

The Student Management System includes:

- Clean dashboard layout
- Student information cards
- Add student form
- Edit student form
- Subject marks display
- Performance report layout
- Responsive design
- Print-friendly report layout

---

## 🧠 Skills Demonstrated

This internship provided practical experience in:

- Java programming
- Object-Oriented Programming
- Spring Boot
- Spring MVC
- Dependency Injection
- Spring Data JPA
- Hibernate ORM
- MySQL database integration
- CRUD operations
- One-to-Many relationships
- Many-to-One relationships
- Thymeleaf
- HTML5
- CSS3
- MVC architecture
- Form handling
- Server-side rendering
- Maven
- Git
- GitHub

---

## 🎯 Internship Outcomes

The internship resulted in the successful development and documentation of two Java-based management applications:

1. **Employee Management System**
2. **Student Management System**

The projects provided practical exposure to backend development, database integration, web application development, MVC architecture, ORM, CRUD operations, and server-side UI development.

---

## 🔮 Future Improvements

Possible future improvements include:

- User authentication
- Admin and user roles
- Student search
- Pagination
- Attendance management
- Semester management
- PDF report generation
- Performance charts
- Student ranking
- Email-based reports
- Dashboard statistics
- Cloud deployment

---

## 📌 Project Status

**Completed**

The internship deliverables include:

- Employee Management System
- Student Management System
- CRUD functionality
- MySQL database integration
- Subject-wise marks management
- Performance calculation
- Grade calculation
- Student performance reports
- Printable reports
- Responsive web interface
- GitHub repository
- Internship documentation
- Presentation deck

---

## 👨‍💻 Author

**Prafful Shikhar**

B.Tech — Computer Science & Engineering  
Specialization in Artificial Intelligence & Machine Learning  
IILM University, Greater Noida

**GitHub:**  
https://github.com/CodesByPrafful

---

## 📜 Acknowledgements

I would like to express my sincere gratitude to **CodecTechnologies** for providing me with the opportunity to undertake this Java Developer Internship and gain practical experience in Java-based application development.

I would also like to thank the **School of Computer Science and Engineering, IILM University, Greater Noida** for providing academic support and guidance throughout the internship.

---

## 📚 References

- Spring Boot Documentation — https://spring.io/projects/spring-boot
- Spring Framework Documentation — https://spring.io/projects/spring-framework
- Hibernate ORM Documentation — https://hibernate.org/orm/
- Thymeleaf Documentation — https://www.thymeleaf.org/
- MySQL Documentation — https://dev.mysql.com/doc/
- Java Documentation — https://docs.oracle.com/en/java/

---
