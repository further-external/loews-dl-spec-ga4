# Modal CTA Click

Send when users engage with a call to action within a modal, prompting them to complete additional information. This event will include the same information that was sent with the model_view event, but will include CTA specific details.

## Javascript Code

```js
// When:
// Fire when users engage with a call to action within a modal, prompting them to complete additional information.

// Code:
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  event: 'modal_cta_click',
  detailed_event: 'Model CTA Click',
  event_data: {
    modal_name: '<modal_name>', // REQUIRED | string | ex. "privacy_settings"
    step_name: '<step_name>', // contextual | string | ex. "We Value Your Privacy"
    step_number: '<step_number>', // contextual | integer | ex. 1
    cta_text: '<cta_text>', // contextual | string | ex."Go To Link"
    cta_outbound: '<cta_outbound>' // required | ex. true, false
  }
});
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
```

## Variable Definitions

| Field              | Type      | Required | Description | Example                   | Pattern | Min Length | Max Length | Minimum | Maximum | Multiple Of |
|--------------------|-----------|----------|-------------|---------------------------|---------|------------|------------|---------|---------|-------------|
| **modal_name**     | `string`  | required | The name of the modal being viewed | `privacy_setting` | | | `500` | | | |
| **step_name**      | `string`  | contextual | The name of the step users are interacting with. This is to be used if there are multiple "screens" within the modal experience to help understand funnel success/abandonment. | `We Value Your Privacy` | | | `500` | | | |
| **step_number**    | `integer` | contextual | Step number in a predefined form flow; should match the step number shown to users on the page. This is to be used if there are multiple "screens" within the modal experience to help understand funnel success/abandonment. | `1` | | | `500` | `0` | | |
| **cta_text**       | `string`  | contextual | The text or label seen by the user on the engaged call to action | `1` | | | `500` | `0` | | |
| **cta_outbound**   | `boolean` | required | Is the CTA taking the user off of the current experience. This value MUST be TRUE or FALSE, never a null or undefined value. | TRUE, FALSE | | `1` | `500` | `0` | | |
