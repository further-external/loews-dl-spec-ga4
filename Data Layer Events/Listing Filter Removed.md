# Listing Filter Removed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "filter_remove",
  "detailed_event": "Listing Filter Removed",
    "detailed_event": "<detailed_event>",
    "event_data": {
        "facets": "<facets>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|detailed_event|string|captures the "detailed\_event" name||||||||
|event_data.facets|string|Details filters used to refine a listing|sort\~price ascending\|color\~green\|size\~medium|||||||




