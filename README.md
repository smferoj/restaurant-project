## json server -->

npm install -g json-server

db=> db.json
{
  "users": [
    { "id": 1, "name": "John Doe", "email": "john@example.com" },
    { "id": 2, "name": "Jane Doe", "email": "jane@example.com" }
  ]
}

json-server --watch db.json

    http://localhost:3000/users - Lists all users
    http://localhost:3000/users/1 - Gets the user with id 1
    http://localhost:3000/users/2 - Gets the user with id 2

    GET http://localhost:3000/user1
    GET http://localhost:3000/users
    GET http://localhost:3000/users/1


    <!--  can check it using postman -->