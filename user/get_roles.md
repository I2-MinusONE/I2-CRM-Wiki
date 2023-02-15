# Get Roles

> This API gets all the roles assigned to an user

Returns a JSON object containing an array of user objects.

- **URL**

  `GET /users/:id/roles.json`

  - **URL Params**
    - id={user id}

- **Success Response:**

  - **Code:** 200 OK <br />
    **Content:**
    ```json
    [
      {
        "id": 1,
        "name": "Role Name",
        "user_ids": [
          1,
          2 // other users that have been assigned this role
        ],
        "permission_ids": [
          1,
          2 // other permission ids for that role
        ]
      }
      // and so on
    ]
    ```
