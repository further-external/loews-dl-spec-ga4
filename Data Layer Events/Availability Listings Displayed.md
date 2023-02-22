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
|event_data.location_id|string|Captures the Location Id. Please refer to this document to determine location ID.
https:\/\/docs.google.com\/spreadsheets\/d\/1PDhNOzXI9E7jZ9obejV4owtW3Wtwq66\_IaN-CBoHbRs\/edit\#gid=1543857253|6558, 70561|||||||

## Attached Notes

<p>This should fire when a user is presented with the option to select dates for their booking.</p>
