# Cinema app

### Project description:
With this app you will be able to pass authentication, 
access URL pages according to your role, 
make an order and finally get a movie ticket on the necessary date 
in your favorite cinema hall. Also, you can see the list of movie 
sessions on that day. Enjoy your movie:)

## Endpoints:
- ```/register, /login``` Method-type: **POST**. Permissions: **ALL**.
- ```/cinema-halls, /movies, /movie-sessions/available``` Method-type: **GET**. Permissions: **USER**, **ADMIN**
- ```/users/by-email``` Method-type: **GET**. Permissions: **ADMIN**
- ```/cinema-halls, /movies, /movie-sessions``` Method-type: **POST**. Permissions: **ADMIN**
- ```/movie-sessions/{id}``` Method-type: **PUT**, **DELETE**. Permissions: **ADMIN**
- ```/orders, /shopping-carts/by-user``` Method-type: **GET**. Permissions: **USER**
- ```/orders/complete``` Method-type: **POST**. Permissions: **USER**
- ```/shopping-carts/movie-sessions``` Method-type: **PUT**. Permissions: **USER**

## 3-layer architecture:
- Data tier - DAOs
- Application tier - Services
- Presentation tier - Controllers

## Technologies:
- Java
- Apache Tomcat - version 9.0.50
- Apache Maven
- MySQL
- Hibernate
- Spring MVC
- Spring Core
- Spring Security

## How to start the program:
- Install MySQL and Apache Tomcat version 9. 
- Configure Apache Tomcat for your IDE. 
- Configure [db.properties](src/main/resources/db.properties) with your *URL*, *USERNAME*, *PASSWORD*, *JDBC_DRIVER*.
- You already have two registered users:
  - first user: login: ```user@i.ua```, password: ```user1234```, role: ```USER```
  - second user: login: ```admin@i.ua```, password: ```admin1234```, role: ```ADMIN```;
- In the [SecurityConfig.java](src/main/java/cinema/config/SecurityConfig.java) you can change access level.