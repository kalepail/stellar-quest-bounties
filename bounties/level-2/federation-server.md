# Implement a federation server for stellar addresses

## Award
| Hunter | Reviewer | Type
| :- | :- | :-
| 3200 XLM | 1500 XLM | Capped (2) 

[//]: # (make sure to replace the file-name placeholders `<BOUNTY_FILE_NAME_NO_EXTENSION>`, `<BOUNTY_FILE_NAME_WITH_EXTENSION> and `<LEVEL>` in the next two lines with the respective values)
📜&nbsp; View [existing submissions](https://github.com/tyvdh/stellar-quest-bounties/issues?q=is%3Aissue+label%3Afederation-server) for this bounty. \
🔵&nbsp; Start [hunting](https://github.com/tyvdh/stellar-quest-bounties/issues/new?assignees=&labels=&template=begin-the-hunt.yml&link=https://github.com/tyvdh/stellar-quest-bounties/blob/main/bounties/level-2/federation-server.md) this bounty.


## Description

We all love our 56-char stellar account-ids. But what about our friends we want to convince to also join stellar-familiy?
There are a few arguments could stand in the way of adoption:

- Most of the wallets don't have address-book functionality
- It is mentally challenging to match a stellar-address to an individual ([vanity-addresses](https://lumenaddr.com/faq.html) help a bit – leaving you with only around 50 chars of gobble)

> "Why can't I send you the money via email?"  
> -— <cite>Your friends</cite>

Well actually they kind of can; enter [federation].

While there are already numerous federation-servers out there – even a [reference implementation] –
you might not want to trust an external entity with your and your friends' addresses.
Further, you might want to hook the addresses to an existing community (think discord, github, twitter, …).


### What is this task?

Implement a [federation]-server that allows to sign-up (register) with an existing social-media-account provider
(e.g. discord, github, google, twitter – preferrably one out of the first two to make it easier for the reviewers).


### What are the requirements for the bounty hunter?

- You know how to implement and deploy an API
- You can implement an authentication-flow to allow signing up through a third-party account provider
- You know how to store and retrieve simple lookups (fed-address/account-id relation)


### What are the deliverables?

- A server application that  
  - allows configuring the domain, that is appended to the federation-addresses
  - provides a simple but appealing UI where anyone can sign-up and login through a social-media account-provider of your choice
    - allow a logged-in user to add, change or remove their stellar account-id
    - presents the user with their full federation-address consisting of their username and the domain (e.g. `@tyvdh*quest.stellar.org`)
    - allow logged-id user to delete their account
  - serves the `/federation` endpoint that 
    - supports at least the `name` query-type (see [federation protocol])
- Documentation that 
  - lays out the installation procedure
  - lays out the deployment process
  - details what query-types are supported by the `/federation` endpoint 


#### Bounty Description

To successfully hunt this bounty implement and publish a federation-server that allows your friends so sign-up with
their social-media account so you can start sending XML (or else) to your easy-to remember federation-addresses.

In order for your federation-server to be testable you need to also host a `/.well-known/stellar.toml` file
on the domain you want to federate. You may use github pages to serve to `toml`-file. Just make sure to configure
the federation server to match the github-pages domain.


#### Review Criteria

The reviewer needs to sign-up with the federation server and configure/add their account-id.  
The reviewer needs to query the server's `/federation` endpoint with all the query-types described in the documentation.  
The reviewer may chose the tooling of their choice (e.g. `curl` or the [js SDK](https://stellar.github.io/js-stellar-sdk/FederationServer.html))
and verify the correct response according to the [federation] server documentation. The reviewer may ask a second person to sign up with their
account to cross-verify.
The reviewer should remove/alter their account-id and verify that the reponse changes.
The reviewer should delete their account and verify that login does not work anymore.
Depending on the ID-provider the reviewer may on the ID-provider's side revoke access and check that
login actually stops working on the federation-server UI.

#### Submission Procedure

Implement the deliverables described above and add to the bounty-issue
- a link to the repository (preferably a PR from implementation branch into base branch – even in your repo)
- a link to the running application
- the name of the domain that the federation-server is configured to (e.g. quest.stellar.org or <your-user-name>.github.io)

Add the URL of the deployed federation-server to the github-repo's 'about' section.


## Links

- [federation] server documentation
- [reference implementation]
- [stellarID.io](https://stellarid.io/) has a UI to sign-up


## Ideas

The actual server endpoint is just a simple lookup in a key-value store. Before bringing up a whole DB like postgres or MySQL
you may consider using [cloudflare workers](https://workers.cloudflare.com/). They provide a [key-value interface](https://developers.cloudflare.com/workers/learning/how-kv-works)
that would perfectly fit the use-case.



[federation]: https://developers.stellar.org/docs/glossary/federation/
[reference implementation]: https://github.com/stellar/go/tree/master/services/federation
[federation protocol]: https://github.com/stellar/stellar-protocol/blob/master/ecosystem/sep-0002.md