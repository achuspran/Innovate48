# Customer Data Management Using Verifiable Credentials and Zero Knowledge Proofs

## FIS Enterprise Customer (EC)

##### A key component of FIS’ Core Modernization Strategy
Provide financial institutions with comprehensive Customer Information Management across all lines of business.
![Slide3.png](https://www.dropbox.com/s/6b4364z921n3bef/Slide3.png?dl=0&raw=1)

## Customer Data Management Concerns
#### User
* Disclosing unwanted personal information
* Chances of data misuse
* Data being shared with other third parties 

#### Bank
* Difficulty in verifying Customer Data
* Expensive to store Customer NPI data
* Adherence to data protection regulations

### Demo
Harry opening a bank account with NextGenBank ![slide5.png](https://www.dropbox.com/s/ljaha8y3reehhdr/slide5.png?dl=0&raw=1)

#### Self Sovereign Identity (SSI) 
* Self Sovereign identity provides decentralized trust to verify Customer information
![slide6.png](https://www.dropbox.com/s/gbv6hxphcjyiyno/slide6.png?dl=0&raw=1)

#### Decentralized Identifier (DID) 
* Key component of Self Sovereign identity is a Decentralized Identifier or DID
![slide7.png](https://www.dropbox.com/s/w4mulfp4fawwrxp/slide7.png?dl=0&raw=1)
* DIDs are globally unique identifiers created by their owner, independent of any central authority
* DIDs point to a DID definition having public keys, endpoints and other information about the owner

# Solution
Integrate Self Sovereign Identity (SSI) to Enterprise Customer providing Digitally Verifiable Identity proofs Selective disclosure of data Zero Knowledge Proofs.

# Architecture Overview
* Leveraging Hyperledger Indy project for Self Sovereign Identify framework
* Integrate SSI agent within Enterprise Customer to process Credential proofs 
![slide9.png](https://www.dropbox.com/s/3kptmz1bxmmxuud/slide9.png?dl=0&raw=1)
# Hyperledger Indy
![slide10a.png](https://www.dropbox.com/s/izezydfsvet5pzy/slide10a.png?dl=0&raw=1) ![slide10b.png](https://www.dropbox.com/s/izueqgp00uxqkaf/slide10b.png?dl=0&raw=1)
* One of the projects under the Hyperledger platform, an open source global collaboration hosted by The Linux Foundation to advance cross-industry Blockchain technologies
* Distributed ledger, purpose-built for decentralized identity
* Public Permissioned Blockchain, validators are within the eco system

### SSI Adoption 
* Current adoption overview
* Dept of Canada – VON 
#### Process Explained - #1 Issuers
* Department of Transport (DoT), General Motors etc. are Issuers of Customer Identity. Eg. Driving License, Employment proof etc.
* DID for issuers are present in Blockchain Ledger and verified
* Issuers generate digitally signed identity proofs (credentials) for members/participants. Eg. Driving License for applicants.
* Credentials follow a credential definition which lists each individual element within the identity proof.
* Issuers update Revocation registry in Blockchain Ledger to add membership for the newly created credentials.
* Revocation registry can be updated anytime to remove membership for credentials that are revoked.

#### Process Explained - #2 Customers
* Customer sets up an agent and wallet in his mobile/laptop.
* Contact issuers to receive identity proofs (credentials).
* Customer shares the connection DID and blinded linked secret.
* Issuers issue credentials to the customer.
* Credentials are securely stored in his own wallet (agent in his mobile/laptop).
![slide15.png](https://www.dropbox.com/s/3hk4ognxjfmvc11/slide15.png?dl=0&raw=1)
#### Process Explained - #3 Bank (EC)
* Depending on the product selected by Customer, EC issues a proof request with information needed for account opening.
* Proof requests can, in addition to the data elements needed, also indicate if it need to be from a specific Issuer.
[image]
* Customer’s SSI agent receives the proof request and generates a response combining data from multiple credentials.
* On receiving the proof response, EC can verify the issuer signature and revocation status.
[image]
* Proof responses are stored in EC.
* [image]
 # Benefits
* Ease of customer onboarding and verification.
* Improved data quality in EC having digitally verified customer data.
* Allows selective disclosure of data elements from an identity document.
* Support for Zero Knowledge Proof – helps capture and verify Customer demographic details without requesting the underlying data.



