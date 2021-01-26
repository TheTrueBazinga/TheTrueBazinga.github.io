---
layout: default
title: Consumers
parent: Users
nav_order: 2
---


## Consumer

**API LINK:**  https://consumerapi.docs.apiary.io/#

List of all routes:
* [Register](#register)
* [Login](#login)
* [Update Password](#update-password)
* [Update Info](#update-info)
* [Reset Password](#reset-password)
* [Update password](#update-password)
* [List all consumers](#list-all-consumers)
* [Own Historic](#get-historic)



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

### Update info
* **PUT https://nite-apigateway.herokuapp.com/users/consumer** - Consumer update own info

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    name: String,
    email: String,
    phone: String,
    birth: Date
}
```
____

### Update Password
* **PUT https://nite-apigateway.herokuapp.com/users/consumer/password** - Update consumer 
password.

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    oldPassword: String,
    newPassword: String
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

___

### Get Historic
* **GET https://nite-apigateway.herokuapp.com/users/consumer/historic** - Get own historic

```js
headers: { Authorization: `Bearer ${token}` }
``` 