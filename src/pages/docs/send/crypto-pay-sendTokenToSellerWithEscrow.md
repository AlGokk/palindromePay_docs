---
title: Send Token in Escrow
description: Connect your application with Metamask over your desktop.
---

Send any ERC20 token to the seller in escrow.

---

## sendTokenToSellerInEscrow

Call the `sendTokenToSellerInEscrow(args)` function to send the choosen ERC20 token to the seller or merchant. This works only if before a order is created `createOrder(args)`

### Import Functions

To use the function you need to import the libarary class called `PalindromePaySend`.

```js
import {
  PalindromePayConnect,
  PalindromePayCreatePayment,
  PalindromePaySend,
} from '@Palindromepay/sdk'
```

**Interfaces**

```js
// Input
export interface ISendTokenToSellerInEscrow {
  token: string;
  to: string;
  paymentSystemUID: string;
  amount: string | BigNumber;
  orderID: string;
  title: string;
  signer: any;
}

// Output
export interface IStates {
  status: boolean;
  tx: ITx;
}
```

**Function**

```js
PalindromePaySend.sendTokenToSellerInEscrow(args)
```

token: string;
to: string;
paymentSystemUID: string;
amount: string | BigNumber;
orderID: string;
title: string;
signer: any;
**Params**

| Name             | Type   | Description                                              |
| ---------------- | ------ | -------------------------------------------------------- |
| token            | string | token address - it can be passed any ERC20 token address |
| to               | string | address of the recipient - seller or merchant            |
| paymentSystemUID | string | paymentSystemUID generated over the system               |
| amount           | string | amount you want to send                                  |
| orderID          | string | the orderID to recognize the order                       |
| title            | string | title of max length 42                                   |
| signer           | any    | signer to send transactions                              |

### Example Code

```js
try {
  const args: ISendTokenToSellerInEscrow = {
    token: '0x17d348eAA30F191eE34c3dE874Ba9989f259e44c',
    to: 'your account address',
    paymentSystemUID: 'your paymentID address',
    amount: '100',
    orderID: '2',
    title: 'IPhone S6',
    signer: 'here the signer',
  }
  const res: IStatus = await PalindromePaySend.sendTokenToSellerInEscrow(args)
} catch (e) {
  console.log(e)
}
```
