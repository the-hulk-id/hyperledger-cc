# hyperledger-cc


### Chaincode (Smart contract) for Digital-ID project on Hyperledger technology
A simple smart contract for performance test against another blockchain technologies
(Quorum, Corda). It receive random chunk of data and perform SHA256 3 times before
write transaction with this following format

`Sequence+RandomData+sha1+sha2+sha3`

Where 
- Sequence: is a running number provided by client application
- RandomData: is a random chunk of data in various size, provided by client application
- sha1: Result from SHA256(RandomData+"1")
- sha2: Result from SHA256(RandomData+"2")
- sha3: Result from SHA256(RandomData+"3")


#### Chaincode method
`{'Args': ["writeBlock", "<sequence_number>", "<random_data>" ]}'`
