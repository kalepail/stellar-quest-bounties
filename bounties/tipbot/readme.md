# Stellar Tip-bot Discord
### Problem
Current Stellar Quest users can't tip other people in case they help out someone. Users should have the option to do so.

### Proposed Solution

Using Slash commands users can tip users XLM or Custom Assets.  Users will first have to link their accounts to the existing app in order to receive funds, if a user attempts to tip a non existent user if the user has DM's enabled will get a message with instructions how to create an account. 

Tipping will be based on Payments. XLM & Assets with established trustlines will go with a payment operation and if the received does not have a trust line with the asset the transaction will be sent with a Claimable balance along with a link to [Stellar - Claimable Balances](https://matejmecka.github.io/stellar-claimable-balances-web/) login with Albedo to claim their funds.  Users who do not have any xlm in their wallet and the transaction is XLM instead of a payment operation it will be a Create Account operation

The bot will also check for exchange accounts such as Coinbase, Lobstr and block the user from signing up with that account. Users will be sent to the laboratory to generate a keypair. 

The minimum amount for tipping will be 1 XLM to prevent spamming 

`/tip <@XXXX> 50` <- Tips the user 50 XLM
`/tip <@> 50 USDC ISSUER` <- Tips the user 50 USDC
`/link GACDXXXX` <- Links the users account

### Preview

![](Stellar%20Tip-bot%20Discord/Screen%20Shot%202021-07-15%20at%2010.50.13%20PM.png)

### Behind the Scenes

![](Stellar%20Tip-bot%20Discord/Untitled%20Diagram(1).png)