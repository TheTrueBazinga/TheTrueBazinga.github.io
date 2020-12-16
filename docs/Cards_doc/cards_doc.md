---
layout: default
title: Cards
parent: Cards
nav_order: 2
---
## Phisical Cards

**API LINK:**

List of all routes:
* [List all cards](#-List-All-Cards)
* [Card Info](#Card-Info)
* [All Available](#All-Available)
* [Available cards from one establishment](#Available-cards-from-one-establishment)
* [Delete All Establishment cards](#Delete-All-Establishment-Cards)
* [Delete card](#Delete-Card)
* [Create new card](#Create-New-Card)
* [Change Card Availability](#Change-Card-Availability)
* [Change Card Circulation](#Change-Card-Circulation)



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
```}
