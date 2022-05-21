# VeriScrbe
Hackathon submissions here:   
https://devpost.com/software/veriscribe-0hz6sq  
https://devpost.com/software/veriscribed  

Submitted to RookieHacksII and Technica  

Prescription NFTs, a way to prevent forged and altered prescriptions.

## Prerequisites

* A testnet or mainnet account (head to https://portal.hedera.com to create an account if you don't have one)
* Node.js v14.9.0
* Yarn 1.22.10
* Docker 
* Docker compose (optional)


## To Run

### Project setup
```
yarn install
```

#### Compiles and hot-reloads for development
```
yarn serve
```

#### Compiles and minifies for production
```
yarn build
```

#### Lints and fixes files
```
yarn lint
```

## Inspiration
Prescription drug fraud and misuse is a significant and growing problem. Users obtain prescription drugs unlawfully in numerous ways, including the following:
- Forging prescriptions
- Consulting multiple doctors to obtain prescriptions ("doctor shopping")
- Altering prescriptions to increase the quantity
- Obtaining prescribed drugs illegally through the Internet
- Acquiring drugs that were legally prescribed to family members or friends

We create VeriScribe, a prescription verification system built on the Hedera network, that attempts to solve the first 3 bullets above. By securely, but publicly recording a prescription on the network, pharmacies are able to verify the authenticity and origin of the prescription, ensuring that the prescriptions were not altered or forged. It also allows for protection against "doctor shopping", as they can check if the client was prescribed multiple times. Our initial demo is a proof-of-concept build, that shows how creation of NFT prescriptions would work.

## What it does
Our proof of concept has 3 users - the doctor (Issuer), the patient (Alice), and the pharmacist (Bob). The doctor can create a NFT prescription, that includes the prescription data, as well as their identification (DEI and NPI numbers). They create and mint a single NFT and transfer it to the patient. The patient then transfers this to the pharmacist when they go to have the prescription filled out. Alice cannot forge this NFT, as Bob can verify that it came from the wallet of the doctor. Alice also cannot change it as the history is recorded on the blockchain.

## How we built it
We built this on top of the hedera hashgraph network. We use react with the hedera sdk and vue to create the front end accessing the hedera api.

## Challenges we ran into
With new hackers, we had a bit of trouble getting the environments set up for developing with hedera, as well as getting the project set up. There were a lot of requirements for installing and being able to run the application. We also ran into some problems when creating the application. We had trouble associating tokens with accounts, as well as figuring out how to modify token properties. User anonymity was also a problem that arose (specifically HIPPA violations) in what would essentially be a publicly available user prescription database.

## Accomplishments that we're proud of
- Completing the hackathon!
- Running the application and minting and transferring NFTs
- Learning to use hedera and npm
- Using vue for the first time (and hedera)

## What's next for VeriScribe
- Allow doctors to register themselves, and only allow their wallet address to add their NPI or DEA numbers.
- Allow better view of the history of NFT
- Allow lookup for doctors and pharmacists
- Anonymity, since some prescriptions are very specific, even without names or DOB attached to them




