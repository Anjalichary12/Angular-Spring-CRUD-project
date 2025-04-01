# Angular-Spring-CRUD-project

Here’s a sample **README** file content for your project, outlining the backend, frontend, and database details:

---

# **Employee Management System**

This is a simple **Employee Management System** that allows the creation of employee records, including basic details such as **First Name**, **Last Name**, and **Email ID**. It is built using the following technologies:

- **Backend**: Spring Boot
- **Frontend**: Visual Studio Code (VS Code), HTML, CSS, Angular
- **Database**: MySQL

---

## **Table of Contents**
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database Setup](#database-setup)
- [Contributing](#contributing)
- [License](#license)

---

## **Technologies Used**
- **Backend**: 
  - Spring Boot (Java)
  - REST API
  
- **Frontend**: 
  - Angular
  - HTML, CSS (for UI styling)
  - Bootstrap (for responsive design)
  
- **Database**: 
  - MySQL

---

## **Installation**

### Backend (Spring Boot)
1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/your-username/employee-management-system.git
   cd employee-management-system
   ```

2. Ensure you have **JDK 8+** installed and the **Maven** tool set up on your machine.

3. Open the project in your preferred IDE (e.g., IntelliJ IDEA, Eclipse).

4. Build the project:
   ```bash
   mvn clean install
   ```

5. Run the Spring Boot application:
   ```bash
   mvn spring-boot:run
   ```

6. By default, the backend server will run on `http://localhost:8080`.

---

### Frontend (Angular)
1. Install **Node.js** and **Angular CLI** if not already installed.
   
2. Navigate to the `frontend` directory and install dependencies:
   ```bash
   cd frontend
   npm install
   ```

3. Start the Angular development server:
   ```bash
   ng serve
   ```

4. The frontend will be available at `http://localhost:4200`.

---

## **Setup Instructions**

1. **Create MySQL Database**: 
   Set up a MySQL database with the following configuration:
   ```sql
   CREATE DATABASE employee_db;
   ```

2. **Configure Database Connection**:
   Update the `application.properties` file in the Spring Boot backend (`src/main/resources/application.properties`) with your MySQL credentials:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/employee_db
   spring.datasource.username=your-username
   spring.datasource.password=your-password
   spring.jpa.hibernate.ddl-auto=update
   ```

---

## **Usage**

- The user can create a new employee by entering **First Name**, **Last Name**, and **Email ID** in the form available in the UI.
- The backend will process this information, save it to the MySQL database, and return a response.

---

## **API Endpoints**

### **1. Create Employee**
- **Endpoint**: `/api/employees`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "firstName": "John",
    "lastName": "Doe",
    "emailId": "john.doe@example.com"
  }
  ```
- **Response**: 
  - Success: 201 Created
  - Error: 400 Bad Request (if any field is missing or invalid)

### **2. Get Employee List**
- **Endpoint**: `/api/employees`
- **Method**: `GET`
- **Response**:
  ```json
  [
    {
      "id": 1,
      "firstName": "John",
      "lastName": "Doe",
      "emailId": "john.doe@example.com"
    }
  ]
  ```

---

## **Database Setup**

1. **Table Structure**:
   - **Employee Table**: Stores employee details.
   ```sql
   CREATE TABLE employees (
     id INT AUTO_INCREMENT PRIMARY KEY,
     first_name VARCHAR(100) NOT NULL,
     last_name VARCHAR(100),
     email_id VARCHAR(100) UNIQUE NOT NULL
   );
   ```

2. **Ensure MySQL server is running** and the `employee_db` database is created.

---

## **Contributing**

If you would like to contribute to this project:

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Create a new Pull Request.

---

## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### **Final Notes:**
- This project is meant for learning purposes and demonstrates a simple employee management system.
- Future improvements include adding authentication, CRUD functionality for all employees, and front-end validation.

---

Feel free to adapt or add more details specific to your project setup! 🚀
