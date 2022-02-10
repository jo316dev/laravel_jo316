
## Larave in Docker (Postgres, Nginx and PHP 8)
 - A basic environment to development and trainning.
 
 
## Requeriments

- This environment was tested only Ubuntu 20.04.
- Docker last version.
- Git tools

## How to install

- Clone the repository
```sh
git clone https://github.com/jo316dev/laravel_jo316.git name_of_project
```
- After, enter in your prject
```sh
cd name_of_project
```
- Update the environment variables in the .env file
```dosini
APP_NAME=name_your_project
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost:8989

LOG_CHANNEL=stack
LOG_LEVEL=debug

DB_CONNECTION=pgsql
DB_HOST=pgsql
DB_PORT=5432
DB_DATABASE=data_file
DB_USERNAME=postgres
DB_PASSWORD=secret
```
- Go up the containers
```sh
docker-compose up -d
```
- Access the project's container
```sh
docker-compose exec laravel-app
```
- Install all dependencies
```sh
composer install
```
- Generate the proeject key
```sh
php artisan key:generate
```
- Access your prject in http://localhost:8989
