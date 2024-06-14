# User Detected

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "detect_user",
  "detailed_event": "User Detected",
    "user_data": {
        "user_id": "<user_id>",
        "user_login_state": "<user_login_state>",
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
|user_data.user_id|string|The id of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||
|user_data.user_login_state|string|Captures the current sign in status for the user \(i.e. signed\_out, signed\_in, unknown\).|logged in, logged out, guest|||||||
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

<p>This is information about the user. &nbsp;We will want to fire the events in this sequence.<br />Page Load Started &gt; User Detected &gt; Page Load Completed. Please populate the user personal data encripted once it is captured(user creates an account/user provides guest information at checkout process) </p>
