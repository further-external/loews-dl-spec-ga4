# Rate Detail Viewed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "view_item",
  "detailed_event": "Rate Detail Viewed",
    "detailed_event": "<detailed_event>",
    "ecommerce": {
        "items": [
            {
                "arrival_date": "<arrival_date>",
                "departure_date": "<departure_date>",
                "location_id": "<location_id>",
                "market_code": "<market_code>",
                "number_of_adults": <number_of_adults>,
                "number_of_children": <number_of_children>,
                "number_of_rooms": <number_of_rooms>,
                "price": <price>,
                "quantity": <quantity>,
                "room_rate_code": "<room_rate_code>",
                "room_type_code": "<room_type_code>"
            }
        ]
    },
    "event_data": {
        "days_to_start_date": <days_to_start_date>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|detailed_event|string|captures the "detailed\_event" name||||||||
|ecommerce.items[n].arrival_date|string|the arrival date of a booking||||||||
|ecommerce.items[n].departure_date|string|captures Departure Date of the booking||||||||
|ecommerce.items[n].location_id|string|The location associated with the event. If possible, set to the Google Place ID that corresponds to the associated item. Can also be overridden to a custom location ID string.|L\_12345|||||||
|ecommerce.items[n].market_code|string|captures the Market Code of the booking||||||||
|ecommerce.items[n].number_of_adults|integer|Captures the number of adults in a booking||||||||
|ecommerce.items[n].number_of_children|integer|captures the Number of Children in a booking \(ecommerce DE\)||||||||
|ecommerce.items[n].number_of_rooms|integer|Number of Rooms||||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.items[n].room_rate_code|string|captures the rate code of the room||||||||
|ecommerce.items[n].room_type_code|string|captures the room type code of the booking||||||||
|event_data.days_to_start_date|integer|Captures the booking window used in search criteria \(e.g. number of days prior to requested check-in date\).|1, 2, 3, 4, 5||||0|||




