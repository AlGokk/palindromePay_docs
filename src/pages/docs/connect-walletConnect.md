---
title: Connect with WalletConnect
description: Connect your application with Metamask or TrustWallet over your mobile.
---

Before you can create a payment system or send any transaction you need to connect with the web3-provider. For that reason we made it as easy as possible to connect over the Palindrome SDK with Metamask or TrustWallet on mobile.

---

## connectMetamask

Call the `connectWalletConnect(args)` function to connect with Metamask or TrustWallet. ThePalindrome Crypto Pay is supporting multiple chains such as AVAX, Ethereum & BSC. Therefore, you need to pass the chainID or rpc with the chaindID so that thePalindrome Crypto Pay Crypto SDK can recognize the chain you want to work with.

### Import Functions

In the first step you need to import thePalindrome Crypto Pay SDK into your JavaScript/TypeScript project with the needed function `PalindromePayConnect`.

```js
import { PalindromePayConnect } from '@Palindromepay/sdk'
```

**Interfaces**

```js
// Input
export interface IConnect {
  rpc?: { [chainId: number]: string }; // optional
  chainId: number;
}

// Output
export interface IAuthInstance {
  account: string;
  provider: any;
  signer: any;
}
```

**Function**

```js
PalindromePayConnect.connectWalletConnect(args)
```

**Params**

| Name           | Type   | Description                                        |
| -------------- | ------ | -------------------------------------------------- |
| rpc (Optional) | Object | Pass Object which includes the chainID and rpc-url |
| chainID        | number | Pass the chainID of the network                    |

### Example Code

```js
try {
  loginMetamask = async () => {
    const args: IConnect = {
      rpc: { 43114: 'https://api.avax.network/ext/bc/C/rpc' },
      chainId: 43114,
    }
    const auth: IAuthInstance = await PalindromePayConnect.connectWalletConnect(
      args
    )
    if (!auth?.account) {
      console.log('Logged in failed...')
    } else {
      console.log('Logged in succeed...')
    }
  }
} catch (e) {
  console.log(e)
}
```
