# Land-Record-Management-using-Hyperledger-Fabric
Manage land records securely, over a decentralized, peer-to-peer network using Blockchain technology. Store valuable documents over the decentralized system of IPFS (Interplanetary File System).
This provides a lucid understanding of Hyperledger Fabric using Hyperledger Composer, to understand the concepts of network definitions in Hyperledger Fabric.

Prerequisites:
1. Docker-ce version 17.03.1-ce or greater, Docker Compose version 1.9.0 or greater., Docker-swarm (for multihost blockchain network), latest released Docker images for Hyperledger Fabric
2. npm version 8.11.2 or greater, node.js for Javascript coding, to connect to a deployed business network, to create, read, update and delete assets and participants and to submit transactions.
3. GoLang (to write chaincode, or smart contracts in the case of Hyperledger Fabric)
4. REST Server for CLI
5. Hyperledger Fabric

In Hyperledger Composer, business network definition is provided using the following primary components:

• Model file (.cto) : This defines entities of the network such as the Assets (land titles), Transaction/s (transfer of land ownership) and Participants (land owners) for the business network.

• Script file (.js) : Transaction Functions thereby defining the business logic are stated in this file. This is effectively the smart contract here. The Function first checks if the Asset is eligible for exchange between two Participants by checking if it is listed for sale, following which, it qualifies the Transaction entry with Buyer, Seller and Asset credentials. To maintain authenticity, transactionID and timestamp are assigned by the Fabric itself.

• Access control (.acl) : This file defines the authorization given to each Participant in the network. Participants such as Government officials on the various levels of the municipality have both, editing and viewing rights, and to prevent tampering of information, land-owners have only viewing rights.

• Query file (.qry) : Queries are written in bespoke Query language. 

These files are zipped together to form a Business Network Archive (.bna), and a .card definition that gets deployed on the running Fabric network. Consequently, connection profiles and user credentials are used to install and access the .bna file to a distributed ledger.
