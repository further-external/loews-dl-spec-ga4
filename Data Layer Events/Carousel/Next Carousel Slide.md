# Next Carousel Slide

Fire whenever a user interacts with the next carousel slide control

## Javascript Code

```js
// When:
// User interacts with 'next' carousel slide control

// Code:
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  event: 'carousel_slide_next',
  detailed_event: 'Next Carousel Slide',
  event_data: {
    identifier: "<identifier>",
    name: "<name>"
  }
});
```

## Variable Definitions

|Path|Type|Description|Example|Minimum Length|Maximum Length|Minimum|
| --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|The computer-readable machine name of the carousel. Use UUID provided by the component|`12345abcde12345`||`100`||
|event_data.name|string|The human-readable name of the carousel. If user does not input one, populate with numerical index of which carousel this is on the page (1-indexed)|`Most Popular Blog Posts`,`Homepage Main Content`||`100`||
