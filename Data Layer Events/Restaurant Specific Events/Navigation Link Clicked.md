# Navigation Link Clicked

Event that captures when user engages with the sites navigation feature (header nav, footer nav, hamburger nav, etc.) 

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "Navigation Link Clicked",
    "event_data": {
        "component_ancestry": "<component_ancestry>",
        "identifier": "<identifier>",
        "link_url": "<link_url>",
        "region_ancestry": "<region_ancestry>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.component_ancestry|string|Captures the name or ID of the container within which navigation links are used.|Best Friends - Best Jeans, Puppy Love, Sail Away, Mens, Kids, Kids : Tops|||||||
|event_data.identifier|string|Captures the name or ID of the navigation links used.|act now, cancel, ok, 3456, 8765|||||||
|event_data.link_url|string|Captures the site destination of the navigation links used.|https:\/\/www.example.com|||||||
|event_data.region_ancestry|string|Captures the name or ID of the region within which navigation links are used.|Top Nav, Footer Nav, Hero, Recommended, Also Shopped, Also Bought|||||||
