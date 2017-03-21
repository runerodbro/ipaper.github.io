---
permalink: /javascript-api/publication
title: Publication (Event Dispatcher)
redirect_from: "/display/DOC/Publication"
---

The publication event dispatcher contains methods for listening to and interacting with the publication in Flipbooks.

## Events
These are events that you can listen for using the addEventListener() method on the event dispatcher.

### onPageElementClicked

Fired when a pageelement is "clicked".
{% include note.html content="Current only shopitems will fire this event!" %}

**Sample data**:

```javascript
{
    type: 'shopitem',
    data: {
        title: 'Coca Cola',
        description: 'Carbonated soft drink ',
        productID: 'C1',
        price: 9.95,
        amountselection: true|false,
        packagesize: 1
    },
    event: {
        originSpreadPages: [4,5],
        coordinates: {
            pageX: 525,
            pageY: 250,
            bookX: 0.523234,
            bookY: 0.124543
        }
    }
}
```

**Return values**:

```javascript
{
    preventDefault: true // If set to true, the item will not be added to the Flipbook basket.
}
```

### onSpreadChanged
Fired when the current spread changes.

**Sample data:**

```javascript
{
    currentSpreadPages: [4,5]
}
```

## Methods
These are methods that you can call on the event dispatcher.

### gotoPage

Navigates to the specified page.

**Sample:**

```javascript
api.Publication.gotoPage(5);
```