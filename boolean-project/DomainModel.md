User stories:
```
1.
As a user, 
I want to view a list of employees, 
so I can see the existing workforce.
```

```
2.
As a user, 
I want to add a new employee, providing their details, 
so that I can keep the employee records up to date.
```

```
3.
As a user, 
I want to edit an existing employee's information, 
so I can keep their details accurate.
```

```
4.
As a user, 
I want to delete an employee from the records, 
in case an employee leaves the organization.
```

```
5.
As a user, 
I want to search for employees based on their name, email, phone, or job title, 
to quickly find specific employees.
```

| Class/Component     | Properties/Methods                                                                                                                       | Description                                                                                         |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **Employee**        | - `id` (number)<br> - `name` (string)<br> - `email` (string)<br> - `phone` (string)<br> - `jobTitle` (string)                         | Represents an employee with basic information.                                                    |
| **EmployeeService** | - `getEmployees(): Observable<Employee[]>`<br> - `addEmployee(employee: Employee): Observable<Employee>`<br> - `updateEmployee(employee: Employee): Observable<Employee>`<br> - `deleteEmployee(employeeId: number): Observable<void>` | Provides methods to interact with employee data source (CRUD operations).                        |
| **AppComponent**    | - `employees` (array of Employee objects)<br> - `editEmployee` (Employee object)<br> - `deleteEmployee` (Employee object)<br> - `getEmployees()`<br> - `onAddEmployee(addForm: NgForm)`<br> - `onUpdateEmployee(employee: Employee)`<br> - `onDeleteEmployee(employeeId: number)`<br> - `searchEmployees(key: string)`<br> - `onOpenModal(employee: Employee, mode: string)` | Main component handling UI interactions and employee data.<br>Contains various methods for CRUD operations and user interactions. |
