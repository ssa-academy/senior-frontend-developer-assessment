<h1 align="center">
Assessment for Frontend Developer (VueJs)
</h1>

<br>

This assessment is designed to test an examinee’s knowledge of Front-end Development and its implementations on VueJs framework. It is divided into 3 levels, with each feature having to be accomplished consecutively.

**Assessment Point System**: The assessment total is 60 points with additional 30 bonus points. 
See breakdown below for more detail.

| Levels  | Points | Bonus | Total |
| ------- | -----: | ----: | ----: |
| Level 1 |     10 |    5  |   15  |
| Level 2 |     20 |    10 |   30  |
| Level 3 |     30 |    15 |   45  |
|   TOTAL |    	60 |    30 |   90  |

**Asessment Duration**: Examinee is given 3 days to complete the assessment. On a separate spreadsheet, please log the time spent per functionality (start time and end time).
For any questions regarding the exam please send inquiry to <a href="mailto:ellen@ssagroup.com">ellen@ssagroup.com</a> or HR.

**Output**: Examinee is expected to send an email with attachment to their output files (preferably a zip file). Alternatively, examinee can attach a link to their GitHub Repository, Google Drive, Dropbox, or any other storage service to download the output if the file is too large to be attached on email, or for other reason.

<br>
<hr>
<br>

<a name="Level-1"></a>
### Level 1

##### Goals

- [ ] Develop User Management pages

<br>

1. Create pages for:
	- Displaying all users 
	- Creating new user 
	- Updating user 
	- Displaying single user details 

1. On create and edit pages, create a form with the following fields:
    - `First Name` - This is a required text field.
    - `Last Name` - This is a required text field
    - `Username` - This is a required text field.
    - `Email` - This is a required email field. This should only contain a valid email value.
    - `Password` - This is a required password field.

1. Add a label text for each field.

1. Add a placeholder text on each field.

1. Add a validation for the fields.

1. Add a submit button. Clicking this button will display an alert/notification that the user has been added.

<br>

##### ★ Bonus

- Add page for deactivated users.

<br>
<hr>
<br>

<a name="Level-2"></a>
### Level 2

##### Goals

- [ ] Make use of reusable components
- [ ] Develop emptystate component to tables 
- [ ] Develop button components

<br>

1. Do all the steps in [Level 1](#Level-1) but make use and re-use of Vue components as much as possible. 

1. Implement a delete functionality that will soft-delete existing users.

1. Add emptystate component to the table if empty.

1. Implement an edit button that will redirect to the edit page (no update function yet).

<br>

##### ★ Bonus

- Add permanent delete button to the soft-delete table.
- Add restore button to the soft-delete table.

<br>
<hr>
<br>

<a name="Level-3"></a>
### Level 3

##### Goals

- [ ] Integrate REST API to the app

<br>


1. Do all steps in [Level 1](#Level-1) and [Level 2](#Level-2)
1. Implement an API client with the following details:
    * Base URL is `http://demo.rippl3s.com/api`
    * Use the following credentials to retrieve a fresh token to be used in the app:
    	- POST -login link-
    	- `username` 
    	- `password`
1. Implement the following API:
    1. Create new users:
        * Request: `POST `http://demo.rippl3s.com/api/v1/test/users`
        * Request Body:
            ```
                {
                    "firstname": "Jane",
                    "lastname": "Smith",
                    "username": "jane",
                    "email": "jane@ssagroup.com"
                    "password": "Demo@1000"
                    "photo": "Demo@1000"
                }
            ```
        * Response: `HTTP 201`
        * Response Body: Note ignore permission, roles, groups and organisation
            ```
                {
                    "name": "jane@ssagroup.com",
                    "permissions": [],
                    "firstName": "Jane",
                    "lastName": "Smith",
                    "email": "jane.smith@ssagroup.com",
                    "password": null,
                    "roles": [],
                    "groups": [],
                    "id": 79,
                    "organisation": null
                }
            ```
    1. Update existing users:
        * Request: `PUT http://authentication-service.jx-ssagroup-authentication-service-pr-15.ssagroup.com/api/users/{id}`
        * Request Body:
            ```
                {
                    "name": "jane.smith@ssagroup.com",
                    "firstName": "Jane",
                    "lastName": "Smith",
                    "email": "jane.smith@ssagroup.com"
                    "password": "Password1"
                }
            ```
        * Response: `HTTP 200`
        * Response Body: Note ignore permission, roles, groups and organisation
            ```
                {
                    "name": "james.jones@ssagroup.com",
                    "permissions": [],
                    "firstName": "Jane",
                    "lastName": "Smith",
                    "email": "jane.smith@ssagroup.com",
                    "password": null,
                    "roles": [],
                    "groups": [],
                    "id": 79,
                    "organisation": null
                }
            ```
    1. Delete existing user:
        * Request: `DELETE http://authentication-service.jx-ssagroup-authentication-service-pr-15.ssagroup.com/api/users/{id}`
        * Response: `HTTP 204`
    1. List all users:
        * Request: `GET http://authentication-service.jx-ssagroup-authentication-service-pr-15.ssagroup.com/api/users`
        * Response: `HTTP 200`
        * Response Body: Note ignore permission, roles, groups and organisation
            ```
                {
                    "content": [
                        {
                            "name": "jane.smith@ssagroup.com",
                            "permissions": [],
                            "firstName": "Jane",
                            "lastName": "Smith",
                            "email": "jane.smith@ssagroup.com",
                            "password": null,
                            "roles": [],
                            "groups": [],
                            "id": 79,
                            "organisation": null
                        }
                    ],
                    "pageable": {
                        "sort": {
                            "sorted": false,
                            "unsorted": true,
                            "empty": true
                        },
                        "pageSize": 20,
                        "pageNumber": 0,
                        "offset": 0,
                        "paged": true,
                        "unpaged": false
                    },
                    "totalPages": 1,
                    "totalElements": 1,
                    "last": true,
                    "first": true,
                    "sort": {
                        "sorted": false,
                        "unsorted": true,
                        "empty": true
                    },
                    "numberOfElements": 1,
                    "size": 20,
                    "number": 0,
                    "empty": false
                }
            ```

<br>


##### ★ Bonus

- Implement pagination.

<br>
<hr>
<br>
