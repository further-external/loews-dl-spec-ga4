# Click

Fire whenever a user clicks on a asset, that is required to be tracked.

All outbound links are tracked automatically. Other needs to be tagged with Javascript code, described below.

## Javascript Code

```js
// When:
// User clicks a non anchor tag used for an action, i.e. <button>

// Code
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  event: "click",
  event_data: {
    identifier: '<identifier>', // REQUIRED | string | ex. uniquely_created_id
    name: '<name>', // REQUIRED | string | ex. Learn More, Book Now, Feedback, Connect
    component_ancestry: "<component_ancestry>", // contextual | string | string - delimited (~) | ex. hero~product carousel
    category: "<category>", // contextual | string | ex. cta_links, wtb_links
    category2: "<category2>", // contextual | string | ex. cta_links, wtb_links
    category3: "<category3>", // contextual | string | ex. cta_links, wtb_links
    category4: "<category4>", // contextual | string | ex. cta_links, wtb_links
    category5: "<category5>", // contextual | string | ex. cta_links, wtb_links
    link_classes: "<link_classes>", // REQUIRED | string | ex. button-red 
    link_id: "<link_id>", // REQUIRED | string | ex. submit-button
    link_text: "<link_text>", // REQUIRED | string | ex. click here
    link_url: "<link_url>", // REQUIRED | string | ex. https://www.example.com/form
    link_hostname: "<link_hostname>", // REQUIRED | string | ex. https://www.example.com
    navigation_ancestry: "<navigation_ancestry>", // contextual | string - delimeted (~) | ex. about~our ceo
    outbound: "<outbound>", // contextual | boolean | ex. false
    region_ancestry: "<region_ancestry>", // contextual | string - delimeted (~) | ex. header~navigation
    protocol: "<type>" // REQUIRED | string | ex. http, https, mailto, tel
    }
});
```

## Variable Definitions

|Field|Type|Required|Description|Example|Maximum Length|
| --- | --- | --- | --- | --- | --- |
|**identifier**|`string`|required|The wtb-event machine-readable name. This should be a unique value specific to this piece of content, if one exists. If one does not exist, this can also be populated with the same value as the <name>.|`contact`, `lead_generation`|`100`|
|**name**|`string`|required|The wtb-event human-readable name. This should be something that an analyst without a deep knowledge of the technical implementation of the site can easily identify the event with. It should be lowercase snake_case.|`contact`, `lead_generation`, `book now`, `learn more`|`100`|
|**component_ancestry**|`string`|contextual|A delimited string showing all components in the ancestry of the link clicked|`hero~product carousel`|`100`|
|**category**|`string`|contextual|Optional field that enables you to assign this link a specific category. Used primarily when you want to analyze the performance of a group of links that aren't connected by component_ancestry, region_ancestry, link_url, or link_text.|`cta_links`, `wtb_links`|`100`|
|**category[2-5]**|`string`|contextual|Optional fields that enable you to assign this link additional subcategories beyond category.|`cta_links`, `wtb_links`|`100`|
|**link_classes**|`string`|required|The list of HTML/CSS classes applied to the link.|`button-red`|`100`|
|**link_id**|`string`|required|The HTML/CSS ID of the link.|`submit-button`|`100`|
|**link_text**|`string`|required|The full text of the link.|`click here`|`100`|
|**link_url**|`string`|required|The full URL of the link.|`https://www.example.com/form`|`100`|
|**link_hostname**|`string`|required|The hostname of the link.|`https://www.example.com`|`100`|
|**navigation_ancestry**|`string`|contextual|A delimited string showing all navigation items in the ancestry of link clicked in a multi-tiered menu|`about~our leadership~our CEO`|`100`|
|**outbound**|`boolean`|contextual|Does the link point to a different domain?|`false`|`100`|
|**region_ancestry**|`string`|contextual|A delimited string showing all regions in the ancestry of the link clicked|`header~navigation`|`100`|
|**protocol**|`string`|required|Records the type of link that was clicked. The type here refers to what comes before the :// on the link itself. Useful for identifying http links that should be https, as well as reporting on mailto, tel, and other alternate link types|`http`, `https`, `tel`, `mailto`|`100`|
