EMPLOYEE MANAGEMENT SYSTEM


A Spring Boot based Employee Management System that provides RESTful APIs to perform CRUD operations on employee data. This project follows layered architecture and best practices for building scalable backend applications.

--> FEATURES

-Add new employee

-UPdate employee details

-Delete employee

-Get employee by ID

-Get all employees 

-Exception handling with meaningful responses

-Validation using annotations

-RESTful API design

--> TECH STACK

Java, Spring Boot, MySQL Workbench, POSTMAN, Eclipse Neon 

--> How to run this project from the IDE :

1. Open the project file in an IDE like Eclipse

2. You can run the DBScript provided in MySQL to create database and tables with basic values.(Creating database is necessary since hibernate- update option is used : "spring.jpa.hibernate.ddl-auto + update")

3. In case you do not want to run file, you can cahnge the line "spring.jpa.hibernate.ddl-auto = update" to "spring.jpa.hibernate.ddl-auto = create-drop" in src/main/resources/application.properties file.

4. Check your database connection in src/main/resources/application.properties file and change if needed.

5. Go to com.employee.management.

6. Right click on Application.

7. Hit "Run as Java Application" in the IDE.

8. Check if localhost server has started.

9. Open Postman client service on Google Chrome.

10. Hit url : "http:/localhost:8080/employees" and url : "https:/localhost:8080/departments"

11. Accordingly select the request method and the url as follows : Department: GET - "https:/localhost:8080/departments" - gets list of all departments GET - "https:/localhost:8080/departments/{id}" - gets            department with selected id POST - "https:/localhost:8080/departments" -  inserts into department PUT - "https:/localhost:8080/departments{id}" - updates department with selected id DELETE -                       "https:/localhost:8080/departments" - deletes all departments DELETE - "https:/localhost:8080/departments{id}" - deletes departments with selected id PATCH - "https:/localhost:8080/departments{id}" -              patches/updates departments with selected id.

12. Same goes with the employee too.

--> Assumptions:

1. DATABASE and TABLES are created in MySQL.

2. DepartmentID is a foreign key in Employee table.

3. Make sure department table is populated with the department you refer for in employees.

4. While inserting employee detail through postman service : give a department id for department.

--> Design Discussion:

1. The employee table has a department id foreign key.

2. Department table needs to have a value existing to be referred by the employee table.

3. Get mapping will fetch the results, POST mapping will insert results, PUT mapping and Patch mapping will update results, Delete mapping will delete results.

4. You will need to create database if not, change in the appication.properties file.
