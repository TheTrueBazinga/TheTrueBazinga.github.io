---
layout: default
title: Payments
parent: Payments
nav_order: 2
---

## Payments

List of all routes:
* [Create Payment](#create-payment)
* [Cancel Payment](#cancel-payment)
* [Confirm Payment](#confirm-payment)
* [Create Credit Card Token](#create-credit-card-token)
* [Get Payment Info ](#get-payment-info)

___

### Create Payment

* **POST https://nite-apigateway.herokuapp.com/payments/createPayment/** - Create Payment ref

Requires token in header (*Bearer token*) from user.

```js
req.body = {
    idNightClub: String,
    iddcard: String,
    method: String
} 
```

Returns:
```js
res = {
    ref: String,
    total: Number
}
```

___

### Cancel Payment

* **POST https://nite-apigateway.herokuapp.com/payments/cancelPayment** - Cancel payment

Requires token in header (*Bearer token*) from user.

```js
req.body = {
    idNightClub: String,
    iddcard: String,
    ref: String
} 
```

___

### Confirm Payment

* **POST https://nite-apigateway.herokuapp.com/payments/confirmPayment** - Confirm payment
Requires token in header (*Bearer token*) from user.

```js
req.body = {
    idNightClub: String,
    iddcard: String,
    ccard_number: String,
    ccard_expMonth: Number,
    ccard_expYear: Number,
    ccard_cvc: String,
    ref: String
} 
```

Dados para testar: 
```json
    ccard_number: '4242424242424242',
    ccard_expMonth: 1,
    ccard_expYear: 2022,
    ccard_cvc: '314'
```

___

### Create Credit Card Token

* **GET https://nite-apigateway.herokuapp.com/payments/hide/hide/hide/stripeCCToken** - Cria um stripe token do cartão de pagamento

Não precisa de nenhum parametro nem token, esta rota só serve para criar um token com o cartão de teste do stripe.

___

### Get Payment Info 

* **GET https://nite-apigateway.herokuapp.com/payments/getPaymentInfo?ref=XXX** - Obtem info de uma dada ref

Requires token in header(*Bearer token*) from user.