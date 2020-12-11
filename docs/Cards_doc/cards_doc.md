---
layout: default
title: Phisical Cards
parent: Cartões
nav_order: 2
---


## Phisical Cards

**API LINK:**

List of all routes:
* [List all cards](#-List-All-Cards)
* [Card Info](#Card-Info)
* [Delete All Establishment cards](#Delete-All-Establishment-Cards)
* [Delete card](#Delete-Card)
* [Create new card](#Create-New-Card)



____

### List All Cards
* **GET https://nite-apigateway.herokuapp.com/cards** - List all cards
```js
headers: { Authorization: `Bearer ${token}` }
``` 


### Card Info
* **GET https://nite-apigateway.herokuapp.com/cards/:id** - List one card info
```js
headers: { Authorization: `Bearer ${token}` }
``` 

### Delete All Establishment Cards
* **DELETE https://nite-apigateway.herokuapp.com/cards/DropAllOrganization** - Delete all cards of his establishment.

THIS ROUTE IS ONLY FOR MANAGERS

```js
headers: { Authorization: `Bearer ${token}` }
``` 

### Delete Card
* **DELETE https://nite-apigateway.herokuapp.com/cards/DeleteCard/:card** - Delete one card of his establishment.

THIS ROUTE IS ONLY FOR MANAGERS

```js
headers: { Authorization: `Bearer ${token}` }
``` 

### Create New Card
* **POST https://nite-apigateway.herokuapp.com/cards/newCard**

THIS ROUTE IS ONLY FOR MANAGERS

```js
headers: { Authorization: `Bearer ${token}` }
``` 
