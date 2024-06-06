# Accommodation Booking Cancelled

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "refund",
  "detailed_event": "Accommodation Booking Cancelled",
    "ecommerce": {
        "transaction_id": "<transaction_id>",
        "value": <value>,
        "currency": "<currency>",
        "items": [
            {
                "cancel_advance_days": "<cancel_advance_days>",
                "cancel_days_after_booking": "<cancel_days_after_booking>",
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "market_code": "<market_code>",
                "number_of_adults": <number_of_adults>,
                "number_of_children": <number_of_children>,
                "price": <price>,
                "room_rate_code": "<room_rate_code>",
                "room_type_code": "<room_type_code>"
            }
        ]
    },
    "event_data": {
        "cancellation_id": "<cancellation_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.items[n].cancel_advance_days|string|How many days in advance a booking was canceled||||||||
|ecommerce.items[n].cancel_days_after_booking|string|How many days after a booking was made it was canceled||||||||
|ecommerce.items[n].item_id|string|Please reference this document to determine the Item ID
https:\/\/docs.google.com\/spreadsheets\/d\/1PDhNOzXI9E7jZ9obejV4owtW3Wtwq66\_IaN-CBoHbRs\/edit\#gid=1543857253|6558, 70561|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|jeggings|||||||
|ecommerce.items[n].market_code|string|captures the Market Code of the booking||||||||
|ecommerce.items[n].number_of_adults|integer|Captures the number of adults in a booking||||||||
|ecommerce.items[n].number_of_children|integer|captures the Number of Children in a booking \(ecommerce DE\)||||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].room_rate_code|string|captures the rate code of the room||||||||
|ecommerce.items[n].room_type_code|string|captures the room type code of the booking||||||||
|ecommerce.transaction_id|string|The unique identifier of a transaction.|T\_12345, 19283j2nm9jdjs|^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||
|event_data.cancellation_id|string|Captures the confirmation number associated with each booking cancellation.||||||||

## Attached Notes

<p>This event should fire when a booking is cancelled.</p>
<p>Please populate the user personal data encripted once it is captured(user creates an account/user provides guest information at checkout process) </p>
