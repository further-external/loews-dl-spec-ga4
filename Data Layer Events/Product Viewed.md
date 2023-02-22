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
|ecommerce.items[n].item_id|string|Please reference this document to determine the Item ID
https:\/\/docs.google.com\/spreadsheets\/d\/1PDhNOzXI9E7jZ9obejV4owtW3Wtwq66\_IaN-CBoHbRs\/edit\#gid=1543857253|6558, 70561|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|jeggings|||||||
|ecommerce.items[n].market_code|string|captures the Market Code of the booking||||||||
|ecommerce.items[n].state|string|State|GA, NY, AZ|||||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||

## Attached Notes

<p>Anytime a users visits a hotel specific url.<br />ex:</p>
<p><a href="https://www.loewshotels.com/live-by-loews-arlington-texas">https://www.loewshotels.com/live-by-loews-arlington-texas</a></p>
<p><a href="https://www.loewshotels.com/live-by-loews-arlington-texas/specials">https://www.loewshotels.com/live-by-loews-arlington-texas/specials</a></p>
<p>&nbsp;</p>
