# Backend API Documentation

## `/users/register` Endpoint

### Description

Registers a new user by creating a user account with the provided information.

### HTTP Method

`POST`

### Request Body

The request body should be in JSON format and include the following fields:

- `fullname` (object):
  - `firstname` (string, required): User's firstname (minimum 3 characters).
  - `lastname` (string, optional): User's lastname (minimum 3 characters).
- `email` (string, required): User's email address (must be a valid email).
- `password` (string, required): User's password (minimum 6 characters).

### Example Response

- `user` (object):
  - `fullname` (object).
    - `firstname` (string): User's firstname (minimum 3 characters).
    - `lastname` (string): User's lastname (minimum 3 characters).
  - `email` (string): User's email address (must be a valid email).
  - `password` (string): User's password (minimum 6 characters).
- `token` (string): JWT Token 

## `/users/login` Endpoint

### Description

Authenticates a user using their email and password, returning a JWT token upon successful verification of their credentials.

### HTTP Method

`POST`

### Endpoint

`/users/login`

### Request Body

The request body should be in JSON format and include the following fields:

- `email` (string, required): User's email address (must be a valid email).
- `password` (string, required): User's password (minimum 6 characters).

### Example Response

- `user` (object):
  - `fullname` (object).
    - `firstname` (string): User's firstname (minimum 3 characters).
    - `lastname` (string): User's lastname (minimum 3 characters).
  - `email` (string): User's email address (must be a valid email).
  - `password` (string): User's password (minimum 6 characters).
- `token` (string): JWT Token

## `/users/profile` Endpoint

### Description

Retrieves the profile information of the currently authenticated user.

### HTTP Method

`GET`

### Authentication

Requires a valid JWT token in the Authentication header:
`Authorization: Bearer <token>`

### Example Response

- `user` (object):
  - `fullname` (object).
    - `firstname` (string): User's firstname (minimum 3 characters).
    - `lastname` (string): User's lastname (minimum 3 characters).
  - `email` (string): User's email address (must be a valid email).


## `/users/logout` Endpoint

### Description

Logout the current user and blacklist the token provided in cookie or headers.

### HTTP Method

`GET`

### Authentication

Requires a valid JWT token in the Authentication header or cookie:

## `/captain/register` Endpoint

### Description

Requires a new captain by creating a captain account with the provided information.

### HTTP Method

`POST`

### Request Body

The request body should be in JSON format and include the following fields:

- `fullname` (object):
  - `firstname` (string, required): Captain's first name (minimum 3 characters)
  - `lastname` (string, optional): Captain's last name (minimum 3 characters)
- `email` (string, required): Captain's email address (must be a valid email)
- `password` (string, required): Captain's password (minimum 6 characters)
- `vehicle` (object):
  - `color` (string, required): Vehicle color (minimum 3 characters)
  - `plate` (string, required): Vehicle plate number (minimum 3 characters)
  - `capacity` (number, required): Vehicle passenger capacity (minimum 1)
  - `vehicleType` (string, required): Type of vehicle (must be 'car', 'motorcycle' or 'auto')

### Example Response

- `captain` (object):
  - `fullname` (object).
    - `firstname` (string): User's firstname (minimum 3 characters).
    - `lastname` (string): User's lastname (minimum 3 characters).
  - `email` (string): User's email address (must be a valid email).
  - `password` (string): User's password (minimum 6 characters).
- `vehicle` (object):
  - `color` (string): Vehicle color (minimum 3 characters).
  - `plate` (string): Vehicle plate number (minimum 3 characters).
  - `capacity` (number): Vehicle passenger capacity (minimum 1).
  - `vehicleType` (string): Type of vehicle (must be 'car', 'motorcycle' or 'auto')
- `token` (string): JWT Token