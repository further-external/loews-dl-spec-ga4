# CTA Clicked

Fire whenever a user clicks on a asset, that is required to be tracked.

All outbound links are tracked automatically. Other needs to be tagged with Javascript code, described below.

## Javascript Code

```js
// When:
// User clicks a non-anchor tag used for an action, i.e. <button>

// Code
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  event: "click",
  detailed_event: "CTA Clicked",
  event_data: {
    identifier: '<identifier>',
    name: '<name>', 
    category: "<category>",
    link_classes: "<link_classes>",
    link_id: "<link_id>",
    link_text: "<link_text>", 
    link_url: "<link_url>",
    link_hostname: "<link_hostname>",
    protocol: "<type>",
    outbound: "<outbound>", 
    region_ancestry: "<region_ancestry>",
    component_ancestry: "<component_ancestry>",
    navigation_ancestry: "<navigation_ancestry>",
    region_ancestry: "<region_ancestry>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Maximum Length|
| --- | --- | --- | --- | --- |
|**identifier**|`string`|The wtb-event machine-readable name. This should be a unique value specific to this piece of content, if one exists. If one does not exist, this can also be populated with the same value as the <name>.|`contact`, `lead_generation`|`100`|
|**name**|`string`|The wtb-event human-readable name. This should be something that an analyst without a deep knowledge of the technical implementation of the site can easily identify the event with. It should be lowercase snake_case.|`contact`, `lead_generation`, `book now`, `learn more`|`100`|
|**category**|`string`|Optional field that enables you to assign this link a specific category. Used primarily when you want to analyze the performance of a group of links that aren't connected by component_ancestry, region_ancestry, link_url, or link_text.|`cta_links`, `wtb_links`|`100`|
|**link_classes**|`string`|The list of HTML/CSS classes applied to the link.|`button-red`|`100`|
|**link_id**|`string`|The HTML/CSS ID of the link.|`submit-button`|`100`|
|**link_text**|`string`|The full text of the link.|`click here`|`100`|
|**link_url**|`string`|The full URL of the link.|`https://www.example.com/form`|`100`|
|**link_hostname**|`string`|The hostname of the link.|`https://www.example.com`|`100`|
|**protocol**|`string`|Records the type of link that was clicked. The type here refers to what comes before the :// on the link itself. Useful for identifying http links that should be https, as well as reporting on mailto, tel, and other alternate link types|`http`, `https`, `tel`, `mailto`|`100`|
|**outbound**|`boolean`|Does the link point to a different domain?|`false`|`100`|
|**component_ancestry**|`string`|A delimited string showing all components in the ancestry of the link clicked|`hero~product carousel`|`100`|
|**navigation_ancestry**|`string`|A delimited string showing all navigation items in the ancestry of link clicked in a multi-tiered menu|`about~our leadership~our CEO`|`100`|
|**region_ancestry**|`string`|A delimited string showing all regions in the ancestry of the link clicked|`header~navigation`|`100`|
