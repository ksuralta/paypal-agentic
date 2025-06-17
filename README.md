# PayPal Agentic Toolkit Quickstart Example

## References

https://github.com/paypal/agent-toolkit
https://developer.paypal.com/tools/agent-toolkit/
https://developer.paypal.com/tools/agents/quickstart/

## Setup

Set the following environment variables

1. PAYPAL_CLIENT_ID
2. PAYPAL_CLIENT_SECRET
3. OPENAI_API_KEY

## To Run

`npx tsx index.ts`

## Sample Output

```
Step 1: I am using the provided prompts to create a request object for PayPal.
Response 1: I have now created the request object with provided details;
 {"currencyCode":"USD","items":[{"name":"Labor","quantity":3,"description":"Plumbing labor for 3 hours","itemCost":120,"taxPercent":50,"itemTotal":540},{"name":"Faucet","quantity":1,"description":"Standard kitchen faucet","itemCost":65,"taxPercent":12,"itemTotal":72.8},{"name":"Pipes","quantity":5,"description":"Standard pipes for installation","itemCost":3,"taxPercent":12,"itemTotal":16.8}],"shippingAddress":null,"notes":null,"returnUrl":"http://localhost:3000/thank-you","cancelUrl":"https://example.com/cancelUrl"}
Proceeding with next step.
Step 2: I am now choosing the correct tool from PayPal's toolkit to create an an order using the generated object from previous step.
Response 2: I have created the order in PayPal's system with order ID: The order has been successfully created. Here are the details:

- **Order ID**: 8XP045806S1666613
- **Status**: PAYER_ACTION_REQUIRED

You can proceed with the payment by following this [link](https://www.sandbox.paypal.com/checkoutnow?token=8XP045806S1666613)..
Proceeding with next step.
Step 3: I am now choosing the correct tool from PayPal's toolkit to retrieve the order details with the order ID from previous step.
Response 3: Here is the order details with ID: The order has been successfully created. Here are the details:

- **Order ID**: 8XP045806S1666613
- **Status**: PAYER_ACTION_REQUIRED

You can proceed with the payment by following this [link](https://www.sandbox.paypal.com/checkoutnow?token=8XP045806S1666613).; "Here are the details of the order with ID **8XP045806S1666613**:\n\n- **Status**: PAYER_ACTION_REQUIRED\n- **Intent**: CAPTURE\n- **Total Amount**: $629.60 USD\n  - **Item Total**: $440.00 USD\n  - **Shipping**: $0.00 USD\n  - **Tax Total**: $189.60 USD\n\n### Purchase Units:\n1. **Reference ID**: default\n   - **Payee Email**: ksuralta+au-facilitator@gmail.com\n   - **Merchant ID**: 3PA8KQ5M6LU8C\n\n### Items:\n- **Labor**\n  - **Unit Amount**: $120.00 USD\n  - **Tax**: $60.00 USD\n  - **Quantity**: 3\n  - **Description**: Plumbing labor for 3 hours\n\n- **Faucet**\n  - **Unit Amount**: $65.00 USD\n  - **Tax**: $7.80 USD\n  - **Quantity**: 1\n  - **Description**: Standard kitchen faucet\n\n- **Pipes**\n  - **Unit Amount**: $3.00 USD\n  - **Tax**: $0.36 USD\n  - **Quantity**: 5\n  - **Description**: Standard pipes for installation\n\n### Links:\n- [Proceed with Payment](https://www.sandbox.paypal.com/checkoutnow?token=8XP045806S1666613)\n\nYou can proceed with the payment by following the link above."
Proceeding with next step.
Step 4: I am now generating the summary of the order using the order details retrieved in the previous step. This makes it easier to read the important information.
Response 4: 
### Order Summary

**Order ID**: 8XP045806S1666613  
**Status**: PAYER_ACTION_REQUIRED  
**Intent**: CAPTURE  
**Total Amount**: $629.60 USD  
- **Item Total**: $440.00 USD  
- **Shipping**: $0.00 USD  
- **Tax Total**: $189.60 USD  

#### Purchase Units:
- **Reference ID**: default  
  - **Payee Email**: ksuralta+au-facilitator@gmail.com  
  - **Merchant ID**: 3PA8KQ5M6LU8C  

#### Items:
1. **Labor**  
   - **Unit Amount**: $120.00 USD  
   - **Tax**: $180.00 USD (calculated as $60.00 * 3)  
   - **Quantity**: 3  
   - **Description**: Plumbing labor for 3 hours  

2. **Faucet**  
   - **Unit Amount**: $65.00 USD  
   - **Tax**: $7.80 USD (calculated as $7.80 * 1)  
   - **Quantity**: 1  
   - **Description**: Standard kitchen faucet  

3. **Pipes**  
   - **Unit Amount**: $3.00 USD  
   - **Tax**: $1.80 USD (calculated as $0.36 * 5)  
   - **Quantity**: 5  
   - **Description**: Standard pipes for installation  

### Payment
To complete your purchase, please proceed with the payment using the link below:

- [Proceed with Payment](https://www.sandbox.paypal.com/checkoutnow?token=8XP045806S1666613)
### Order Summary

**Order ID**: 8XP045806S1666613  
**Status**: PAYER_ACTION_REQUIRED  
**Intent**: CAPTURE  
**Total Amount**: $629.60 USD  
- **Item Total**: $440.00 USD  
- **Shipping**: $0.00 USD  
- **Tax Total**: $189.60 USD  

#### Purchase Units:
- **Reference ID**: default  
  - **Payee Email**: ksuralta+au-facilitator@gmail.com  
  - **Merchant ID**: 3PA8KQ5M6LU8C  

#### Items:
1. **Labor**  
   - **Unit Amount**: $120.00 USD  
   - **Tax**: $180.00 USD (calculated as $60.00 * 3)  
   - **Quantity**: 3  
   - **Description**: Plumbing labor for 3 hours  

2. **Faucet**  
   - **Unit Amount**: $65.00 USD  
   - **Tax**: $7.80 USD (calculated as $7.80 * 1)  
   - **Quantity**: 1  
   - **Description**: Standard kitchen faucet  

3. **Pipes**  
   - **Unit Amount**: $3.00 USD  
   - **Tax**: $1.80 USD (calculated as $0.36 * 5)  
   - **Quantity**: 5  
   - **Description**: Standard pipes for installation  

### Payment
To complete your purchase, please proceed with the payment using the link below:

- [Proceed with Payment](https://www.sandbox.paypal.com/checkoutnow?token=8XP045806S1666613)
```

