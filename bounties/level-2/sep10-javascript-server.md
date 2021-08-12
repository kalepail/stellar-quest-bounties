# JavaScript SEP-0010 Server Reference Implementation

## Award

| Hunter | Reviewer | Type
| :- | :- | :-
| 3500 XLM | 2000 XLM | Capped (3)

[//]: # (make sure to replace the file-name placeholders `BOUNTY_FILE_NAME_NO_EXTENSION` and `BOUNTY_FILE_NAME_WITH_EXTENSION` in the next two lines with the actual bounty filename)
📜&nbsp; View [existing submissions](https://github.com/tyvdh/stellar-quest-bounties/issues?q=is%3Aissue+label%3Asep10-javascript-server) for this bounty. \
🔵&nbsp; Start [hunting](https://github.com/tyvdh/stellar-quest-bounties/issues/new?assignees=&labels=&template=begin-the-hunt.yml&link=https://github.com/tyvdh/stellar-quest-bounties/blob/main/bounties/level-2/sep10-javascript-server.md) this bounty.

## Description

### What is this task?

The Stellar ecosystem is comprised of many different developers, validators,
organizations, individuals, etc. that work together to make the network run in a
smooth, predictable, and reliable manner. To that end, there are many
**S**tellar **E**cosystem **P**roposals (**SEP**s) that serve to instruct the
network about how certain actions should (or should not) be done.

SEP-0010 is one such SEP which dictates how Stellar web authentication is to be
done. The SEP includes instructions on how servers should be developed, what
they are expected to send/receive, as well as how clients should interact with
those servers to authenticate to the network for purposes of establishing a
session for the user.

In order for developers to make use of these SEPs, many of them contain
"Reference Implementations," indicating what a *vanilla* example of the SEP
functioning in the real world might look like.

Your task, should you choose to accept it, is to build, document, and make
publicly available a fully-functional server-side application, written in
JavaScript, that fills the role of the server in the SEP-0010 authentication
flow.

When deployed, this implementation should successfully produce a **J**SON
**W**eb **T**oken (**JWT**) after authenticating with a client. All SEP-0010
endpoints should be working and producing the appropriate responses (both
success and error).

### What are the requirements for the bounty hunter?

The bounty hunter should be familiar with JavaScript, HTTP request methods, and
testing. They ought to be able to create a server-side application that receives
and responds to various API calls and endpoints.

### What are the deliverables?

#### Submission Procedure

  - The bounty hunter will submit a link to a GitHub repository containing the
    reference implementation.
  - The bounty hunter will submit a link to the SEP-0010 implementation hosted
    online (**must** be accessible through HTTPS).
  - The reference implementation will incorporate any necessary unit tests
    throughout the codebase.

#### Review Criteria

  - Reviewers will attempt to authenticate with the Stellar network, using the
    submitted server implementation.
  - Reviewers will examine each of the API endpoints for accurate responses.
  - Reviewers will inspect the JWT to ensure all relevant pieces are included.
  - Reviewers will pay special attention to testing the various conditional and
    optional pieces of the authentication flow.

## Links

- [SEP-0010 Specification](https://github.com/stellar/stellar-protocol/blob/master/ecosystem/sep-0010.md)
- [Implementation in Go](https://github.com/stellar/go/tree/master/exp/services/webauth)
- [Implementation for iOS and macOS](https://github.com/Soneso/stellar-ios-mac-sdk/blob/master/README.md#8-stellar-web-authentication)
- [JSON Web Tokens](https://jwt.io/)
- [You could host your implementation at repl.it](https://replit.com/)
