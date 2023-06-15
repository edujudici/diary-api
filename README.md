# Build a RESTful API using Golang and Gin

## Packages

- <b>Go Cryptography:</b> This provides supplementary Go cryptography libraries.
- <b>GoDotEnv:</b> This will help with managing environment variables.
- <b>GORM:</b> This is an ORM (Object Relational Mapper) for Golang. In addition to the library, the GORM dialect (driver) for Postgres is installed to enable connections to PostgreSQL databases.
- <b>JWT-Go:</b> A Go implementation of JSON Web Tokens.

## Installation

It assumes that you meet the prerequisites stated above to follow the steps below:

Clone repository
```sh
git clone https://github.com/edujudici/diary-api.git
```

Running database local

```sh
docker run --name postgres_db  -p 5432:5432 -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=diary -d postgres
```

Running application

```sh
go run main.go
```

## Collections

<https://documenter.getpostman.com/view/6493792/2s93sgVpmF>

## Request

```sh
# register new user
POST: http://localhost:8000/register

# login with user and pass
# return jwt token
POST: http://localhost:8000/login

Example payload to register/login
    {
        "username": "userfortest",
        "password": "passfortest"
    }
```

```sh
# get all entries, set Bearer Token
GET: http://localhost:8008/api/entry

# create entry, set Bearer Token
POST: http://localhost:8008/api/entry
    {
        "content": "content here"
    }
```

License

----

MIT

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)