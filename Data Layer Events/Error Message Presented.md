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

## Attached Notes

<p><span style="font-weight: 400;">When a user select dates through blackout or unavailable dates and an error message appears.&nbsp;</span></p>
<p><span style="font-weight: 400;">Also for any 404 error messages</span></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
