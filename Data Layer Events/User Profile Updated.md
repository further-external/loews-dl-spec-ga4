# User Profile Updated

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "update_profile",
  "detailed_event": "User Profile Updated",
    "event_data": {
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.type|string|Captures the type of profile update \(i.e. change email\) completed by the user.|email, address, phone, subscriptions|||||||




