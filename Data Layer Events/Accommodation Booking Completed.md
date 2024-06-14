# Accommodation Booking Completed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "purchase",
  "detailed_event": "Accommodation Booking Completed",
    "ecommerce": {
        "transaction_id": "<transaction_id>",
        "value": <value>,
        "currency": "<currency>",
        "coupon": "<coupon>",
        "payment_method": "<payment_method>",
        "checkout_type": "<checkout_type>",
        "items": [
            {
                "arrival_date": "<arrival_date>",
                "coupon": "<coupon>",
                "days_before_start_date": <days_before_start_date>,
                "departure_date": "<departure_date>",
                "discount": <discount>,
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
        ],
    },
    "event_data": {
        "payment_method": "<payment_method>",
        "checkout_type": "<checkout_type>",
    },
     "user_data": {
               "user_id": "<user_id>",
               "sha256_first_name": "<hashed_user_first_name>",
               "sha256__last_name": "<hashed_user_last_name>",
               "sha256_user_email": "<hashed_user_email>",
               "sha256_user_phone_number": "<hashed_user_phone_number>",
               "sha256_street": "<hashed_street>",
               "sha256_city": "hashed_city",
               "sha256_region": "<hashed_region>",
               "sha256_postal_code": "<hashed_postal_code>",
               "sha256_country": "<hashed_country>"
            }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|checkout_type|string|captures Checkout Type||||||||
|ecommerce.coupon|string|Order-level coupon code used for a purchase.|summer\_fun|||||||
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format.||||||||
|ecommerce.items[n].arrival_date|string|the arrival date of a booking|YYYY-MM-DD|||||||
|ecommerce.items[n].coupon|string|Item-level coupon code used for a purchase.|SUMMER\_FUN|||||||
|ecommerce.items[n].days_before_start_date|number|captures the Days Before Start Date of the booking||||||||
|ecommerce.items[n].departure_date|string|captures Departure Date of the booking||||||||
|ecommerce.items[n].discount|number|Monetary value of discount associated with a purchase.|2.22|||||||
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
|ecommerce.transaction_id|string|The unique identifier of a transaction.|T\_12345, 19283j2nm9jdjs|^[a-zA-Z0-9]{6,20}$|6|20||||
|ecommerce.value|number|The monetary value of the event.|7.77, 239.55, 659|||||||
|event_data.payment_method|string|Captures the payment methods used for a transaction \(i.e. credit card, Visa, MasterCard, Amex, Paypal, purchase order, etc\).|Credit Card, PayPal, Mastercard, Visa, Amex, Discover|||||||
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||
|sha256_first_name|string|required|The Hashed and encoded first name of the user.|916b1f01b7d7c08d6a19905fa9eea0fa34289ccf0c0b0e29d523fc57b78283cc|
|sha256_last_name|string|required|Hashed and encoded last name of the user.|10eb1eee807536048c3b55f44cc5fe82ae6ab3c4fa89226758a41d02bd53e5d2|
|sha256_email_address|string|required|Hashed and encoded email address of the user.|c90b8279a7042d9d6342bdf1d71699814111d8dc95b9e030e4dbb8d186b41a6f|
|sha256_street|string|required|Hashed and encoded street and number of the user.|d96546c4c670d8742647c66dd9ad232638cafe4ee10d711d4d45ad20f6b3c7fa|
|sha256_phone_number|string|required|Hashed and encoded phone number of the user.|048140ceb8abc7e186e47e3ae374d63897c85b19f710dd88e89a5394b2576f9d|
|sha256_street|string|required|Hashed and encoded street and number of the user.|c044f5159556b36e967305141d35bc10076a01f0b2f8339e85ba11785cff19c3|
|sha256_city|string|required|City for the address of the user.|c55ec4bbe9c7c1614204f286194b109010ca0680f41325ec1a82302a34b4f3f7|
|sha256_region|string|required|State or territory for the address of the user.|8e9e26c2ef86ecd02ba5c84da8a0859a39b4181b19f4c89312d6f1c1b78ccf15|
|sha256_postal_code|string|required|Postal code for the address of the user.|a187be7bb4885205afe3ba3b3ddc549693035523bcf9a48bdb10ce920200f15e|
|sha256_country|string|required|Country code for the address of the user.|aa5ab35a9174c2062b7f7697b33fafe5ce404cf5fecf6bfbbf0dc96ba0d90046|


## Attached Notes

<p>When the user has completed booking a room on the order confirmation page.</p>
<p>Please populate the user personal data encripted once it is captured(user creates an account/user provides guest information at checkout process) </p>
