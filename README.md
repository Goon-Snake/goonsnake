# Installing

0. Ensure you are using Python 3

   ```bash
   python --version
   Python 3.7.3
   ```

1. Set up an isolated [virtualenv](https://virtualenv.pypa.io/en/latest/)

   ```bash
   pip install virtualenv
   virtualenv goonsnake
   cd goonsnake
   source ./bin/activate
   ```

2. Set up the repository

   ```bash
   git clone git@github.com:Goon-Snake/goonsnake.git
   cd goonsnake
   pip install -r requirements.txt
   ```

# Using Django

## Administration commands

```bash
python manage.py --help
```

### Run migrations

```bash
python manage.py migrate
```

### Run a local server

```bash
python manage.py runserver
```

# Deploying

We deploy to Heroku, typically using the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-command-line).

## Continous Delivery

Commits to `master` will be automatically deployed to our [staging site](https://github.com/Goon-Snake/goonsnake) on Heroku.

## Server administration

### Run migrations

```bash
heroku run --app goonsnake-staging python manage.py migrate
```

### Create a user

```bash
heroku run --app goonsnake-staging python manage.py createsuperuser

Username (leave blank to use 'u25552'): steve
Email address: steve@kotiri.com
Password:
Password (again):
Superuser created successfully.
```
