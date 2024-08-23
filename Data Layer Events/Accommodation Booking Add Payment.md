# Accommodation Booking Add Payment

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "add_payment_info",
  "detailed_event": "Accommodation Booking Add Payment",
    "ecommerce": {
        "currency": "<currency>",
        "value": <value>,
        "payment_method": "<payment_method>",
        "items": [
            {
                "arrival_date": "<arrival_date>",
                "days_before_start_date": "<days_before_start_date>",
                "departure_date": "<departure_date>",
                "item_id": "<item_id>",
                "item_name": "<item_name>",
                "market_code": "<market_code>",
                "number_of_adults": <number_of_adults>,
                "number_of_children": <number_of_children>,
                "price": <price>,
                "quantity": <quantity>,
                "room_rate_code": "<room_rate_code>",
                "room_type_code": "<room_type_code>"
            }
        ]
    },
    "event_data": {
               "payment_method": "<payment_method>"
        },
        "user_data": {
               "user_id": "<user_id>",
               "user_first_name": "<user_first_name>",
               "user_last_name": "<user_last_name>",
               "user_email": "<user_email>",
               "user_phone_number": "<user_phone_number>",
               "user_street": "<user_street>",
               "user_city": "<user_city>>",
               "user_region": "<user_region>",
               "user_postal_code": "<user_postal_code>",
               "user_country": "<user_country>"
            }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.items[n].arrival_date|string|the arrival date of a booking|YYYY-MM-DD|||||||
|ecommerce.items[n].days_before_start_date|number|captures the Days Before Start Date of the booking||||||||
|ecommerce.items[n].departure_date|string|captures Departure Date of the booking||||||||
|ecommerce.items[n].item_id|string|Please reference this document to determine the Item ID
https:\/\/docs.google.com\/spreadsheets\/d\/1PDhNOzXI9E7jZ9obejV4owtW3Wtwq66\_IaN-CBoHbRs\/edit\#gid=1543857253|6558, 70561|||||||
|ecommerce.items[n].item_name|string|Item Name \(context-specific\).|jeggings|||||||
|ecommerce.items[n].market_code|string|captures the Market Code of the booking||||||||
|ecommerce.items[n].number_of_adults|integer|Captures the number of adults in a booking||||||||
|ecommerce.items[n].number_of_children|integer|captures the Number of Children in a booking \(ecommerce DE\)||||||||
|ecommerce.items[n].price|number|The monetary price of the item, in units of the specified currency parameter.|9.99|||||||
|ecommerce.items[n].quantity|integer|Item quantity.|1|||||||
|ecommerce.items[n].room_rate_code|string|captures the rate code of the room||||||||
|ecommerce.items[n].room_type_code|string|captures the room type code of the booking||||||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||
|event_data.payment_method|string|Captures the payment methods used for a transaction \(i.e. credit card, Visa, MasterCard, Amex, Paypal, purchase order, etc\).|Credit Card, PayPal, Mastercard, Visa, Amex, Discover|||||||
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||
|user_data.user_first_name|string|required|The first name of the user.|John|
|user_data.user_last_name|string|required|The last name of the user.|Smith|
|user_data.user_email_address|string|required|The email address of the user.|john.smith@test.com|
|user_data.user_street|string|required|The street and number of the user.|1 river bend rd|
|user_data.user_phone_number|string|required|The phone number of the user.|1.888.888.8888|
|user_data.user_city|string|required|City for the address of the user.|Plymoth|
|user_data.user_region|string|required|State or territory for the address of the user.|Massachusetts|
|user_data.user_postal_code|string|required|Postal code for the address of the user.|02345|
|user_data.user_country|string|required|ISO country code for the address of the user.|US|

## Attached Notes

<p>This will fire on the final screen in the booking flow where a user enters credit card info and completes the captcha validation. Right now this is the 'Review &amp; Book' screen(https://reservations.loewshotels.com/billing)</p>
<p>Please populate the user personal data encripted once it is captured(user creates an account/user provides guest information at checkout process) </p>

