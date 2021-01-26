---
layout: default
title: Digital Cards
parent: Night Club
nav_order: 2
---
## Digital Cards

List of all routes:
* [Creates Digital Card](#creates-digital-card)
* [Connect digital card](#connect-digital-card)
* [Insert Guest Code](#insert-guest-code)
* [Add product in digital card](#add-product-in-digital-card)
* [Change state](#change-state)
* [Change State to Locked](#change-state-to-locked)
* [Change Payment State](#change-payment-state)
* [Get Digital Card info](#get-digital-card-info)
* [Calculate Total](#calculate-total)


____

### Creates Digital Card
* **POST https://nite-apigateway.herokuapp.com/nightClub/digitalCards** - Creates one digital card and connect it with phisical card.

Requires token in header (*Bearer token*) from employee.

```js
req.body = {
    idfcard : String,
    sex: String (optional)
}
```
___

### Connect digital card
* **POST https://nite-apigateway.herokuapp.com/nightClub/digitalCards/connect** - Creates a connection between user and digital card.

Requires token in header (*Bearer token*) from consumer.

```js
req.body = {
    idfcard : String,
}
```
___

### Insert Guest Code
* **POST https://nite-apigateway.herokuapp.com/nightClub/digitalCards/guestCode** - Insert guest code in one digital card.

Requires token in header (*Bearer token*) from consumer.

```js
req.body = {
    idDcard : String,
    idEstablishment: String,
    guest_code: String
}
```
____

### Add product in digital card
* **POST https://nite-apigateway.herokuapp.com/nightClub/digitalCards/product** - Add product in digital card.

Requires token in header (*Bearer token*) from employee.

```js
req.body = {
    idDcard: String,
    idProduto: String,
    nome: String,
    preço: Number,
    categoria: String
}
```
___

### Change State
* **PUT localhost:3000/nightClub/digitalCards/cardState** - Change digital card status

Requires token.

```js
req.body = {
    idEstablishment: String
    idDcard : String
}
```
___

### Change State to Locked
* **PUT localhost:3000/nightClub/digitalCards/cardState/Locked** - Change digital card status to Locked

Requires token from employee.

```js
req.body = {
    idDcard : String
}
```

___

### Change Payment State
* **PUT localhost:3000/nightClub/digitalCards/cardPayment** - Change Digital Card Payment Status

Requires token from employee (or manager)

```js
req.body = {
    idDcard: String
}
```

___
### Get Digital Card info
* **GET https://nite-apigateway.herokuapp.com/nightClub/digitalCards** - Get digital card info.

    * FOR CONSUMER:
        
        Requires token in header (*Bearer token*) from consumer.
        Sends info in query.params (*iddcard* and *idNightClub*): `/digitalCards?iddcard=XXXX&idNightClub=YYYY`
    
    * FOR EMPLOYEE

        Requires token in header (*Bearer token*) from employee.
        Sends info in query.params (*iddcard*): `/digitalCards?iddcard=XXXX`

___

### Calculate total
* **GET https://nite-apigateway.herokuapp.com/nightClub/digitalCards/total** - Calculate total.

Requires token from consumer.

Sends info in query.params (*iddcard* and *idNightClub*): `/digitalCards/total?idNightClub=XXXX&iddcard=YYYY`


