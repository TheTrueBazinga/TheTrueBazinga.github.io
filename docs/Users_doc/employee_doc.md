---
layout: default
title: Employee
parent: Users
nav_order: 2
---

## Employee

**API LINK:** https://employeeapidocumentation.docs.apiary.io/#

List of all routes:
* [Register](#register)
* [Login](#login)
* [Reset Password](#reset-password)
* [Update info](#update-info)
* [Update email](#update-email)
* [Update password](#update-password)
* [Get own info](#get-own-info)
* [Reset password](#reset-password)

____

### Register


This route will send an email to employee with his first password.

* **POST https://nite-apigateway.herokuapp.com/users/employee** - Create employee profile

```js
headers: { Authorization: `Bearer ${token}` }
``` 
Requires token from manager.


```js
req.body = {
    name: String,
    email: String,
    birth: Date,
    job: String,
    establishment: String,
    phone: String,
    address: String
}
```
___

### Login

* **POST https://nite-apigateway.herokuapp.com/users/employee/login** - Employee login
```js
req.body = {
    email: String,
    password: String
}
```
____

### Reset password
* **POST https://nite-apigateway.herokuapp.com/users/employee/resetPassword** - Employee reset Password

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

* **PUT https://nite-apigateway.herokuapp.com/users/employee** - Update employee info


```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    name: String,
    email: String,
    phone: String,
    birth: Date,
    password: String
}
```

____

### Update email

* **PUT https://nite-apigateway.herokuapp.com/users/employee/email** - Update employee email


```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body={
    email: String
}
```

____

### Update password

* **PUT https://nite-apigateway.herokuapp.com/users/employee/password** - Update employee password


```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body={
    oldPassword: String,
    newPassword: String
}
```
____

### Get own info

* **GET https://nite-apigateway.herokuapp.com/users/employee** - Get own info


```js
headers: { Authorization: `Bearer ${token}` }
``` 

____

### Reset password

* **GET https://nite-apigateway.herokuapp.com/users/employee/sendMail?email=** - Ask email to resetPassword

Email in `req.query`.

____
