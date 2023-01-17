# User Signed Out

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "logout",
  "detailed_event": "User Signed Out",
    "detailed_event": "<detailed_event>",
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|detailed_event|string|captures the "detailed\_event" name||||||||
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||




