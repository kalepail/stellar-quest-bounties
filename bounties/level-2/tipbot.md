# TipBot / Bear Bot
| Hunter | Reviewer | Type
| :- | :- | :-
| 1500 XLM | 500 XLM | Capped (1) | 

## Description
Current Stellar Quest users can't tip other people in case they help out someone. Users should have the option to do so. By using a Discord bot and by reacting to messages with different bear emojis they can sent a tip instantly

### What is this task?

Users will be able to tip the message author of a sent message on Discord by reacting with 4 kinds of bears. This is the proposed valuation for different kinds of bear emojis and the amount of worth the user can tip.

🐻‍❄️ - 100 BEARS

🐻 - 10 BEARS

🐼 - 5 BEARS

🧸 - 1 BEAR

Using Slash commands users can tip a custom amount of bears. The command for tipping a custom amount of bears is  `/tip 50`.

 Users will first have to link their accounts to the existing app to receive funds, if a user attempts to tip a nonexistent user and if the user has DM's enabled they will get a message with instructions on how to create an account. 

Tipping will work with the Payments operation. Assets with established trust lines will go with a payment operation. If the recipient does not have a trust line with the asset, the recipient will receive it as a Claimable balance. Users will either setup up the trust line in Lobstr Vault or be redirected to a tool like this: [Stellar - Claimable Balances](https://matejmecka.github.io/stellar-claimable-balances-web/) where they can login with Albedo to claim their funds. Users who do not have any xlm in their wallet and the transaction is XLM instead of a payment operation it will be a Create Account operation 

The bot will also check for exchange accounts such as Coinbase and block the user from signing up with that account. 

If a User doesn't have an account they'll get the suggestion to use Lobstr Vault. This Bounty has not been sponsored by them.

Before they can use the bot they'll be able to link their account with a Slash command. `/link GACDXXXX` , This later can be phased out for a federation server that Stellar Quest users will use.

### What are the requirements for the bounty hunter?

For this bounty to be completed a Git repository with an Open Source License is required to be submitted. The Git repository should also include instructions on how to easily compile everything or provide build scripts that will do that for the developer.

It would be nice if the code is easily readable and documented.

You can use any tech stack you want to build the XDR signer. Make sure it has a good UI/UX experience and works well :D


### What are the deliverables?

*Description* <br>
* The Developer should submit an Open Source bot that will be available either on GitHub, GitLab, Bitbucket or any place that can allow easily cloning a repository via Git. 
* The Developer should link a demo bot on a test server to allow reviewers to test the app.

*Judging Criteria and Metrics* <br>
  * Code Quality - Is the code understandable?
  *  Does it adhere to language-specific style guidelines?
  
*Submission Procedure* <br>
* The bounty will only be considered complete, after a Git repository has been submitted and a preview of the submission has been provided.

## Links
- [Discord Developer Portal](https://discord.com/developers/docs)
- https://github.com/Lobstrco/Vault-Android

