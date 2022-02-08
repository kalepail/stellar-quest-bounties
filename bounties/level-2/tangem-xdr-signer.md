# Tangem Web XDR Signer
## Award
| Hunter | Reviewer | Type
| :- | :- | :-
| 3500 XLM | 1500 XLM | Competitive | 

[//]: # (make sure to replace the file-name placeholders `<BOUNTY_FILE_NAME_NO_EXTENSION>`, `<BOUNTY_FILE_NAME_WITH_EXTENSION> and `<LEVEL>` in the next two lines with the respective values)
📜&nbsp; View [existing submissions](https://github.com/tyvdh/stellar-quest-bounties/issues?q=is%3Aissue+label%3Atangem-xdr-signer) for this bounty. \
🔵&nbsp; Start [hunting](https://github.com/tyvdh/stellar-quest-bounties/issues/new?assignees=&labels=&template=begin-the-hunt.yml&link=https://github.com/tyvdh/stellar-quest-bounties/blob/main/bounties/level-2/tangem-xdr-signer.md) this bounty.

## Description
Tangem is a company that produces hardware wallets and one of the supported cryptocurrencies is Stellar. You can access your Stellar Account using a compatible NFC phone and send payments by holding the card near your phone. 

The current problem is there is no easy way to sign transactions when a website asks you. The goal if this task is to bridge a hardware wallet that communicates with NFC to the web

### What is this task?
The goal of this project is to bridge an NFC wallet and the web. Luckily Tangem provides an API that can interact with the card. All that has to be done is to build a nice web browser extension and mobile app that can interact with the card.

This bounty can be separated into 2 Main objectives:

1) Create a browser extension that developers will be able to call with an XDR to later transfer to a phone app

Or

1) Create a website where you can paste an XDR that will later transfer the XDR to the phone app

2) The app should accept an XDR either via a QR Code or something better. The App should use the Tangem SDKs to sign the XDR and return it to the extension or website.

Here's a design idea on how the App and Extension should look like: 

![Design Preview](../../assets/tangem-design-preview-.png)

### What are the requirements for the bounty hunter?
For this bounty to be completed a GitHub repository with an Open Source License are required to be submitted. The GitHub repository should also include instructions on how to easily compile everything or provide build scripts that will do that for the developer.

It would be nice if the code is easily readable and documented.

You can use any tech stack you want to build the XDR signer. Make sure it has a good UI/UX experience and works well :D

### What are the deliverables?

#### Bounty Description
- The hunter should provide a link to a GitHub or GitLab repository that addresses a solution to the problem
- Links where we can test the Signer without compiling it ourselves

#### Submission Procedure
- The bounty will only be considered complete, after a GitHub repository has been submitted and a preview of the submission has been provided.

## Links
- [Tangem iOS SDK](https://github.com/tangem/tangem-sdk-ios)
- [GitHub - tangem/tangem-sdk-android: The native Kotlin library for Android and JVM platforms (Windows, Linux, macOS)](https://github.com/tangem/tangem-sdk-android)
- [Tangem Flutter SDK](https://github.com/tangem/tangem-sdk-flutter)

