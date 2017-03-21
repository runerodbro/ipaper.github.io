---
permalink: /javascript-api/shop
title: Shop (Event Dispatcher)
redirect_from: "/display/DOC/Shop"
---

The shop event dispatchers contains methods for listening to and interacting with the shop module in Flipbook.

## Events
These are events that you can listen for using the addEventListener() method on the event dispatcher.

### addItem

Fired when a shop item is added to the basket.

**Sample data**:

```javascript
{
    title: 'My product',
    description: 'Product description',
    productID: 'PROD-25B',
    price: '29.95',
    originPage: 6
}
```

**Return values**:

```javascript
{
    preventDefault: true // If set to true, the item will not be added to the Flipbook basket.
}
```

### onBasketClick
Fired when the open basket icon is clicked in the Flipbook.

**Return values:**

```javascript
{
    preventDefault: true // If set to true, the basket will not be opened.
}
```

## Methods
These are methods that you can call on the event dispatcher.

### addItem

Adds an item to the Flipbook basket.

**Sample:**

```javascript
api.Shop.addItem({
    title: 'My product',
    description: 'Product description',
    productID: 'PROD-25B',
    price: '29.95',
    originPage: 6,
    quantity: 1
});
```