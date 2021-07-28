# Bounty Submissions Voting

| Hunter | Agent
| :- | :-
| 2000 XLM | 4 Credits

## Description

### What is this task?
In order to make it fair and create competitiveness, we need to allow multiple submissions of certain bounty. With this in mind, we may need a voting mechanism to decide prize winners.

 - Some bounties can be time-limited, which mean we would only accept submissions during certain time period. Need a way to encourage early submitters and fight copycat.
 - For such bounties, we can have maximum 3 winners to share the pool (100 - 60/40 - 50/35/15, respectively for number of maximum winners).
 - Only Senior Agents votes which can be done using Github reactions as MVP, are counted in the result
 - Optionally, create a Github Bot to conduct voting and announce the winners. The bot can check the list of all agents and their respective levels in a JSON file.

### What are the requirements for the bounty hunter?

The developer should have knowledge of using Github and Github Bot

### What are the deliverables?
The developer should provide a completed fork of the bounty repository implementing new functionality with at least below items:
 - [ ] Github Bot to conduct voting for voting required bounty
 - [ ] Github Bot to announce winners by counting votes by Senior Agents defined in a config file

#### *Judging Criteria and Metrics*
 - [ ] Code Quality - Is the code well-organized and documented? Does it adhere to language-specific style guidelines?
 - [ ] UI/UX - Is it easy to follow the bot messages?

#### *Submission Procedure*

 - Fork the bounty [repository](https://github.com/tyvdh/stellar-quest-bounties) and submit a PR with implemented solution
 - Create a [new issue](https://github.com/tyvdh/stellar-quest-bounties/issues/new) in the bounty [repository](https://github.com/tyvdh/stellar-quest-bounties)
   - Choose `review <title of the bounty issue>` as the issue's title
   - In the new issue description link to the original bounty issue and your PR in laboratory repository
   - Add a comment to the bounty issue linking to your newly created review issue to denote it being ready for review

## Links
 - https://github.com/stellar/laboratory
 - https://laboratory.stellar.org/#?network=test
