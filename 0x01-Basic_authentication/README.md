# 0x0. Basic authentication

## Description

In this project I learnt the following while doing the tasks in the project:

```
-what authentication means
-What Base64 is
-How to encode a string in Base64
-What Basic authentication means
-How to send the Authorization header

```

---

## Tasks

+ [x] [0. Simple-basic-API](./api/v1/app.py)

   + Download and start your project from this [archive.zip](https://alx-intranet.hbtn.io/rltoken/2o4gAozNufil_KjoxKI5bA)
   + Setup and start server

```
bob@dylan:~$ pip3 install -r requirements.txt
...
bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
 * Serving Flask app "app" (lazy loading)
...
bob@dylan:~$

Using the API (in another tab or in your browser)

bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status" -vvv
*   Trying 0.0.0.0...
* TCP_NODELAY set
* Connected to 0.0.0.0 (127.0.0.1) port 5000 (#0)
> GET /api/v1/status HTTP/1.1
> Host: 0.0.0.0:5000
> User-Agent: curl/7.54.0
> Accept: */*
> 
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: application/json
< Content-Length: 16
< Access-Control-Allow-Origin: *
< Server: Werkzeug/1.0.1 Python/3.7.5
< Date: Mon, 18 May 2020 20:29:21 GMT
< 
{"status":"OK"}
* Closing connection 0
bob@dylan:~$

```

+ [x] [1. Error handler: Unauthorized](./api/v1/app.py)

   + What the HTTP status code for a request unauthorized? 401 of course!
   + Edit api/v1/app.py:

Add a new error handler for this status code, the response must be:
a JSON: {"error": "Unauthorized"}
status code 401
  + you must use jsonify from Flask
For testing this new error handler, add a new endpoint in api/v1/views/index.py:

  + Route: GET /api/v1/unauthorized
This endpoint must raise a 401 error by using abort - Custom Error Pages
By calling abort(401), the error handler for 401 will be executed.

In the first terminal:

+ [x] [2. Error handler: Forbidden](./api/v1/auth)

   + What the HTTP status code for a request where the user is authenticate but not allowed to access to a resource? 403 of course!


+ [x] [3. Auth class](./api/v1/auth/auth.py)

   + Now you will create a class to manage the API authentication.

+ [x] [4. Define which routes don't need authentication](./api/v1/app.py)

   + Update the method def require_auth(self, path: str, excluded_paths: List[str]) -> bool: in Auth that returns True if the path is not in the list of strings excluded_paths:

+ [x] [5. Request validation!](./api/v1/app.py)

   + Now you will validate all requests to secure the API:

+ [x] [6. Basic auth](./api/v1/auth/basic_auth.py)

   +  Create a class BasicAuth that inherits from Auth. For the moment this class will be empty.

+ [x] [7. Basic - Base64 part](./api/v1/auth/basic_auth.py)

   + Add the method def extract_base64_authorization_header(self, authorization_header: str) -> str: in the class BasicAuth that returns the Base64 part of the Authorization header for a Basic Authentication:

+ [x] [8. Basic - Base64 decode](./api/v1/auth/basic_auth.py)

   + Add the method def decode_base64_authorization_header(self, base64_authorization_header: str) -> str: in the class BasicAuth that returns the decoded value of a Base64 string base64_authorization_header:

+ [x] [9. Basic - User credentials](./api/v1/auth/basic_auth.py)

   + Add the method def extract_user_credentials(self, decoded_base64_authorization_header: str) -> (str, str) in the class BasicAuth that returns the user email and password from the Base64 decoded value.

+ [x] [10. Basic - User object](./api/v1/auth/basic_auth.py)

   + Add the method def user_object_from_credentials(self, user_email: str, user_pwd: str) -> TypeVar('User'): in the class BasicAuth that returns the User instance based on his email and password.

+ [x] [11. Basic - Overload current_user - and BOOM!](./api/v1/auth/basic_auth.py)

   + Now, you have all pieces for having a complete Basic authentication.

+ [x] [12. Basic - Allow password with ":"](./api/v1/auth/auth.py)

   + Improve the method def extract_user_credentials(self, decoded_base64_authorization_header) to allow password with :.

---
