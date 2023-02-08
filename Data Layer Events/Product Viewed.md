# Product Viewed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "view_item",
  "detailed_event": "Product Viewed",
    "ecommerce": {
        "currency": "<currency>",
        "items": [
            {
                "city": "<city>",
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "market_code": "<market_code>",
                "state": "<state>"
            }
        ],
        "value": <value>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.items[n].city|string|city||||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|SKU\_12345|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|jeggings|||||||
|ecommerce.items[n].market_code|string|captures the Market Code of the booking||||||||
|ecommerce.items[n].state|string|State|GA, NY, AZ|||||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||




