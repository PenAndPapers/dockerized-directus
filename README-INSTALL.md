## Application Installation

#### Change file permission by running the ff. commands
```sudo chmod -R 777 docker_services_config/nginx/cert```
```sudo chmod -R 777 logs```
```sudo chmod -R 777 public/uploads```

#### Install depedencies by running the ff. commands
```composer install```
```yarn install```

#### Dump schema by running the ff. commands
```docker-compose up```
```docker exec -it YOUR_MYSQL_CONTAINER_NAME /bin/bash```
```mysql -u root -p YOUR_DATABASE_NAME < /PATH/TO/YOUR/schema.sql```
  - use .env DB configuration values

#### Validate database tables by signing in to mysql
```mysq -u root -p```
```USE YOUR_DATABASE_NAME;```
```SHOW TABLES;```
```exit```

#### Update config file
  - create new file api.php in config directory using _example.php contents
  - open config/api.php using your text editor
  - change DB parameters using .env database details

#### Accessing directus from host machine
```https://localhost:4499/admin/#/login````