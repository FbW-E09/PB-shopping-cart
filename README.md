# Shopping Cart

Create 2 classes:

- Product: a simple class to represent products containing the properties `name` and `price`
- Cart: a class store products and manage the shopping cart of an e-commerce website.

## Cart
### Fields
- `items`: the cart should have an `items` property to store the products that a customer wants to buy

### Methods

- `list()`: this method should output a nicely formatted list of all the products in the cart to the console (see example below)
- `add(product)`: the `add` method accepts a `product` object as input and adds it to the cart. Besides saving the product in the `items` array, the `add` method also sets the quantity for the item: if an item with the same name is already in the cart, it just increases its quantity, otherwise it sets it to 1
- `remove(name)`: finds a cart item by name and decreases the quantity by 1. If the quantity becomes 0, completely removes the item from the cart
- `getTotal()`: prints the total cost of the items in the cart. The total should take into account also the quantity of each item
- `shippingCost()`: it returns 0 if the total of the cart is more than 100. Otherwise it returns 4.9, if the number of items in the cart is less than 5. If it's more, then it returns 9.9

## Example

```
let myCart = new Cart();
let shoes = new Product("shoes", 15.99);
let shirt = new Product("shirt", 25.99);
let jeans = new Product("jeans", 29.99);

myCart.add(shoes);
myCart.add(shirt);
myCart.add(shirt);
myCart.add(jeans);

myCart.list()
console.log(myCart.getTotal());
```

```
// myCart.list() output

Cart:
----------

Item: shoes
Price: 15.99€
Quantity: 1
Subtotal: 15.99€

---

Item: shirt
Price: 25.99€
Quantity: 2
Subtotal: 51.98€

---

Item: jeans
Price: 29.99€
Quantity: 1
Subtotal: 29.99€

----------
Total: 97.96€
```
