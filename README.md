# Docker PHP Project
This repository contains a Docker configuration for setting up a PHP development environment with MySQL and phpMyAdmin.

## Prerequisites
Before you begin, ensure you have met the following requirements:

Docker installed on your local machine.
## Getting Started
To get started with this project, follow these steps:

Clone this repository to your local machine:
```
   git clone https://github.com/vikaskamboj321/docker-php.git
```
Navigate into the project directory:
   ```
   cd docker-php-project
   ```
Build and start the Docker containers:
   ```
   docker-compose up -d
   ```
Access your PHP application at <b>http://localhost</b> and phpMyAdmin at <b>http://localhost:8080</b>.
## Configuration
### PHP Container
   * Port: 80
   * Volume: ./src directory mapped to /var/www/html inside the container.
### MySQL Container
   * Image: MySQL 5.7
   * Port: 3306
   * Volume: ./dbdata directory mapped to /var/lib/mysql inside the container.
   * Environment Variables:
      * MYSQL_ROOT_PASSWORD: rootpass
      * MYSQL_DATABASE: phpdocker
      * MYSQL_USER: dbuser
      * MYSQL_PASSWORD: dbpass
### phpMyAdmin Container
   * Image: phpMyAdmin
   * Port: 8080
   * Environment Variables:
      * PMA_HOST: mysql
      * PMA_PORT: 3306
      * UPLOAD_LIMIT: 256M
## Contributing
Contributions are welcome! Feel free to submit a pull request or open an issue if you find any bugs or have suggestions for improvements.

## License
This project is licensed under the MIT License.
