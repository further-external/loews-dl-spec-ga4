# Onsite Search Performed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "search",
  "detailed_event": "Onsite Search Performed",
    "event_data": {
        "days_to_start_date": <days_to_start_date>,
        "end_date": "<end_date>",
        "location_id": "<location_id>",
        "market_code": "<market_code>",
        "number_of_adults": <number_of_adults>,
        "number_of_children": <number_of_children>,
        "rate_code": "<rate_code>",
        "start_date": "<start_date>",
        "type": "<type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.days_to_start_date|integer|Captures the booking window used in search criteria \(e.g. number of days prior to requested check-in date\).|1, 2, 3, 4, 5|||||||
|event_data.end_date|string|Captures the end date requested in search criteria.|2022-10-28, 2023-01-15|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|event_data.location_id|string|Captures the Location Id. Please refer to this document to determine location ID.
https:\/\/docs.google.com\/spreadsheets\/d\/1PDhNOzXI9E7jZ9obejV4owtW3Wtwq66\_IaN-CBoHbRs\/edit\#gid=1543857253|6558, 70561|||||||
|event_data.market_code|string|market code||||||||
|event_data.number_of_adults|integer|Captures the number of adults entered in search criteria.|1, 2, 3, 4, 5||||1|||
|event_data.number_of_children|integer|Captures the number of children entered in search criteria.|1, 2, 3, 4, 5||||0|||
|event_data.rate_code|string|Room Rate Code||||||||
|event_data.start_date|string|Captures the start date requested in search criteria. \(e.g. check-in date\)|2022-10-22, 2023-01-15|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|event_data.type|string|Captures the type of on-site search performed \(i.e., content, product, location, product location, scheduled event, room, report\)|products, properties, articles, authors, coupons, publications|||||||

## Attached Notes

<p>When a user selects the dates and location of their booking and conducts a search</p>
