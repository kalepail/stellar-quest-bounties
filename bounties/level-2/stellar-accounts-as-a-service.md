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
on Stellar.

Currently, exchanges assign each of their users a unique id that should be put in the memo field of a transaction when depositing.
This approach is error-prone. Users can forget to add the memo, or they can input the wrong memo.

To solve this issue [muxed accounts](https://github.com/stellar/stellar-protocol/blob/master/core/cap-0027.md) were added to Stellar. Muxed accounts are essentially a way to combine Stellar addresses with integer identifiers.
Payments sent to a muxed account are actually sent to the account used to create the muxed account. However, the muxed account identifier is also added to the transaction.

For this bounty the task is to create an API for a custodial wallet service using muxed accounts.
A simple database should be used to keep track of the registered users, their muxed account addresses and their balances.

The api should have the following endpoints:
```
POST /register

POST body: {
  username: "<Username to register with">,
  password: "<Password to register with>"
}

Endpoint info:
Making a POST request to this endpoint allows users to register an account with the service.
The request body should be in JSON format.
```
```
POST /login

POST body: {
  username: "<Username to login with">,
  password: "<Password to login with>"
}

Server response: {
  apikey: "<Sometype of api key to use the service>"
}

Endpoint info:
Making a POST request to this endpoint allows users to receive an apikey which can be used to use the service.
The request body should be in Json format and the server response is a JSON object.

```
```
GET /info 

Request headers : {
  Authorization : "Bearer <APIKEY>" 
}

Server response: {
  address: "<your muxed account address>",
  balance: "<your account balance in xlm>"
}

Endpoint info:
Making a request to this endpoint allows users to receive information about their account address and their XLM balance.
The Server response is a Json object.
```
```
POST /pay

Request Headers : {
  Authorization: "Bearer <APIKEY>" 
}

POST body: {
  destination: "<stellar address or muxed account address>",
  amount: "<amount of xlm to send>"
}

Endpoint info:
Making a request to this endpoint allows users to send XLM to stellar accounts.
```


### What are the requirements for the bounty hunter?
The hunter should be able to make simple Web APIs.

### What are the deliverables?

#### Bounty Description
- The hunter should provide a link to the repository containing the solution.
- The API should be hosted online or posted to a website like [repl.it](https://replit.com/~) to make it easier for reviewers to review the solution.


#### Review Criteria
- The API should be tested to insure proper functionality.
- Code quality is not of primary importance but should be reasonable reviewable.
- Security is also not primarily important but at least some attention should have been paid to security.

## Links
- [repl.it for hosting the api](https://replit.com/~)
- [glitch.com for hosting the api](https://glitch.com/)
- [tutorial about setting up a custodial account](https://developers.stellar.org/docs/building-apps/setup-custodial-account/)
- [muxed accounts](https://github.com/stellar/stellar-protocol/blob/master/core/cap-0027.md)
