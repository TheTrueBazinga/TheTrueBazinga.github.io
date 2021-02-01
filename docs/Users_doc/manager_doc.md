---
layout: default
title: Manager
parent: Users
nav_order: 2
---


## Manager

**API LINK:**  https://managerapidocumentation.docs.apiary.io/#


All routes:
* [Login](#login)
* [Register](#register)
* [Reset Password](#reset-password)
* [Update Employee info](#update-employee-info)
* [Update password](#update-password)
* [Update email](#update-email)
* [Update own info](#update-own-info)
* [Delete manager](#delete-manager)
* [Delete employee](#delete-employee)
* [Get own info](#get-own-info)
* [Reset Password](#reset-password)
* [List all employes](#list-all-employees)

____

### Login
* **POST https://nite-apigateway.herokuapp.com/users/manager/login** - Manager Login
```js
req.body = {
    email: String,
    password: String
}
```
____

### Register
* **POST https://nite-apigateway.herokuapp.com/users/manager/** - Create manager profile
```js
req.body = {
    name: String,
    email: String,
    password: String,
    establishment: String,
    phone: String,
    address: String,
    birth : Date
}
```
____

### Reset Password
* **POST https://nite-apigateway.herokuapp.com/users/manager/resetPassword** - Manager reset Password

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    password: String
}
```
_____

### Update Employee info
* **PUT https://nite-apigateway.herokuapp.com/users/manager/employee/:employee_id** - Update employee info

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body={
    name: String
    birth: Date
    job: String
    email: String
    establishment: String
    phone: String
    address: String
}
```
_____

### Update password
* **PUT https://nite-apigateway.herokuapp.com/users/manager/password** - Update manager password

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body={
    oldPassword: String,
    newPassword: String
}
```
_____

### Update email
* **PUT https://nite-apigateway.herokuapp.com/users/manager/email** - Update manager email

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body={
    email: String
}
```
_____

### Update own info
* **PUT https://nite-apigateway.herokuapp.com/users/manager** - Update manager own info

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body={
    name: String,
    address: String,
    birth: Date,
    phone: String,
    establishment: String
}
```
_____

### Delete manager
* **DELETE https://nite-apigateway.herokuapp.com/users/manager** - Delete a manager

```js
headers: { Authorization: `Bearer ${token}` }
``` 
_____

### Delete employee
* **DELETE https://nite-apigateway.herokuapp.com/users/manager/employee/:idEmployee** - Delete employee

```js
headers: { Authorization: `Bearer ${token}` }
``` 

_____


### Get own info
* **GET https://nite-apigateway.herokuapp.com/users/manager/** - Get manager own info

```js
headers: { Authorization: `Bearer ${token}` }
``` 
_____

### Reset Password
* **GET https://nite-apigateway.herokuapp.com/users/manager/sendMail?email=** - Ask email to resetPassword

Email in `req.query`.

____


### List all employees
* **GET https://nite-apigateway.herokuapp.com/users/manager/employees** - List all employees

```js
headers: { Authorization: `Bearer ${token}` }
``` 
____
