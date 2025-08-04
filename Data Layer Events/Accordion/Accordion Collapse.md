# Accordion Collapse

Fire whenever a user collapses an accordion item.

## Javascript Code

```js
// When:
// User collapses accordion item.

// Code:
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  event: "accordion_collapse",
  detailed_event: "Accordion Collapse",
  event_data: {
    identifier: "<identifier>", // REQUIRED | string | ex. 12345abcde12345
    name: "<name>", // REQUIRED | string | ex. Where To Begin, Having Important Conversations, Financial Options
    heading: "<heading>", // REQUIRED | string | ex. How to Get Started
    index: "<index>", // contextual | integer | ex. 1 | min. lgth. 1 | min. 1
    type: "<type>" // contextual | string | ex. FAQ
  }
});
```

## Variable Definitions

|Field|Type|Required|Description|Example|Minimum Length|Maximum Length|Minimum|
| --- | --- | --- | --- | --- | --- | --- | --- |
|**event_data.identifier**|`string`|required|The computer-readable machine name of the accordion. Use UUID provided by the component.|`12345abcde12345`||`100`|
|**event_data.name**|`string`|required|The human-readable name of the accordion. If user does not input one, populate with numerical index of which accordion this is on the page (1-indexed). FAQs are the big one that currently need to be broken out in reporting, so getting a name for those should be the priority.|`Where To Begin`<br>`Having Important Conversations`<br>`Financial Options`||`100`|
|**event_data.heading**|`string`|required|The text heading of the accordion item that was opened/closed|`How to Get Started`||`100`|
|**event_data.index**|`integer`|contextual|The ordinal slot number of the accordion item. E.g. - the top item in the accordion will be slot 1. (1-indexed)|1|`1`|`100`|1|
|**event_data.type**|`string`|contextual|The type of accordion.|`FAQ`<br>`Ingrediant Type`||`100`|
