# Simple API

A Simple HTTP API for playing with `User` model.


## Files

### `models/`

- `base.py`: The base of all models of the API - handle serialization to file
- `user.py`: The user model

### `api/v1`

- `app.py`: The entry point of the API
- `views/index.py`: The basic endpoints of the API: `/status` and `/stats`
- `views/users.py`: The all users endpoints


## Setup

```
$ pip3 install -r requirements.txt
```


## Run

```
$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```


## Routes

- `GET /api/v1/status`: The returns the status of the API
- `GET /api/v1/stats`: The returns some stats of the API
- `GET /api/v1/users`: The returns the list of users
- `GET /api/v1/users/:id`: The returns an user based on the ID
- `DELETE /api/v1/users/:id`: The deletes an user based on the ID
- `POST /api/v1/users`: The creates a new user (JSON parameters: `email`, `password`, `last_name` (optional) and `first_name` (optional))
- `PUT /api/v1/users/:id`: The updates an user based on the ID (JSON parameters: `last_name` and `first_name`)
