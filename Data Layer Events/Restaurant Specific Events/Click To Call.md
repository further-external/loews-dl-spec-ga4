
# Click To Call

Fire whenever a user successfully clicks on a valid phone number that initiates a phone call.

## Javascript Code

```js
// When:
// User clicks to call a phone number

// Code:
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data and user_data objects.
dataLayer.push({
  event: 'click_to_call',
  detailed_event: "Click to Call",
  },
  event_data: {
    identifier: '<identifier>', // REQUIRED | string | ex. call_support, call_sales, call_inquiry, call_book_tour, call_pricing_availability
    name: '<name>', // REQUIRED | string | ex. support_call, sales_call, inquiry_call, book_tour_call, pricing_availability_call
    type: '<type>', // REQUIRED | string | ex. reservation, call, inquiry, support, book_tour, lead_generation
    call_category: '<call_category>', // REQUIRED | string | ex. reservations, support, sales, inquiry, family, resident, book_tour
    event_phone_number: '<event_phone_number>' // REQUIRED | string | ex. 888-777-7777
  }
});
dataLayer.push({ event_data: null });  // Clear the previous event_data and user_data objects.
```

## Variable Definitions

|Field|Type|Required|Description|Example|Maximum Length|
| --- | --- | --- | --- | --- | --- |
|**identifier**|`string`|required|The form machine-readable name. This should be a unique value specific to this piece of content, if one exists. If one does not exist, this can also be populated with the same value as the <name>.|`call_support`, `call_sales`, `call_inquiry`, `call_book_tour`, `call_pricing_availability`|`100`|
|**name**|`string`|required|The form human-readable name. This should be something that an analyst without a deep knowledge of the technical implementation of the site can easily identify the form with. It should be lowercase snake_case.|`support_call`, `sales_call`, `inquiry_call`, `book_tour_call`, `pricing_availability_call`|`100`|
|**type**|`string`|required|The form type. This will act as a filtering mechanism in reporting to enable analysts to view form drop off funnels. It can also act as an internal aid in firing additional events if necessary. For instance, lead-generating forms require a `generate_lead` event to be fired alongside `form_complete`, and that could be written into the logic based upon this field. This can be used alongside `call_category`, such as `book_tour` and `sales` versus `inquiry`.|`call`, `inquiry`, `support`, `book_tour`, `lead_generation`|`100`|
|**call_category**|`string`|required|Specifies the category of the call.|`support`, `sales`, `inquiry`, `family`, `resident`, `book_tour`|`100`|
|**event_phone_number**|`string`|required|The user-provided phone number. This must only be populated if the user has provided their phone number via a form or some other information collection method.|`888-777-7777`|`100`|
|**form_category**|`string`|required|The categorization of the form based on the option selected by a user or automatically set by the form.|`book_a_tour`, `pricing_and_availability`, `careers`, `volunteering`, `other`|`100`|
||||&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;||&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
