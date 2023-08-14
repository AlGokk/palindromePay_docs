---
title: Getting started
pageTitle: Palindrome - Decentralized Crypto Pay Documentation.
description: Integrate the Payment-System into your Online-Shop and never use a centralized crypto payment system again.
---

Learn how to getPalindrome Crypto Pay SDK set up. {% .lead %}

{% quick-links %}

{% quick-link title="Quick Start" icon="installation" href="#quick-start" description="Step-by-step guides to setting up your system and installing the library." /%}

{% quick-link title="Widget" icon="plugins" href="/" description="Integrate the checkout widget into your website without programming it from scratch." /%}

{% /quick-links %}

---

## Quick start

Do you want to start right away? Then install Palindrome Crypto Pay with a command line.

### Installing dependencies

The SDK is written in **TypeScript** and can be imported into React, Vue and Angular applications. The SDK will be also in other languages such as **Go** and **Python** available.

```typescript
yarn @Palindromepay/sdk
```

After the library is installed just import it to you (decentralized) application.

### Importing the library

```js
// App.tsx
import {
  PalindromePayConnect,
  PalindromePayCreatePayment,
  PalindromePayOrder,
  PalindromePaySend,
  PalindromePayWithdraw,
} from '@Palindromepay/sdk'
```

{% callout title="You should know!" %}
We will start with creating your own Crypto Payment. Each payment system is encapsuled and the image/docs and description are saved encrypted on decentralized web3 storage.

There are two ways to create a payment system:

a) Using the library directly and calling the function `PalindromePayCreatePayment.init()` within your implementation.

b) Or you can create it over the page [link](https://Palindromepay.app/create-crypto-payment) if you want to skip an own implementation. The result is that you get a `paymentSystemUID`, `orderBookUID`which is essential for the Crypto Payment System.

{% /callout %}

---

## Getting help

### Join the Discord Dev Channel

If you need help then write us at [Discord](https://discord.com/invite/5mwebaUMpk)
