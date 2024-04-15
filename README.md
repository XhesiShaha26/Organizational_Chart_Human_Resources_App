# Organizational_Chart_Human_Resources_App

Base Class: Employee
Purpose: Acts as an abstract base class for all types of employees within the organization.
Properties:
name: Stores the employee's name.
position: Stores the job title of the employee within the company.
wage: Records the salary of the employee.
yearsOfService: Tracks how many years the employee has worked for the company.
employmentType: Specifies the type of employment (e.g., full-time, part-time, contractor).
Methods:
Constructor: Initializes a new employee object with the specified properties.
Getters and Setters: Provide access and update capabilities for each property.
calculateBonus(): An abstract method that each subclass must implement to calculate a bonus based on specific criteria.
conductPerformanceReview(): An abstract method that outlines how performance reviews should be conducted, specific to each type of employee.
displayDetails(): Prints out the employee's details, including name, position, wage, years of service, and employment type. This method is essential for verifying that the information is accurately stored and represented.

Subclass: Manager
Purpose: Represents a specific type of employee who manages a department.
Properties:
department: The department that the manager oversees.
Specialized Methods:
calculateBonus(): Implements the method from Employee to calculate the manager's bonus, typically based on their wage, years of service, and possibly departmental performance.
conductPerformanceReview(): Specific implementation for conducting performance reviews for managerial staff, which may include leadership performance and department achievements.

Class: HRSystem
Purpose: Manages a collection of employees and handles operations such as adding, updating, and removing employees, as well as displaying organizational details.
Properties:
employees: A list that holds all employee objects.
Methods:
addEmployee(Employee employee): Adds a new employee to the system.
removeEmployee(Employee employee): Removes an employee from the system.
updateEmployeeWage(Employee employee, double newWage): Updates the wage of an existing employee.
displayOrgChart(): Displays details for all employees in the system, along with their calculated bonuses and outcomes from their performance reviews.

Main Class:
This class acts as the entry point for the application, where instances of Manager and StaffMember are created, manipulated, and their details are displayed through the HRSystem. It demonstrates how the system can be interacted with, such as adding employees, updating their wages, and removing them from the system.

Each class and subclass is designed to encapsulate specific functionalities and attributes related to different types of employees in an organization, while the HRSystem manages these objects and orchestrates operations across them. This structure promotes organized code management, ease of updates, and scalability.
