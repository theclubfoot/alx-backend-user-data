# 0x03 User authentication service
An authentication service is an identity verification mechanism—similar to passwords—for apps, websites, or software systems. It is designed to authenticate the identity of clients (or users) by servers (a computer program), and vice versa. It works similar to time-sharing operating systems that allow many users to perform tasks simultaneously using the same computer memory. An authentication service makes sure that information is accessed only by users who have the access permission or right.

## Description

* I learnt the following while doing the tasks in his project:
   + How to declare API routes in a Flask app
   + How to get and set cookies
   + How to retrieve request form data
   + How to return various HTTP status codes

---

## Tasks

+ [x] [0. User model](./user.py)

   + In this task I created a SQLAlchemy model named User for a database table named users (by using the mapping declaration of SQLAlchemy).

+ [x] [1. create user](./db.py)

   + In this task, I completed the DB class provided below to implement the add_user method.

+ [x] [2. Find user](./db.py)

   + In this task I implemented the DB.find_user_by method. This method takes in arbitrary keyword arguments and returns the first row found in the users table as filtered by the method’s input arguments. No validation of input arguments required at this point.

+ [x] [3. update user](./db.py)

   + Implemented the DB.update_user method that takes as argument a required user_id integer and arbitrary keyword arguments, and returns None.

+ [x] [4. Hash password](./auth.py)

   + Defined a _hash_password method that takes in a password string arguments and returns a string.

+ [x] [5. Register user](./auth.py)

   + Implemented the Auth.register_user in the Auth class provided below:

+ [x] [6. Basic Flask app](./app.py)

   + Set up a basic Flask app.

+ [x] [7. Register user](./app.py)

   + Implemented the end-point to register a user. Define a users function that implements the POST /users route.

+ [x] [8. Credentials validation](./auth.py)

   + Implemented the Auth.valid_login method. It should expect email and password required arguments and return a boolean.

+[x] [9. Generate UUIDs](./auth.py)

   + mplemented a _generate_uuid function in the auth module. The function should return a string representation of a new UUID. Use the uuid module.

+ [x] [10. Get session ID](./auth.py)

   + Implemented the Auth.create_session method. It takes an email string argument and returns the session ID as a string.

+ [x] [11. Log in](./app.py)

   + Implemented a login function to respond to the POST /sessions route.

+ [x] [12. Find user by session ID](./auth.py)

   + Implemented the Auth.get_user_from_session_id method. It takes a single session_id string argument and returns a string or None.

+ [x] [13. Destroy session](./auth.py)

   + Implemented Auth.destroy_session. The method takes a single user_id integer argument and returns None.

+ [x] [14. Log out](./app.py)

   + Implemented logout function to respond to the DELETE /sessions route.

+ [x] [15. User profile](./app.py)

   + Implemented a profile function to respond to the GET /profile route.

+ [x] [16. Generate reset password token](./auth.py)

   + Implemented the Auth.get_reset_password_token method. It take an email string argument and returns a string.

+ [x] [17. Get reset password token](./app.py)

   + Implemented a get_reset_password_token function to respond to the POST /reset_password route.

+ [x] [18. Update password](./auth.py)

   + Implemented the Auth.update_password method. It takes reset_token string argument and a password string argument and returns None

+ [x] [19. Update password end-point](./app.py)

    + Implemented the update_password function in the app module to respond to the PUT /reset_password route.

+ [x] [20. End-to-end integration test](./main.py)

    + Start app. Open a new terminal window.

---


