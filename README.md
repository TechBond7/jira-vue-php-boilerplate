# Boilerplate for Jira board project

Hi! Welcome to the Jira project, which is used to evaluate 
code quality and efficiency in engineering candidates.
The code in this project is not perfect, and there are some bugs and improvements
to be made. The code is MIT licensed, do with it whatever you want!

## Requirements
- Docker (https://docs.docker.com/install/)

## Installation of the test project
```
cp .env.example .env
docker compose build
docker compose run web composer install
docker compose run web npm install
docker compose run web php artisan key:generate
docker compose run web php artisan migrate --seed
docker compose up -d
```

You should now be able to browse to http://localhost:8000 and see the project.
Either you can register a new account in the system, or you can use the following 
credentions to log in (or any of the others generated in the UserSeeder):
```
Email: Farmboy2Jedi@TheForce.net
Pass:  password
```

Note: Make sure that the port 8000 and 5173 are available on your machine. 