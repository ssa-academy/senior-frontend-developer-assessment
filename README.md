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
For any questions regarding the exam please send inquiry to <a href="mailto:louie@ssagroup.com">jonathan@ssagroup.com</a> or HR.

**Output**: Examinee is expected to send an email with attachment to their output files (preferably a zip file). Alternatively, examinee can attach a link to their GitHub Repository, Google Drive, Dropbox, or any other storage service to download the output if the file is too large to be attached on email, or for other reason.

<br>
<hr>
<br>

<a name="GettingStarted"></a>
### Getting Started

- Clone this repository.
    ```
    git clone https://github.com/ssa-academy/senior-frontend-developer-assessment.git
    ```
- Install package dependencies
    ```
    npm install
    ```
- Run the development server
    ```
    npm run serve
    ```

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

- Add page to view deactivated users.

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
    * Base URL is `http://oreo.rippl3s.com/api/v1`
    * Use the following credentials to retrieve a fresh token to be used in the app:
    	- `POST` `https://oreo.rippl3s.com/api/v1/login`
            
            Use the following credentials:
            ```
            +------------+-----------+----------------------+-----------+-----------+------------+
            | First Name | Last Name | Email                | Username  | Password  | Role       |
            +------------+-----------+----------------------+-----------+-----------+------------+
            | Jane       | Smith     | jane@ssagroup.com    | janesmith | Jane@8799 | Examinee   |
            +------------+-----------+----------------------+-----------+-----------+------------+
            ```

            Request:
            ```json
            {
                "username": "janesmith",
                "password": "Jane@8799"
            }
            ```
            
            Response:

            ```json
            {
                "user": {
                    "id": 1,
                    "prefixname": "Dr.",
                    "firstname": "Jane",
                    "middlename": "Stark",
                    "lastname": "Smith",
                    "suffixname": null,
                    "username": "janesmith",
                    "email": "jane@ssagroup.com",
                    "photo": "data:image/png;base64,<hash>",
                    "type": "superadmin",
                    "email_verified_at": null,
                    "created_at": "2020-10-08 09:36:29",
                    "updated_at": "2020-10-08 10:15:21",
                    "deleted_at": null,
                    "avatar": "data:image/png;base64,<hash>",
                    "birthday": null,
                    "created": "45 minutes ago",
                    "deleted": "",
                    "details": { ... },
                    "details:common": [ ... ],
                    "details:others": [ ... ],
                    "displayname": "Jane S. Smith",
                    "is:superadmin": true,
                    "modified": "6 minutes ago",
                    "permissions": [ ... ],
                    "role": "Examinee",
                    "roles": [
                        5
                    ]
                },
                "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6IjhkYzc4MmQ3NzU5YWI4MjM2ZTFkOGU4MGIxZTM4ZWJmODk0YmUzYmZhZjU3NWMxMWZiYTc0M2I2ZWY4ZmE2YmJjZjliNmQ3Mjg0ZjVhYTc4In0.eyJhdWQiOiIxIiwianRpIjoiOGRjNzgyZDc3NTlhYjgyMzZlMWQ4ZTgwYjFlMzhlYmY4OTRiZTNiZmFmNTc1YzExZmJhNzQzYjZlZjhmYTZiYmNmOWI2ZDcyODRmNWFhNzgiLCJpYXQiOjE2MDIxNTI1MDQsIm5iZiI6MTYwMjE1MjUwNCwiZXhwIjoxNjMzNjg4NTA0LCJzdWIiOiIxIiwic2NvcGVzIjpbXX0.TktHs1otSWTmEClasZCTML8DrFqX3NKk63rwz3AKjN92nbsyKoWlq_RJmQBGkdy-RAsMQ7lkKdMo-2Fr60WJ9ILTDja5-4p3lMcgTHVImmiI1Azm4XKea7tL56o9FYITXY7pmOZSaeWoT_mtxhZOgnC9V0lNyHWCoZJnP5mpQVhyMrsDxadKw-PUIuQ6lTZip5UIX_DgPpOPwWcLOvbY-LQ7hK3DG9cTgYPb9WgRwKXc59Lv-K_XOcLwY73eeMrutBfbbv9tcdw6zrYvEMChCM_QDnLSNf-ccySUZyQwFEmC8WuksIepN-tJPOQXFlX41ON_Y4qrUpalPWpgQwGGOGyCH0Tz1GaeIYhTeoVlyhy9OUvqdtcwFpjeZvb_9oL5vn9Ua7mNTa2kaeWEJgQ4p8TbWNNgoH24SNCGj_TCPyNvQspoUGOrhvJ5686mw_8vEyT3ETDqgFVKVl53JOzJO5v654aRQh9iYToQvzBnjswySuJ_xbiLk4GM4jLuA1lc9SYoqwwhFYC6aSsgedMInmTQM8_-k-veDajI-13y-TSZHjdtubertoy4rwXgAFgvpCMv9lW17SrER_vfUXDv07hIxumodw0HlUGfqT-b7sxhV-CUb8MqfhIx26fqyLALluks_HRYGSZd5rlw6ayJVkMqJp6fP5BFVYR6rNW3R0I"
            }
            ```
