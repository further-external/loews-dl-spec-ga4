# Download Link Clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "file_download",
  "detailed_event": "Download Link Clicked",
    "event_data": {
        "file_name": "<file_name>",
        "identifier": "<identifier>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.file_name|string|Captures the file name associated with file downloads.|Year End 2012.pdf, Operating Instructions.doc`|||||||
|event_data.identifier|string|Captures the ID associated with download links used.|act now, cancel, ok, 3456, 8765|||||||

## Attached Notes

<p>When a user clicks a link that downloads a document.<br />ex: Click "Catering Menu" here: https://www.loewshotels.com/coral-gables/meetings/function-space</p>
