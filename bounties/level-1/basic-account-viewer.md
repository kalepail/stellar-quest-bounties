# Basic account viewer

| Hunter | Reviewer | Type
| :- | :- | :-
| 800 XLM | 400 XLM | Continuos

📜&nbsp; View [existing submissions](https://github.com/tyvdh/stellar-quest-bounties/issues?q=is%3Aissue+basic-account-viewer) for this bounty. \
🔵&nbsp; Start [hunting](https://github.com/tyvdh/stellar-quest-bounties/issues/new?assignees=&labels=&template=begin-the-hunt.yml&title=%F0%9F%94%B5+%60basic-account-viewer.md%60) this bounty.

## Description

### What is this task?

When building websites ontop of Stellar, there needs to be a way to access a user's Stellar account. This is where web-wallets like [Albedo](https://albedo.link/), [Rabet](https://rabet.io/) and [Freighter](https://www.freighter.app/) come in. They allow websites to easily and securely access your Stellar account.

Your task is to build a simple website which allows users to sign in and log out using a web-wallet like Albedo, Freighter or Rabet.

The website should show some basic information about the account currently logged in:
 * The asset-codes and balances of the account's assets should be shown.
 * The date when the account was created should be shown.
 * The account which created this account should be shown.

For this bounty, the UI is not of primary importance. However CSS and HTML should be used to create a simple layout. Additionally, the solution should be licensed as open source.
 
### What are the requirements for the bounty hunter?
* The hunter should be able to build simple websites with Javascript.

### What are the deliverables?
#### Description
  - The hunter should provide a link to the repository containing the solution.
  - The hunter should publish the website and provide a link to the published website.

#### Review Criteria
  - UI is not of primary importance but there should at least be a basic layout.
  - The code quality is also not primarily important but should function properly and be reasonably reviewable.
  - The code should be checked to insure the integration with the web-wallet is done correctly.

## Links
- [Albedo](https://albedo.link/)
- [Rabet](https://rabet.io/)
- [Freighter](https://www.freighter.app/)
- [Stellar js SDK](https://github.com/stellar/js-stellar-sdk)
- [Example of web-app with albedo sign in](https://app.lumenswap.io/swap)

## Ideas
 - Take a look at the [Stellar account viewer](https://github.com/stellar/account-viewer-v2) to see if you can get some ideas.
 - Consider using github pages to host the website. If react is used, check out [Hosting react website on github pages](https://github.com/gitname/react-gh-pages).
