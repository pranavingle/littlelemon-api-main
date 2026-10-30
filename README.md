# Little Lemon Restaurant API

A Django REST Framework capstone for restaurant menus, table bookings, and user registration.

## Requirements

- Python 3.12
- Pipenv
- MySQL Server

## Setup

Create a MySQL database and user, then set the `DB_NAME`, `DB_USER`, `DB_PASSWORD`, `DB_HOST`, and `DB_PORT` environment variables. Install dependencies and run the migrations:

```shell
pipenv install
pipenv run python manage.py check
pipenv run python manage.py migrate
pipenv run python manage.py test restaurant
pipenv run python manage.py runserver
```

See [Readme.txt](Readme.txt) for database setup details, example API requests, and endpoint permissions.

## API

- `GET /api/menu/` — public menu listing
- `/api/menu/` — menu changes for staff or members of the `Manager` group
- `/api/bookings/` — authenticated booking management
- `/api/auth/users/` — user registration
- `/api-token-auth/` — token authentication
