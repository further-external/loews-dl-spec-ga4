# User Detected

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "detect_user",
  "detailed_event": "User Detected",
    "user_data": {
        "user_login_state": "<user_login_state>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user_data.user_login_state|string|Captures the current sign in status for the user \(i.e. signed\_out, signed\_in, unknown\).|logged in, logged out, guest|||||||

## Attached Notes

<p>This is information about the user. &nbsp;We will want to fire the events in this sequence.<br />Page Load Started &gt; User Detected &gt; Page Load Completed</p>
