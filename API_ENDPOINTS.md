# RESTful API Endpoints Specifications

## User Management

### Create User
- **Endpoint:** `POST /api/users`
- **Description:** Creates a new user in the system.
- **Payload:**  `{ "name": "string", "email": "string", "password": "string" }`

### Get User
- **Endpoint:** `GET /api/users/{id}`
- **Description:** Retrieves the user details.

### Update User
- **Endpoint:** `PUT /api/users/{id}`
- **Description:** Updates the user information.
- **Payload:**  `{ "name": "string", "email": "string" }`

### Delete User
- **Endpoint:** `DELETE /api/users/{id}`
- **Description:** Deletes a user from the system.

## Clinic Management

### Create Clinic
- **Endpoint:** `POST /api/clinics`
- **Description:** Creates a new clinic.
- **Payload:**  `{ "name": "string", "location": "string" }`

### Get Clinic
- **Endpoint:** `GET /api/clinics/{id}`
- **Description:** Retrieves the clinic details.

### Update Clinic
- **Endpoint:** `PUT /api/clinics/{id}`
- **Description:** Updates the clinic information.
- **Payload:**  `{ "name": "string", "location": "string" }`

### Delete Clinic
- **Endpoint:** `DELETE /api/clinics/{id}`
- **Description:** Deletes a clinic from the system.

## Assistant Management

### Create Assistant
- **Endpoint:** `POST /api/assistants`
- **Description:** Creates a new assistant.
- **Payload:**  `{ "name": "string", "clinic_id": "int" }`

### Get Assistant
- **Endpoint:** `GET /api/assistants/{id}`
- **Description:** Retrieves the assistant details.

### Update Assistant
- **Endpoint:** `PUT /api/assistants/{id}`
- **Description:** Updates the assistant information.
- **Payload:**  `{ "name": "string" }`

### Delete Assistant
- **Endpoint:** `DELETE /api/assistants/{id}`
- **Description:** Deletes an assistant from the system.

## Time Clock Management

### Clock In
- **Endpoint:** `POST /api/clock-in`
- **Description:** Records the clock in time for an employee.
- **Payload:**  `{ "user_id": "int" }`

### Clock Out
- **Endpoint:** `POST /api/clock-out`
- **Description:** Records the clock out time for an employee.
- **Payload:**  `{ "user_id": "int" }`

## Salary Management

### Get Salary
- **Endpoint:** `GET /api/salaries/{user_id}`
- **Description:** Retrieves the salary details for a specific user.

### Update Salary
- **Endpoint:** `PUT /api/salaries/{user_id}`
- **Description:** Updates the salary details for a specific user.
- **Payload:**  `{ "salary": "float" }`

### Delete Salary
- **Endpoint:** `DELETE /api/salaries/{user_id}`
- **Description:** Deletes salary information for a specific user.