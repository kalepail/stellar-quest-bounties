# Operation Reorder improvement for Stellar Laboratory

| Hunter | Agent
| :- | :-
| 550 XLM | 3 Credits

## Description

### What is this task?

In the stellar laboratory's transaction builder it is possible to re-order operations by entering a new number as the desired position
in the order-input box to the very left of the operation-entry:
![grafik](https://user-images.githubusercontent.com/1752217/127267291-878bb2bf-c42f-470b-aa22-26fe4a51cc95.png)

This approach has the advantage that an operation could be repositioned anywhere in a long list of operations with a single action.
Unfortunately it is not very intuitive and could be improved by UI elements (e.g. up-/down arrows). Further a hint explaining the box's
functionality would be really helpful.

### What are the requirements for the bounty hunter?

* The developer should have knowledge of Stellar Laboratory.
* The developer should have a good sense for UI/UX and knowledge of CSS as such elements don't exist in the lab, yet.

### What are the deliverables?

*Description* <br>
  * The developer should provide a completed fork of the laboratory implementing new functionality
    * Add UI elements that allow re-ordering an operation by one position up or down
      * first operation can only be moved down (up-element must be either inactive or hidden)
      * last operation can only be moved up (down-element must be either inactive or hidden)
    * Hint/Tooltip explaining the oder box's functionality (optional)

*Judging Criteria and Metrics* <br>
  * Code Quality - Is the code well-organized and documented? Does it adhere to language-specific style guidelines?
  * UX/UI - Do the added elements fit well into the lab's design and are intuitive to use?
  
*Submission Procedure* <br>
  * Create a fork of the [lab repository] and implement the solution
  * Create a pull-request from your submission into the [lab repository]
    * make sure to follow their [contribution guidelines](https://github.com/stellar/laboratory/blob/master/CONTRIBUTING.md)
  * [Add a link](https://github.com/tyvdh/stellar-quest-bounties/edit/main/bounties/level-2/stellar-lab-improve-reorder-ux.md) to your pull-request to the [submissions](https://github.com/tyvdh/stellar-quest-bounties/blob/main/bounties/level-2/stellar-lab-improve-reorder-ux.md#submissions) section below
    * create a PR to merge the patch-branch (the one that adds your submission to this file) into `main` branch
      * choose `review <title of the bounty-issue>` as title for your PR
      * mention the bounty-issue in the PR description field

## Submissions


## Links

- https://github.com/stellar/laboratory
- https://laboratory.stellar.org/#txbuilder


[lab repository]: https://github.com/stellar/laboratory
