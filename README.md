# Installation Guide

## Folder Structure and Content

The project follows this folder structure:

- **laravel/**: This directory holds all the Laravel project files.
- **mysql/**: This directory contains configuration files for the MySQL database.
- **nginx/**: Here you'll find the Nginx server configuration files.
- **php/**: This directory contains configuration files for PHP.
- **docker-compose.yml**: This file contains the configuration for Docker Compose.
- **Dockerfile**: This file is used to build the Docker image for the Laravel application container.
- **README.md**: The markdown file you're currently reading.


## How to Setup and Run the Project

1. **Start Docker Compose:**

    Navigate to the project root directory and start Docker Compose to set up the development environment:

    ```bash
    cd path/to/project
    docker-compose up -d
    ```

2. **Initialize the Laravel Application:**

    Access the Laravel application container and initialize the application by executing the following commands:

    ```bash
    docker exec -it laravel_app sh -c 'cd /var/www/html/laravel && cp .env.example .env && composer install && php artisan key:generate && php artisan migrate --seed'
    ```

3. **Access the Application:**

    Once the setup is complete, you can access the application by navigating to [http://localhost/](http://localhost/) in your web browser.

That's it! You've successfully set up and initialized the Laravel project using Docker. You can now start developing your application.
