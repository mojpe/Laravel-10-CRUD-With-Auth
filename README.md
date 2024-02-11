# Instalation guide

## How to setup and run the project
1. clone Laravel in to the folder "laravel"
2. docker-compose up -d
3. docker exec -it laravel_app sh -c 'cd /var/www/html/laravel && cp .env.example .env && composer install && php artisan key:generate && php artisan migrate --seed'
4. http://localhost/
