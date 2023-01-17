# User Registered

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "sign_up",
  "detailed_event": "User Registered",
    "detailed_event": "<detailed_event>",
    "event_data": {
        "method": "<method>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|detailed_event|string|captures the "detailed\_event" name||||||||
|event_data.method|string|Captures the website method \(i.e. search, top nav\) used to find each product.|email, facebook, twitter|||||||
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||




