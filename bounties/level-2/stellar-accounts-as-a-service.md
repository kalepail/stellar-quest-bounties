# Stellar accounts as a service

## Award
| Hunter | Reviewer | Type
| :- | :- | :-
| 2000 XLM | 800 XLM | Continuous

📜&nbsp; View [existing submissions](https://github.com/tyvdh/stellar-quest-bounties/issues?q=is%3Aissue+stellar-accounts-as-a-service+) for this bounty. \
🔵&nbsp; Start [hunting](https://github.com/tyvdh/stellar-quest-bounties/issues/new?assignees=&labels=&template=begin-the-hunt.yml&title=%F0%9F%94%B5+%60stellar-accounts-as-a-service.md%60) this bounty.

## Description

### What is this task?

Each Stellar account needs to hold 1 XLM to be valid. This can be costly when companies like exchanges want to build
on the Stellar network.

Currently, exchanges assign each of their users a unique id that should be put in the memo field of a transaction when depositing.
This approach is error-prone. Users can forget to add the memo, or they can input the wrong memo.

To solve this issue [muxed accounts](https://github.com/stellar/stellar-protocol/blob/master/core/cap-0027.md) were added to Stellar. Muxed accounts are essentially a way to combine Stellar addresses with integer identifiers.
Payments sent to a muxed account are actually sent to the account used to create the muxed account. However, the muxed account identifier is also added to the transaction.

For this bounty the task is to create an API for a [custodial](https://www.gemini.com/cryptopedia/crypto-wallets-custodial-vs-noncustodial) wallet service using muxed accounts.
A simple database should be used to keep track of the registered users, their muxed account addresses and their balances.

The api should have the following endpoints:

```
openapi: 3.0.1
info:
  title: Stellar accounts as a service
  description: 'This is the api specification for the Stellar accounts as a service bounty.'
  version: 1.0.0
tags:
- name: auth
  description: Authenticate yourself
- name: info
  description: Info
- name: pay
  description: Different ways to pay
paths:
  /register:
    post:
      tags:
      - auth
      summary: Create an account.
      requestBody:
        description: Credentials to register with.
        content:
          application/json:
            schema:
              properties:
                username:
                  type: string
                password:
                  type: string
        required: true
      responses:
        400:
          description: Invalid body.
        500:
          description: Catch all response for other errors aside from the ones listed.
          content:
            application/json:
              schema:
                properties:
                  error:
                    type: string
                    description: Text explaining the error.
        
  /login:
    post:
      tags:
      - auth
      summary: Get an auth token.
      requestBody:
        description: Credentials to login with.
        content:
         application/json:
          schema:
            properties:
              username:
                type: string
              password:
                type: string
        required: true
      responses:
        200:
          description: Successful login.
          content:
            application/json:
              schema:
                properties:
                  apikey:
                    type: string
        400:
          description: Invalid Body.
  /info:
    get:
      tags:
      - info
      security:
        - bearerAuth : []
      summary: Get info about the user's address and XLM balance.
      responses:
        200:
          description: Sucessful operation.
          content:
            application/json:
              schema:
                properties:
                  address:
                    type: string
                    description: The user's address.
                  balance:
                    type: string
                    description: The user's balance in XLM.
        401:
          description: Invalid api key.
  /pay:
    post:
      tags:
      - pay
      security:
       - bearerAuth: []
      summary: Pay Stellar accounts with XLM.
      requestBody:
        required: true
        description: Destination address and amount in XLM
        content:
          application/json:
            schema:
              properties:
                destination:
                  type: string
                  description: Address to send XLM to.
                amount:
                  type: string
                  description: Amount of XLM to send.
      responses:
        200: 
          description: Successful payment.
        401:
          description: Invalid api key.
        404:
          description: Dstination address does not exist.
        400:
          description: Invalid body
        500:
          description: Catch all response for other errors aside from the ones listed.
          content:
            application/json:
              schema:
                properties:
                  error:
                    type: string
                    description: Text explaining the error.
          
  
components:
  securitySchemes:
    bearerAuth:     
      type: http
      scheme: bearer
```      


### What are the requirements for the bounty hunter?
The hunter should be able to make simple Web APIs.

### What are the deliverables?

#### Bounty Description
- The hunter should provide a link to the repository containing the solution.
- The API should be hosted online or posted to a website like [repl.it](https://replit.com/~) to make it easier for reviewers to review the solution.
- The API **must** be served over https
- The API **must not** use the _PUBLIC_ network


#### Review Criteria
- The API should be tested to insure proper functionality.
- Code quality is not of primary importance but should be reasonable reviewable.
- Security is also not primarily important but at least some attention should have been paid to security. Basic things like hashing passwords and mitigating SQL injections should have been done.

## Links
- [repl.it for hosting the api](https://replit.com/~)
- [glitch.com for hosting the api](https://glitch.com/)
- [tutorial about setting up a custodial account](https://developers.stellar.org/docs/building-apps/setup-custodial-account/)
- [muxed accounts](https://github.com/stellar/stellar-protocol/blob/master/core/cap-0027.md)
