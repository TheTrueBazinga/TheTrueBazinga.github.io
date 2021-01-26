---
layout: default
title: Phisical Cards
parent: Cards
nav_order: 2
---

## Phisical Cards

**API LINK:**

List of all routes:
* [List all cards](#list-all-cards)
* [Card Info](#card-info)
* [All Available](#all-available)
* [Available cards from one establishment](#available-cards-from-one-establishment)
* [Delete All Establishment cards](#delete-all-establishment-cards)
* [Delete card](#delete-card)
* [Create new card](#create-new-card)
* [Change Card Availability](#change-card-availability)
* [Change Card Circulation](#change-card-circulation)
* [Reset](#reset)



____

### List All Cards
* **GET https://nite-apigateway.herokuapp.com/cards** - List all cards
```js
headers: { Authorization: `Bearer ${token}` }
``` 


### All Available
* **GET https://nite-apigateway.herokuapp.com/cards/AllAvailable** - List all available cards
```js
headers: { Authorization: `Bearer ${token}` }
``` 

### Available cards from one establishment 
* **GET https://nite-apigateway.herokuapp.com/cards/Available** - List all available cards from one establishment

ONLY FOR MANAGERS

```js
headers: { Authorization: `Bearer ${token}` }
``` 

### Card Info
* **GET https://nite-apigateway.herokuapp.com/cards/** - List one card info
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
* **POST https://nite-apigateway.herokuapp.com/cards/newCard** - New phisical card

THIS ROUTE IS ONLY FOR MANAGERS

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    idfcard: String
}
```

### Change Card Availability
* **PUT https://nite-apigateway.herokuapp.com/cards/Availability** - Update card's availability

THIS ROUTE IS ONLY FOR MANAGERS

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    id: String,
    availability: Boolean
}
```

### Change Card Circulation
* **PUT https://nite-apigateway.herokuapp.com/cards/Circulation** - Update card's circulation

THIS ROUTE IS ONLY FOR MANAGERS

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    id: String,
    circulating: Boolean
}
```

### Reset
* **PUT https://nite-apigateway.herokuapp.com/cards/Reset** - Reset one fcard

THIS ROUTE IS ONLY FOR MANAGERS AND EMPLOYEES

```js
headers: { Authorization: `Bearer ${token}` }
``` 

```js
req.body = {
    idfcard: String
}
```
