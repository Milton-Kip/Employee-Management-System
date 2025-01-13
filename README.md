# Employee Management System - Admin Panel

Welcome to the **Employee Management System - Admin Panel** repository! This project is a Java Swing-based desktop application with MySQL database integration. It enables administrators to manage employee records efficiently, including adding, updating, and deleting employee details.

---

## Features

- **Add Employees:** Register new employees with details like name, contact info, position, department, and status.
- **Update Employees:** Modify the details of existing employees.
- **Delete Employees:** Remove employees from the system.
- **View Employees:** Display a list of employees filtered by their status.
- **User-friendly Interface:** Swing-based GUI for ease of use.

---

## Prerequisites

### Software Requirements
- **Java Development Kit (JDK):** Version 17 or later (Tested on JDK 21).
- **Apache Maven:** For building the project.
- **MySQL Server:** For database management.
- **NetBeans IDE:** Recommended for development.

### Libraries Used
- **MySQL JDBC Driver:** Ensure the MySQL connector JAR is included in your project.

---

## Project Setup

1. **Clone the Repository:**
   ```
   git clone https://github.com/<your-username>/employee-management-system.git
   cd employee-management-system
   ```

2. **Set Up the Database:**
   - Create a MySQL database named `employee_management`.
   - Run the following SQL script to set up the `employees` table:
     ```sql
     CREATE TABLE employees (
         id INT AUTO_INCREMENT PRIMARY KEY,
         full_name VARCHAR(255) NOT NULL,
         contact_info VARCHAR(255),
         position VARCHAR(255),
         department VARCHAR(255),
         status VARCHAR(50)
     );
     ```

3. **Configure Database Connection:**
   - Update the database connection details in `DatabaseConnection.java`:
     ```java
     private static final String DB_URL = "jdbc:mysql://localhost:3306/employee_management";
     private static final String DB_USER = "root";
     private static final String DB_PASSWORD = "<your-password>";
     ```

4. **Build the Project:**
   ```
   mvn clean install
   ```

5. **Run the Application:**
   ```
   mvn exec:java -Dexec.mainClass=com.mycompany.adminpanel.AdminPanel
   ```

---

## Project Structure

```
.
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.mycompany.adminpanel
│   │   │       ├── AdminPanel.java        # Main GUI class
│   │   │       ├── DatabaseConnection.java # Handles DB connectivity
│   │   │       ├── Employee.java           # Employee model
│   │   │       └── EmployeeDAO.java        # Data Access Object for employees
│   └── test                               # Test classes (if any)
├── pom.xml                               # Maven configuration
└── README.md                             # Project documentation
```

---

## Usage

- Launch the application.
- Use the input fields to add or update employee details.
- View the list of employees in the text area, filtered by their status.
- Delete employees as needed.

---

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

1. Fork the repository.
2. Create a new branch:
   ```
   git checkout -b feature-name
   ```
3. Make your changes and commit them:
   ```
   git commit -m "Add your message here"
   ```
4. Push to your fork:
   ```
   git push origin feature-name
   ```
5. Open a pull request on the original repository.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Contact

For any questions or feedback, feel free to contact the author:

**Author:** Kipyegon M

- Email: <kipyegonmilton@gmail.com>

Thank you for checking out the Employee Management System!
