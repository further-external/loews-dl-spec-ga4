# Interstitial Viewed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "view_interstitial",
  "detailed_event": "Interstitial Viewed",
    "event_data": {
        "interstitial_name": "<interstitial_name>",
        "interstitial_type": "<interstitial_type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.interstitial_name|string|Interstitial Name||||||||
|event_data.interstitial_type|string|Captures the type of interstitial that was shown to visitors.|alert, offer, info required|||||||

## Attached Notes

<p>Users views an interstitial<br />ex: Click "cancellation policy" or other popup on final booking page ("Review &amp; Book")</p>
