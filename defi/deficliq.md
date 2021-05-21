---
title: Deficliq
description: The Place to Unify all De-Fi Features.
---

# Deficliq - The Place to unify all De-Fi Features

![deficliq Banner](../images/deficliq/deficliq.png)

**Disclaimer:** Projects themselves entirely manage the content in this guide. Moonbeam is a permissionless network. Any project can deploy its contracts to Moonbeam.

## Introduction

Staking Smart Contract is based on the Defi Staking concept in which users can stake their token and Dev for a particular period of time and can get reward based on it.
Staking Contract work on modules like users can stake tokens and Dev for 30 days, 60 days, and 90 days respectively.

Rewards are defined which are based on the number of staking days.
The penalty will be applied on early withdrawal that means if the user withdraws a staked token or Dev before the stake end time, the penalty will be applicable.

The contract is divided into two contract 
 - **Cliq Token Smart Contract**
 - **Staking Contract**

The Staking Smart Contract ecosystem constitute two smart contract which work together, these are:
 - **Cliq Token Smart Contract** — ERC20 based smart contract for token functionality.
 - **Staking Contract** — Staking Smart contract with functionalities like stake token, reward and penalty and withdraw stake function.

You can read more about deficliq in the following links:

 - [deficliq Website](https://www.deficliq.com/)
 - [deficliq Github](https://github.com/deficliq/moonbeam_work)
 - [deficliq twitter](https://twitter.com/deficliq)

## Moonbase Alpha Implementation

Deficliq has deployed its core smart contract to the Moonbase Alpha TestNet.  
In this Smart Contract you can do the following:
-> **Cliq Token Smart Contract**
   - [Token Smart Contract Address](https://moonbase-blockscout.testnet.moonbeam.network/address/0xBa6C068122C91E46304F3CBE768ddF8927BA4314/transactions)
   - Can transfer token from one address to another
   - Can burn particular amount of token
   - Can mint particular amount of token
   - Can approve particular amount of token via which further transfer can be happen.

-> **Staking Smart Contract**
   - [Staking Smart Contract Address](https://moonbase-blockscout.testnet.moonbeam.network/address/0x0a2105B5b02AF23db5d5779beA8Dd8184bA6Fc45/transactions)
   - Users can stake particular amount of token
   - users can know their reward and penalty via functions
   - users can withdraw their stake token
   - users can stake Dev and can earn rewards
   - users can withdraw Dev 

### Contract Functionality

Staking Smart Contract Ecosystem is based on De-Fi concept in which user will need to stake cliq token or native token in order to get rewards.
Basic Functionality of Smart Contract is..
 - Cliq token Contract is deployed via Cliq Smart Contract
 - Staking Smart Contract is using Cliq smart contract via internal calls by which user can stake cliq.
 - In order to stake Cliq token, user need to input particular amount of token amount and time period.
 - Time period can be selected from 30, 60 and 90 days respectively.
 - Rewards are managed as per the days user stake their token.
 - Penalty will be applicable if user want to unstake or withdraw token before particular period of time.
 - This Scenario work same for Native Token i.e Dev token.
 - Reward and Penalty Percentage are managed as per the Staking Days of token or Native Token.
 - Users will get particular 'ID' via which they can see their reward in real time.
 - These 'ID' help user to see their investment and amount of token they stake on the platform.

### Contract Information

You can find all the contracts relevant to the deficliq staking platform in [this GitHub repo](https://github.com/deficliq/moonbeam_work). 
Addresses that are relevant for the Moonbase Alpha implementation are outlined in the following table:

|             Contract             |                  Address                   |
| :-------------------------------:| :----------------------------------------: |
|      Token Contract Address      | 0xBa6C068122C91E46304F3CBE768ddF8927BA4314 |
|      Staking Contract Address    | 0x0a2105B5b02AF23db5d5779beA8Dd8184bA6Fc45 |
