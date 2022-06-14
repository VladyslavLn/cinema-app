# <p align="center">:clapper: Cinema app :clapper:</p>


# :closed_book: General info:
A simple web-application that supports authentication, registration and other CRUD operations. You can check movie sessions, buy tickets, add new movies, etc.
The application uses Spring, Hibernate and is built on Rest principles. The user can have the `user` role or the `admin` role.

# :eyes: About project:
The application has the ability:
- view lists of cinema halls, movies, all movie sessions, orders, movie sessions for a movie on a date
- find movie session by id, shopping cart by user, user by email
- add movie, movie session, cinema hall, order
- change movie session by id, movie session from shopping cart
- delete movie session </br>

There are two types of roles in the application: `ADMIN` and `USER`. During registration, the user is assigned a role USER.
###### All users have access to pages:
`/register` </br>
`/login` </br>
###### Users with role Admin or User have access to pages:
`GET: /cinema-halls` - get a list of cinema halls </br>
`GET: /movies` - get a list of movies </br>
`GET: /movie-sessions/available` - get a list of all movie sessions for a movie (by id) on a date </br>
`GET: /movie-sessions/{id}` - get movie sessions with id </br>
###### Users with role Admin have access to pages:
`POST: /movies` - add movie </br>
`POST: /movie-sessions` - add movie session </br>
`POST: /cinema-halls` - add cinema hall </br>
`GET: /users/by-email` - get user by email </br>
`PUT: /movie-sessions/{id}` - change movie session by id </br>
`DELETE: /movie-sessions/{id}}` - delete movie session by id </br>
###### Users with role User have access to pages:
`GET: /orders` - get a list of user's orders </br>
`GET: /shopping-carts/by-user` - get user's shopping cart </br>
`POST: /orders/complete` - add order </br>
`PUT: /shopping-carts/movie-sessions` - change movie session (by id) from shopping cart </br>

# :abacus: Technologies used:
- Java 11
- Hibernate
- Spring Framework
- REST
- MySQL
- Lombok (v1.18.20)
- Apache Tomcat 9.0.54 (to run app locally)

# :computer: If you want to run this project on your computer, you need:
1. To have or install MySQL and Apache Tomcat 9.0.50
2. Clone this project:
```bash
git clone https://github.com/VladyslavLn/cinema-app.git
```
3. Configure `dbProperties` file from `resources` directory to create connection to db:
```java
    db.driver=com.mysql.cj.jdbc.Driver
    db.url=YOUR_URL
    db.user=YOUR_LOGIN
    db.password=YOUR_PASSWORD
```
4. Add Tomcat configuration to your project. Use `/` as your Tomcat application context
5. Add [Lombok](https://projectlombok.org/setup/overview) plugin to your IDE

After all these steps you will be able to run this project locally.

Then you can log in with :

`USER` roles:
```java
username - user@i.ua
password - user1234
```
`ADMIN` roles:
```java
username - admin@i.ua
password - admin123
```