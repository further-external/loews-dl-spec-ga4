# Availability Listings Displayed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "availability_listings_displayed",
  "detailed_event": "Availability Listings Displayed",
    "event_data": {
        "finding_method": "<finding_method>",
        "location_id": "<location_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.finding_method|string|The method by which a user arrived at the availability listings displayed|Onsite Search|||||||
|event_data.location_id|string|Captures the Location Id requested in search criteria.|155, 65588, 987764448|||||||




