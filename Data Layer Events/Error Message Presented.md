# Error Message Presented

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "site_error",
  "detailed_event": "Error Message Presented",
    "event_data": {
        "error_message": "<error_message>",
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.error_message|string|Captures the specific error ID or description associated with errors. |Credit Card Authorization Failed, EC345, Form is incomplete|||||||
|event_data.type|string|Captures the type of error.|Payment, System, Form|||||||




