# User Registered

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "sign_up",
  "detailed_event": "User Registered",
    "event_data": {
        "method": "<method>"
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
|event_data.method|string|Captures the website method \(i.e. search, top nav\) used to find each product.|email, facebook, twitter|||||||
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

<p>User registers for a loews account</p>
