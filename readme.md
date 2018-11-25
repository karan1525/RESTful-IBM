## What it does?

The following repo is for creating a quick REST API mock using JSON-Server NPM module and does the following:

- Pagination
- Sorting
- Adding a new record

### How to run

```sh
$ git clone https://github.com/karan1525/RESTful-IBM
$ cd RESTful-IBM
$ npm install -g json-server
$ json-server --watch data/db.json -r routes.json
```

### What are all the routes

- Pagination -> paginates by arguments -> page and limit
  - Provide pagination as : localhost/paginate/limit/page
    - Example: http://localhost:3000/paginate/10/100
- Sorting -> by either 1, 2 or 3 parameters
  - Provide sorting as: localhost/sort/column1/sort1
    - Example: http://localhost:3000/sort/id/desc
    - Example: http://localhost:3000/sort/id/asc/first_name/desc/
- Adding a new record -> adds a new record to the given DB file.
  - POST call on localhost/data
    Example: {
    "id": 9291,
    "first_name": "Andrea",
    "last_name": "Duffus",
    "email": "aduffus0@163.com",
    "gender": "Female",
    "age": 24
    }
