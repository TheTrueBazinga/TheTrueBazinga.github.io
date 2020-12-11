---
layout: default
title: Consumers
parent: Users
nav_order: 2
---


## Consumer

**API LINK:**  https://consumerapi.docs.apiary.io/#

List of all routes:
* [Register](#Register)
* [Login](#Login)
* [Update Password](#Update-Password)
* [Reset Password](#Reset-Password)
* [List all consumers](#-List-all-consumers)



____

### Register 
* **POST https://nite-apigateway.herokuapp.com/users/consumer** - Create consumer profile
```js
req.body = {
    name: String,
    email: String,
    password: String,
    birth: Date,
    phone: String
}
```
____

### Login
* **POST https://nite-apigateway.herokuapp.com/users/consumer/login** - Consumer login
```js
req.body = {
    email: String,
    password: String
}
```
____

### Update Password
* **POST https://nite-apigateway.herokuapp.com/users/consumer/resetPassword** - Consumer update password

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    password: String
}
```
____

### Reset Password
* **GET https://nite-apigateway.herokuapp.com/users/consumer/sendMail?email=** - Ask email to resetPassword

Email in `req.query`.

____

### List all consumers
* **GET https://nite-apigateway.herokuapp.com/users/consumer** - List all consumers 

```js
headers: { Authorization: `Bearer ${token}` }
``` 

