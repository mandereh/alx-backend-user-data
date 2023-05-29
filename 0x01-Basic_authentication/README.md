# My Simple API

Simple HTTP API for playing with `User` model.


## The Files

### `models/`

- `base.py`: base of all models of the API - handle serialization to file
- `user.py`: user model

### `api/v1`

- `app.py`: entry point of the API
- `views/index.py`: basic endpoints of the API: `/status` and `/stats`
- `views/users.py`: all users endpoints


## The Setup

```
$ pip3 install -r requirements.txt
```


## The Run

```
$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```


## The Routes

- `GET /api/v1/status`: This returns the status of the API
- `GET /api/v1/stats`: This returns some stats of the API
- `GET /api/v1/users`: This returns the list of users
- `GET /api/v1/users/:id`: This returns an user based on the ID
- `DELETE /api/v1/users/:id`: This deletes an user based on the ID
- `POST /api/v1/users`: This creates a new user (JSON parameters: `email`, `password`, `last_name` (optional) and `first_name` (optional))
- `PUT /api/v1/users/:id`: This updates an user based on the ID (JSON parameters: `last_name` and `first_name`)
