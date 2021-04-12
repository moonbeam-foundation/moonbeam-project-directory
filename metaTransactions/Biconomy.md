# Biconomy

## Scalable Relayer Infrastructure for Blockchain Transactions.

## Introduction

Biconomy is a scalable transaction relayer infrastructure, which can pay blockchain transaction's gas fee for your dApp user, while collecting fees from you on monthly basis, in form of some stable token.

- **Dapps require way too much onboarding and are too hard to even begin using. We need a solution to make onboarding easy for users.** Non-crypto savvy new users will have to pass KYC, purchase ETH from an exchange, download a wallet, then connect their wallet before they can go any further, which can take days! No one waits for days to try out an application.
- **One of the major issues is need to hold Native currency for using dapps. Users can only pay in ETH**, which they may not have at that moment. Or the user may not want to spend their ETH investment.
- **The** n**ecessity to pay a gas** fee every time the user uses your application. Netflix does not charge you their AWS fees for every time you watch a video, so why should Dapps charge you gas fees for every interaction you do?
- **Proficiency in complex blockchain technicalities is required** such as using MetaMask, signing transactions, understanding gas etc. If the project is on layer 2, they need to know what that really means and be able to change RPC manually.
- **Volatile and high gas fees** further dampen the user experience on your Dapp.
- **Pending and stuck transactions** can force your users to wait for minutes and even hours before they can carry on interacting with your application. And sometimes the transaction fails altogether.

## What are Meta-Transactions?

Meta Transactions are transactions whose data is created and signed off-chain by a user and relayed to the network by another party who pays the gas fees.

Since meta transactions are not native to the protocol, you would need to either use a 3rd party setup (e.g. Biconomy) or set up a service on your own.

**We enable this at scale by providing a non-custodial and gas efficient relayer infrastructure network.**

## We support different approaches for implementing meta Transactions:

### 1. Smart Contract Wallet

In this approach, for each user, an upgradable contract wallet is created, which acts as a proxy contract & relays all transactions to the destination smart contract. As user needs to keep all of their assets under supervision of this proxy contract, all blockchain transactions to be routed via this proxy contract.

Biconomy supports Gnosis contract wallet integration. Checkout how you can integrate meta transactions via Gnosis smart contract wallet here.

### 2. Custom Implementation

If dApps support native meta transactions, then Biconomy's relayers would directly relay the transactions to the network without the need for any proxy contract.

![../images/biconomy/NativeMetaTx.png](../images/biconomy/NativeMetaTx.png)

### 3. EIP 2771 Standard Implementation

Instead of integrating meta transaction validation logic directly into your contract - you can inherit a recipient contract that can accept validated calls from a trusted forwarder. The trusted forwarder complies with EIP 2771 and verifies signatures before calling smart contract with the original user address data appended. It makes development easier and gives you the flexibility to change the trusted forwarder address when your needs change.

![../images/biconomy/trustedForwarder.png](../images/biconomy/trustedForwarder.png)

Using Biconomy's Mexa SDK you can integrate Biconomy into your DApp seamlessly. Using Biconomy's dashboard gives you a fine control on settings and configuration for enabling MetaTransactions.

## Integration

**Integration using Mexa is a simple step process:**

1. Register your DApp on Biconomy Dashboard, a dashboard for developers, and copy API Key generated for your DApp.
2. Add the contract address and contract ABI on which you wanna enable Meta Transaction to your Biconomy dashboard.
3. Integrate Mexa SDK in your DApp code using API Key you got from dashboard.

### Dashboard

Follow the steps **[here](https://docs.biconomy.io/biconomy-dashboard)**, to register an account and add a DApp to get the keys, and configure functions that will accept signed transactions.

### Using mexa

1. Get inside the DApp client code directory, to configure meta transactions. Let's first install `@biconomy/mexa` from npm.

   ```jsx
   npm install @biconomy/mexa --save
   ```

2. Now you need to initialize Biconomy & web3. In place of `<web3 provider>` you can use `window.ethereum` if your DApp users are using MetaMask.

```jsx
import { Biconomy } from "@biconomy/mexa";

const biconomy = new Biconomy(<web3 provider>, {apiKey: <API Key>});
web3 = new Web3(biconomy);

biconomy.onEvent(biconomy.READY, () => {

  // Initialize your dapp here like getting user accounts, initialising contracts and etc

}).onEvent(biconomy.ERROR, (error, message) => {

  // Handle error while initializing mexa

});
```

## 🥳

## Congrats, you've successfully integrated Biconomy into your Dapp and now your dapp supports meta Tx.

### Wanna make your users pay gas-fee in ERC20 tokens? We can help you with that. Read more about that on our [docs](http://docs.biconomy.io).

**Wanna get in touch?**

Discord: [Biconomy's Discord](https://discord.gg/tQPxHBT)

Telegram: [Biconomy's Telegram](https://t.me/biconomy)

Twitter: [Biconomy's Twitter](https://twitter.com/biconomy)
