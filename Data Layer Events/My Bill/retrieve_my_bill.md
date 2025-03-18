# Retrieve My Bill

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "retrieve_my_bill",
  "detailed_event": "Retrieve My Bill",
    "event_data": {
        "identifier": "<identifier>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the ID associated with download links used.|act now, cancel, ok, 3456, 8765|||||||

## Attached Notes

<p>When a user clicks a link that requests options to retrieve a document within the My Bill experience.<br />ex: Click "Retrieve My Bill" after entering your information here: https://www.loewshotels.com/bill</p>
