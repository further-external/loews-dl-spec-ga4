# Form Submission Failed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "form_error",
  "detailed_event": "Form Submission Failed",
    "event_data": {
        "error_message": "<error_message>",
        "event_type": "<event_type>",
        "identifier": "<identifier>",
        "location_id": "<location_id>",
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.error_message|string|Captures the form error code or message associated with form errors.|Credit card declined, Required entries missing, EC3456, EC8976|||||||
|event_data.event_type|string|Type of event an RFP is submitted for|meeting, wedding, social|||||||
|event_data.identifier|string|Captures the unique ID of the form.|F-0113, 2543, CU001, PI-0988|||||||
|event_data.location_id|string|Captures the Location Id|155, 65588, 987764448|||||||
|event_data.type|string|Captures the type of form \(i.e. RFP, demo, free trial, contact us\).|Address, Contact, Comment, Review, Payment|||||||




