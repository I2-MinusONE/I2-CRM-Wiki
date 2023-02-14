# Get Users

> This API gets all the users in the database.

Returns a JSON object containing an array of user objects.

- **URL**

  `/api/users?{search_params}`
  - **Search Params**
    - company_id={value}
    - team_id={value}

- **Method:**

  `GET`

- **Success Response:**

  - **Code:** 200 OK <br />
    **Content:** `{ users: [ { id : 1, contact_id: 234 }, { id: 2, contact_id: 543 } ] }`

- **Error Response:**

  - **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "No users found" }`

- **Sample Call:**

  ```javascript
  $.ajax({
    url: "/api/users",
    dataType: "json",
    type : "GET",
    success : function(r) {
      console.log(r);
    }
  });
  ```


## Notes:

The response will be a JSON object containing an array of user objects. Each user object will contain an id and a contact_id.