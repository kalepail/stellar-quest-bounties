# Create a Cloud Flare Workers template for serving .well-known/stellar.toml files
## Award
| Hunter | Reviewer | Type
| :- | :- | :-
| {400} XLM | {200} XLM | Capped ({1})

[//]: # (make sure to replace the file-name placeholders `<BOUNTY_FILE_NAME_NO_EXTENSION>`, `<BOUNTY_FILE_NAME_WITH_EXTENSION> and `<LEVEL>` in the next two lines with the respective values)
📜&nbsp; View [existing submissions](https://github.com/tyvdh/stellar-quest-bounties/issues?q=is%3Aissue+label%3Acf-workers-stellar-toml-template) for this bounty. \
🔵&nbsp; Start [hunting](https://github.com/tyvdh/stellar-quest-bounties/issues/new?assignees=&labels=&template=begin-the-hunt.yml&link=https://github.com/tyvdh/stellar-quest-bounties/blob/main/bounties/level-1/cf-workers-stellar-toml-template.md) this bounty.

## Description

### What is this task?

Create a cloudflare workers (MODULES) template that can be used to create a worker who's purpose is to server a stellar.toml file.

### What are the requirements for the bounty hunter?

This should utilize javascript to serve the toml and the cloudflare workers KV namespace to store the stellar.toml.  
It should also have an easy to fork/deploy repository.

### What are the deliverables?

Deliver the github repository, and an example domain showing functionality.

#### Bounty Description
  - A github repo with a cloudflare workers template.
  - The template should serve valid stellar.toml files
  - The stellar.toml files should be stored in the workers KV namespace
  - Deliverables are the github repo with codebase, and a functional example.

#### Review Criteria
  - Reviewers should be able to build and deploy the worker to CF workers
  - Reviewers should check the code for general style and completeness, and provide suggestions for changes where necessary.
  - If it is missing any of the requirements above, it is not yet ready for review.
  
#### Submission Procedure
  - Create an issue in SQ bounties repo with the name of "cf-workers-stellar-toml-template - Bounty submission"
  - The issue should include a link to the PR of your worker template.

## Links*
- [Cloudflare Workers Examples](#https://github.com/cloudflare/cloudflare-docs/tree/26f8bfc4bfd2e5127334e4a462342cd03148eaea/products/workers/src/content/examples)
- [Cloudflare Workers](#https://workers.cloudflare.com/)
- [Cloudflare Workers Docs](#https://developers.cloudflare.com/workers/)
- [~~Get Rick Rolled~~](https://youtu.be/dQw4w9WgXcQ)

## Ideas*
- Please use es modules rather than service workers.