<br>
<br>

1. Implement the following API:
    1. Create new users:
        * `POST` `https://oreo.rippl3s.com/api/v1/user/tests`
        * Request:
            ```json
            {
                "firstname": "Angelina",
                "lastname": "Jolie",
                "username": "angel",
                "email": "angelina@demo.io",
                "password": "Angel@1000",
                "photo": <UploadedFile> or NULL
            }
            ```
        * Response:
            ```json
            {
                "data": {
                    "prefixname": null,
                    "firstname": "Angelina",
                    "middlename": null,
                    "lastname": "Jolie",
                    "suffixname": null,
                    "username": "angel",
                    "email": "angel@demo.io",
                    "photo": null,
                    "type": "test",
                    "updated_at": "2020-10-08 10:58:00",
                    "created_at": "2020-10-08 10:58:00",
                    "id": 4,
                    "avatar": "data:image/png;base64,<hash>",
                    "birthday": null,
                    "created": "1 second ago",
                    "deleted": "",
                    "displayname": "Angelina  Jolie",
                    "modified": "1 second ago",
                    "role": ""
                }
            }
            ```
    <br><br>
    1. Update existing users:
        * `PUT` `https://oreo.rippl3s.com/api/v1/user/tests/${id}`
        * Request:
            ```json
            {
                "firstname": "Angelina",
                "lastname": "Jolie",
                "username": "angelina",
                "email": "angelina@demo.io",
                "password": "Angelina@1000",
                "photo": null
            }
            ```
        * Response:
            ```json
            true
            ```
    <br><br>
    1. Delete existing user:
        * `DELETE` `https://oreo.rippl3s.com/api/v1/user/tests/${id}`
        * Response:
        ```json

        ```
    <br><br>
    1. Retrieve all existing users:
        * `GET` `https://oreo.rippl3s.com/api/v1/user/tests`
        * Response:
        ```json
        {
            "data": [ ... ],
            "links": { ... },
            "meta": { ... }
        }
        ```
    <br><br>
    1. Retrieve a single user:
        * `GET` `https://oreo.rippl3s.com/api/v1/user/tests/${id}`
        * Response:
        ```json
        {
            "data": {
                "id": 1,
                "prefixname": "Dr.",
                "firstname": "Jane",
                "middlename": "Stark",
                "lastname": "Smith",
                "suffixname": null,
                "username": "janesmith",
                "email": "jane@ssagroup.com",
                "photo": "data:image/png;base64,<hash>",
                "email_verified_at": null,
                "created_at": "2020-10-08 09:36:29",
                "updated_at": "2020-10-08 10:15:21",
                "deleted_at": null,
                "avatar": "data:image/png;base64,<hash>",
                "birthday": null,
                "created": "1 hour ago",
                "deleted": "",
                "displayname": "Jane S. Smith",
                "modified": "53 minutes ago",
                "role": "Examinee"
            }
        }
        ```


    

<br>


##### ★ Bonus

- Implement pagination.

<br>
<hr>
<br> 

<p align="center">
:four_leaf_clover:  Good luck!
</p>

<p align="center">
<small>Prepared for SSA Academy Software and Web Developer Applicants only.<br>Do not reproduce document elsewhere.</small>
</p>
