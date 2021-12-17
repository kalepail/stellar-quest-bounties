# JavaScript SEP-0010 Client Reference Implementation

## Award

| Hunter | Reviewer | Type
| :- | :- | :-
| 1200 XLM | 800 XLM | Capped (3)

[//]: # (make sure to replace the file-name placeholders `BOUNTY_FILE_NAME_NO_EXTENSION` and `BOUNTY_FILE_NAME_WITH_EXTENSION` in the next two lines with the actual bounty filename)
📜&nbsp; View [existing submissions](https://github.com/tyvdh/stellar-quest-bounties/issues?q=is%3Aissue+label%3Asep10-javascript-client) for this bounty. \
🔵&nbsp; Start [hunting](https://github.com/tyvdh/stellar-quest-bounties/issues/new?assignees=&labels=&template=begin-the-hunt.yml&link=https://github.com/tyvdh/stellar-quest-bounties/blob/main/bounties/level-2/sep10-javascript-client.md) this bounty.

## Description

### What is this task?

The Stellar ecosystem is comprised of many different developers, validators,
organizations, individuals, etc. that work together to make the network run in a
smooth, predictable, and reliable manner. To that end, there are many
**S**tellar **E**cosystem **P**roposals (**SEP**s) that serve to instruct the
network about how certain actions should (or should not) be done.

The **[SEP-0010 specification](https://github.com/stellar/stellar-protocol/blob/master/ecosystem/sep-0010.md)**
is one such SEP which dictates how Stellar web authentication is to be done. The
SEP includes instructions on how servers should be developed, what they are
expected to send/receive, as well as how clients should interact with those
servers to authenticate to the network for purposes of establishing a session
for the user.

In order for developers to make use of these SEPs, many of them contain
"Reference Implementations," indicating what a *vanilla* example of the SEP
functioning in the real world might look like.

Your task, should you choose to accept it, is to build, document, and make
publicly available a fully-functional client-side application, written in
JavaScript, that fills the role of the client in the SEP-0010 authentication
flow.

When used, this implementation should successfully receive valid a **J**SON
**W**eb **T**oken (**JWT**) after authenticating with a SEP-0010 server.

### What are the requirements for the bounty hunter?

The bounty hunter should be familiar with JavaScript and HTTP request methods.
They should feel comfortable interacting with servers through GET/POST requests.

### What are the deliverables?

#### Submission Procedure

  - The bounty hunter will submit a GitHub repository containing their SEP-0010
    client, coded in either JavaScript or TypeScript.
  - The submitted SEP-0010 client will adhere closely to the
    **[SEP-0010 specification](https://github.com/stellar/stellar-protocol/blob/master/ecosystem/sep-0010.md)**
    as described in the `stellar/stellar-protocol` repository.
  - The bounty hunter will submit a link to their SEP-0010 client implementation
    hosted online (**must** be available through HTTPS).
  - The hosted client will include a user interface that will perform these
    tasks:
    1. Generates a JWT by successfully authenticating with the Test Anchor,
    1. Retrieves and displays that JWT to the user (including information about
       all the pieces of the JWT), and
    1. Performs some testing of the JWT for validity.

#### Review Criteria

  - Reviewers will proceed through the authentication flow both with and without
    a client home domain, ensuring a valid JWT is returned in both cases.
  - Reviewers will attempt to receive a valid JWT from the Stellar Test Anchor,
    utilizing each of the various conditional and optional elements of the
    authentication flow.
  - Reviewers will examine the client code to ensure a clean and clear codebase,
    with sufficient tests in place.
  - Reviewers will inspect the JWT to ensure all relevant pieces are included.

## Links

- [SEP-0010 Specification](https://github.com/stellar/stellar-protocol/blob/master/ecosystem/sep-0010.md)
- [Implementation for iOS and macOS](https://github.com/Soneso/stellar-ios-mac-sdk/blob/master/README.md#8-stellar-web-authentication)
- [Stellar Test Anchor Webauth endpoint](https://testanchor.stellar.org/auth)
- [JSON Web Tokens](https://jwt.io/)
