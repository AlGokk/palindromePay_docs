---
title: Create Crypto Payment
description: Start with creating crypto payment.
---

In order to use the crypto payment system it is necessary to use the paymentSystemUID and orderBookUID.

---

## Init

Call the `Init()` function to create the payment system. In the background an own contract called PalindromePaymentSystem

### Import Functions

In the first step you need to import thePalindrome Crypto Pay SDK into your JavaScript/TypeScript project with the needed function `PalindromePayCreatePayment`.

```js
import {
  PalindromePayConnect,
  PalindromePayCreatePayment,
} from '@Palindromepay/sdk'
```

**Interface**

```js
// Input
export interface IInit {
  signer: any;
}
```

**Function**

```js
PalindromePayCreatePayment.init(args)
```

**Params**

| Name   | Type | Description                                     | Result  |
| ------ | ---- | ----------------------------------------------- | ------- |
| signer | any  | Sending transactions a signer need to be passed | boolean |

### Example Code

```js
try {
 const args: IInit = {
    signer: signer
 }
  const status = await PalindromePayCreatePayment.init(args);
  if (status) {
    /** do something */
  }
} catch(e: any) {
  console.log(e);
}
```

---

## Payment Generator Page

You are also able to use the lightweight-wizard to create the payment-system [link](https://Palindromepay.app/create-crypto-payment)
