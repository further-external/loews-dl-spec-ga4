# Exit Link Clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "Exit Link Clicked",
    "event_data": {
        "identifier": "<identifier>",
        "link_url": "<link_url>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the ID associated with exit links used. |act now, cancel, ok, 3456, 8765|||||||
|event_data.link_url|string|Captures the URL of the exit link.|https:\/\/www.usda.gov. https:\/\/msnbc.com|||||||




