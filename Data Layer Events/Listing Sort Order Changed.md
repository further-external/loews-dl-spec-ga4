# Listing Sort Order Changed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "sort_list",
  "detailed_event": "Listing Sort Order Changed",
    "detailed_event": "<detailed_event>",
    "event_data": {
        "sort_order": <sort_order>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|detailed_event|string|captures the "detailed\_event" name||||||||
|event_data.sort_order|number|The sort value selected by the user on listings.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||




