# Destroy Token
> Destroys all exiting tokens for the user

## URL
`DELETE` /users/token.json?user_id=`:id`

## Query Parameters
* `id`: User ID  

## Response: Success
Status Code: `200 OK`
```
No Content
```

## Response: Failure
> Could happen is authorization fails `403` or record is not found `404`

Status Code: `403 Forbidden`
```
No Content
```

Status Code: `404 Not Found`
```
No Content
```