
# Setup Docker For Laravel 9 Projects with PHP 8
[www.laravelcart.com](https://laravelcart.com)

### Step by step
Repository clone
```sh
git clone https://github.com/laravel20/docker-laravel-9.git laravel9
```

```sh
cd laravel9/
```


Alterne For a branch laravel 8.x
```sh
git checkout laravel-9-com-php-8
```


Remove Versioning
```sh
rm -rf .git/
```


Create the .env file
```sh
cd example-project/
cp .env.example .env
```


Update environment variables from .env file
```dosini
APP_NAME=Laravel
APP_URL=http://localhost:8180

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Upload project containers
```sh
docker-compose up -d
```


access the container
```sh
docker-compose exec app bash
```


Install project dependencies
```sh
composer install
```


Generate Laravel project key
```sh
php artisan key:generate
```


Access the project
[http://localhost:8989](http://localhost:8989)
