# 0x02. Session authentication

## Description:

I learnt the followingas as I did the tasks in this project:

* What authentication means
* What session authentication means
* What Cookies are
* How to send Cookies
* How to parse Cookies

---

## Tasks

+ [x] [0. Et moi et moi et moi!](./api/v1/app.py)

   + Copy all your work of the 0x06. Basic authentication project in this new folder.

+ [x] [1. Empty session](./api/v1/auth/session_auth.py)

   + Create a class SessionAuth that inherits from Auth. For the moment this class will be empty. It’s the first step for creating a new authentication mechanism:

+ [x] [2. Create a session](./api/v1/auth/session_auth.py)

   + Update SessionAuth class:

+ [x] [3. User ID from Session ID](./api/v1/auth/session_auth.py)

   + Update SessionAuth class:

+ [x] [4. Session cookie](./api/v1/auth/auth.py)

   + Update api/v1/auth/auth.py by adding the method def session_cookie(self, request=None): that returns a cookie value from a request:

+ [x] [5. Before request](./api/v1/app.py)

   + Update the @app.before_request method in api/v1/app.py:

+ [x] [6. Use Session ID for identifying a User](./api/v1/auth/session_auth.py)

   + Update SessionAuth class:

+ [x] [7. New view for Session Authentication](./api/v1/views/session_auth.py)

   + Create a new Flask view that handles all routes for the Session authentication.

+ [x] [8. Logout](./api/v1/auth/session_auth.py)

   + Update the class SessionAuth by adding a new method def destroy_session(self, request=None): that deletes the user session / logout:

---

## Author

**Nicholas M Mwanza** - [Nicky-muindi](https://github.com/Nicky-muindi) :black_nib:
