```markdown
# 1-Month Java Developer Internship — CodecTechnologies

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.java.com/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white)](https://hibernate.org/)
[![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=for-the-badge&logo=thymeleaf&logoColor=white)](https://www.thymeleaf.org/)

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
An enterprise-grade web application designed to handle workforce records, departmental mappings, and role-based permissions with transactional integrity.
- **Architecture:** Model-View-Controller (MVC)
- **Key Features:**
  - Full CRUD operations for employee records.
  - Role-Based Access Control (Admin / Manager / Employee).
  - Departmental mapping, salary updates, and profile searching/filtering.
- **Tech Stack:** Java, Spring MVC, Hibernate ORM, MySQL.

### 2. Student Management System
A dynamic academic tracking portal designed to automate student profile management, course enrollment, and performance computation.
- **Architecture:** Spring Boot Multi-Tier Architecture
- **Key Features:**
  - Dynamic CRUD for student personal and academic details.
  - Real-time semester marks entry and automated GPA / grade aggregation.
  - Printable report card generation and responsive UI dashboards.
- **Tech Stack:** Java, Spring Boot, Spring Data JPA, MySQL, Thymeleaf, HTML5/CSS3.

---

## 🛠️ Technology Stack & Tools

| Layer / Category | Technologies & Tools |
| :--- | :--- |
| **Core Language** | Java (JDK 17 / JDK 21) |
| **Frameworks** | Spring Boot, Spring MVC, Spring Data JPA |
| **Persistence / ORM** | Hibernate ORM, JDBC API |
| **Database** | MySQL Server 8.0, MySQL Workbench |
| **Frontend / Templating** | Thymeleaf, HTML5, CSS3, JavaScript |
| **Build & Dependency Tool** | Apache Maven |
| **Version Control** | Git, GitHub |
| **IDEs Used** | IntelliJ IDEA / Eclipse / VS Code |

---

## 🏛️ System Architecture

The projects follow a decoupled **5-Layer Architecture**:

```text
┌───────────────────────────────────────────────────────────┐
│               PRESENTATION / VIEW LAYER                   │
│        (Thymeleaf Templates, HTML5, CSS3 UI)              │
└─────────────────────────────┬─────────────────────────────┘
                              │ HTTP Requests
┌─────────────────────────────▼─────────────────────────────┐
│                 CONTROLLER / ROUTING LAYER                │
│         (Spring MVC & Spring Boot Web Controllers)        │
└─────────────────────────────┬─────────────────────────────┘
                              │ Service Invocations & DTOs
┌─────────────────────────────▼─────────────────────────────┐
│                  SERVICE / BUSINESS LAYER                 │
│   (Business Rules, Validations, RBAC Security, Logic)     │
└─────────────────────────────┬─────────────────────────────┘
                              │ Entity Transactions
┌─────────────────────────────▼─────────────────────────────┐
│              DATA ACCESS / PERSISTENCE LAYER              │
│       (Spring Data JPA Repositories / Hibernate ORM)      │
└─────────────────────────────┬─────────────────────────────┘
                              │ JDBC Queries
┌─────────────────────────────▼─────────────────────────────┐
│                 DATABASE / STORAGE LAYER                  │
│               (MySQL Relational Database)                 │
└───────────────────────────────────────────────────────────┘

```

---

## 📅 4-Week Milestone Breakdown

* **Week 1:** Core Java OOP Refinement (Collections, Streams, Generics), Environment Setup, Maven configuration, Spring Core (IoC & DI).
* **Week 2:** *Employee Management System* schema design, Hibernate entity mappings (`@Entity`, `@Table`, `@Id`), Spring MVC controller routing, and CRUD implementation.
* **Week 3:** *Student Management System* setup via Spring Boot, Spring Data JPA repositories, derived queries, and grade computation business logic.
* **Week 4:** Thymeleaf server-side UI integration, responsive styling (CSS3), input validation, unit testing, Git versioning, and documentation.

---

## 📂 Repository Structure

```text
├── employee-management-system/    # Spring MVC + Hibernate Project Source Code
├── student-management-system/     # Spring Boot + JPA + Thymeleaf Project Source Code
├── documentation/
│   ├── Internship_Report.pdf      # Complete Academic Report (IILM University Format)
│   ├── Presentation_Deck.html     # Slide Deck Presentation
│   ├── Offer_Letter.pdf           # Official CodecTechnologies Offer Letter
│   └── Completion_Certificate.pdf # CodecTechnologies Certificate of Completion
└── README.md

```

---

## ⚙️ How to Run Locally

### Prerequisites

* JDK 17 or higher installed
* Apache Maven installed
* MySQL Server 8.0+ running locally

### Steps

1. **Clone the repository:**
```bash
git clone [https://github.com/](https://github.com/)<your-username>/<your-repo-name>.git
cd <your-repo-name>

```


2. **Configure Database:**
Update database credentials in `src/main/resources/application.properties` (or `hibernate.cfg.xml`):
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_db?useSSL=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update

```


3. **Build and Run:**
```bash
mvn clean install
mvn spring-boot:run

```


4. **Access Applications:**
* Student Management System: `http://localhost:8080/students`
* Employee Management System: `http://localhost:8080/employees`



---

## 📜 Acknowledgements & References

* **CodecTechnologies** for structured mentorship and practical training.
* **School of Computer Science & Engineering, IILM University, Greater Noida** for institutional support.
* [Spring Boot Official Documentation](https://spring.io/projects/spring-boot)
* [Hibernate ORM Documentation](https://hibernate.org/orm/)
* [Thymeleaf Guides](https://www.thymeleaf.org/)

```

```
