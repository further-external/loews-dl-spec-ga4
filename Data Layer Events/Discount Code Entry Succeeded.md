# Discount Code Entry Succeeded

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "coupon_success",
  "detailed_event": "Discount Code Entry Succeeded",
    "event_data": {
        "coupon": "<coupon>",
        "discount_code_type": "<discount_code_type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.coupon|string|Captures the coupon code associated with product level discounts for a transaction.|5OFFSHOES, AKRONCANDLES2019|||||||
|event_data.discount_code_type|string|Type of discount code applied||||||||

## Attached Notes

<p>When a user's discount code entered succeeds.</p>
