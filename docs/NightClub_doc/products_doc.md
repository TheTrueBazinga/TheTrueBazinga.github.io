---
layout: default
title: Products
parent: Night Club
nav_order: 2
---
## Products

List of all routes:
* [List all products](#list-all-products)
* [Update product](#update-product)
* [Create new product](#create-new-product)
* [Delete product](#delete-product)

___

### List All Products

* **GET https://nite-apigateway.herokuapp.com/nightClub/products/** - List all products

Requires token in header (*Bearer token*) from employee or manager.


___

### Update product

* **PUT https://nite-apigateway.herokuapp.com/nightClub/products/{id}** - Update a product

Requires token from manager.

```js
req.body = {
    product_name: String,
    product_category: String,
    product_price: Number
}
```

___

### Create new product
* **POST https://nite-apigateway.herokuapp.com/nightClub/products/** - Create new product

Requires token from manager.

```js
req.body = {
    product_name: String,
    product_category: String,
    product_price: Number
}
```

___

### Delete-product
* **DELETE https://nite-apigateway.herokuapp.com/nightClub/products/{id}** - Deletes product

Requires token from manager
