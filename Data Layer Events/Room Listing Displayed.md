# Room Listing Displayed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "view_item_list",
  "detailed_event": "Room Listing Displayed",
    "detailed_event": "<detailed_event>",
    "ecommerce": {
        "item_list_id": "<item_list_id>",
        "item_list_name": "<item_list_name>",
        "items": [
            {
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "location_id": "<location_id>",
                "room_type_code": "<room_type_code>"
            }
        ]
    },
    "event_data": {
        "facets": "<facets>",
        "listing_driver": "<listing_driver>",
        "listing_filter_count": <listing_filter_count>,
        "number_of_items": <number_of_items>,
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|detailed_event|string|captures the "detailed\_event" name||||||||
|ecommerce.item_list_id|string|The computer-readable machine name of the list the item showed up in \(if sent with a view\_item\_list event\). Use UUID provided by the component if no more specific ID is available.|12345abcde12345|||||||
|ecommerce.item_list_name|string|The human-readable name of the item list the item showed up in \(if sent with a view\_item\_list event\). If one is not available, populate with numerical index of which list this is on the page \(1-indexed\). For filter\_by\_group component, use that value.|filter\_by\_group, recommended\_products, recently\_viewed\_products|||||||
|ecommerce.items[n].item_id|string|Item ID \(context-specific\).The product primary ID \(SKU or UPC\)|SKU\_12345|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|jeggings|||||||
|ecommerce.items[n].location_id|string|The location associated with the event. If possible, set to the Google Place ID that corresponds to the associated item. Can also be overridden to a custom location ID string.|L\_12345|||||||
|ecommerce.items[n].room_type_code|string|captures the room type code of the booking||||||||
|event_data.facets|string|Details filters used to refine a listing|sort\~price ascending\|color\~green\|size\~medium|||||||
|event_data.listing_driver|string|Listing Driver|Onsite Search, Curated Assortment, Navigation|||||||
|event_data.listing_filter_count|integer|Captures the number of filters applied to a listing.|0, 20, 12|||||||
|event_data.number_of_items|integer|Count of rooms returned in room listings.|1, 21, 111, 166|||||||
|event_data.type|string|Captures the methods that bring users to listings \(i.e. Onsite Search, Top Nav, External Link, Category Landing Page\). Does not update if listings are sorted, filtered, or paginated.|Product, Location, Event, Room, Content|||||||




