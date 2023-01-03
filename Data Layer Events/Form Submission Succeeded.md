# Form Submission Succeeded

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "form_complete",
  "detailed_event": "Form Submission Succeeded",
    "ecommerce": {
        "items": [
            {
                "location_id": "<location_id>"
            }
        ]
    },
    "event_data": {
        "event_type": "<event_type>",
        "identifier": "<identifier>",
        "rfp_event_destination": "<rfp_event_destination>",
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.items[n].location_id|string|Captures a unique ID of a physical location such as a store, banking branch, atm, hotel, office, or other.|155, 65588, 987764448|||||||
|event_data.event_type|string|Type of event an RFP is submitted for|meeting, wedding, social|||||||
|event_data.identifier|string|Captures the unique ID of the form.|F-0113, 2543, CU001, PI-0988|||||||
|event_data.rfp_event_destination|string|Specific hotel an RFP is booked for||||||||
|event_data.type|string|Captures the type of form \(i.e. demo, free trial, contact us\).|Address, Contact, Comment, Review, Payment|||||||




