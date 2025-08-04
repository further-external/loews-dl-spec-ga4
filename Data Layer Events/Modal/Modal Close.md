# Modal Close

Send when users manually close a modal, usually with an icon like an "X" or "close".

## Javascript Code

```js
// When:
// Send when users manually close a modal, usually with an icon like an "X" or "close".

// Code:
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
event: 'modal_close',
detailed_event: 'Model Close',
event_data: {
  modal_name: "<modal_name>", // REQUIRED | string | ex. "privacy_settings"
  step_name: "<step_name>", // contextual | string | ex. "We Value Your Privacy"
  step_number: "<step_number>", // contextual | integer | ex. 1
  }
});
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
```

## Variable Definitions

| Field                         | Type      | Required | Description | Example                   | Pattern | Min Length | Max Length | Minimum | Maximum | Multiple Of |
|-------------------------------|-----------|----------|-------------|---------------------------|---------|------------|------------|---------|---------|-------------|
| **event_data.modal_name**     | `string`  | required | The name of the modal being viewed | `privacy_setting` | | | `500` | | | |
| **event_data.step_name**      | `string`  | contextual | The name of the step users are interacting with when the m odal contains multiple steps/interactions. This is to be used if there are multiple "screens" within the modal experience to help understand funnel success/abandonment. | `We Value Your Privacy` | | | `500` | | | |
| **event_data.step_number**    | `integer` | contextual | Step number in a predefined form flow; should match the step number shown to users on the page. This is to be used if there are multiple "screens" within the modal experience to help understand funnel success/abandonment. | `1` | | | `500` | `0` | | |
