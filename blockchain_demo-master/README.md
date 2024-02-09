# blockchain_demo

## Basic BlockChain Demo App in Python (Flask)

This is a very simple proof of concept project which allows to run multiple
blockchain Nodes and Clients. The Nodes can accept transactions, add to the
blocks and chain the blocks. There is a basic functionality to resolve
conflicts, mine and validate the chain. All features are accessible via
a simple web interface.

## Manual

Make sure you have `virtualenv` or `pipenv`. All required dependencies
are in `requirements.txt`. 

To load dependencies:

`pip install -r requirements.txt`

Easiest way to run the whole thing is to do it locally:

1. To run couple of nodes - you can multiply them by e.g. setting various port numbers.
E.g.
`python blockchain/blockchain.py -p 5001`, 
`python blockchain/blockchain.py -p 5002`, etc.

2. To run couple of clients - same trick:
e.g.
`python blockchain_client/blockchain_client.py -p 8081`,
`python blockchain_client/blockchain_client.py -p 8082`, etc.

### As a client:

E.g. http://127.0.0.1:8081/

Using UI you can:
1. Generate Wallet (public/private key pair)
2. Submit new transaction
3. View the list of transactions in the blockchain

### On the node:

E.g. http://127.0.0.1:5001/

Using IU you can:
1. Mine new block
2. Configure other nodes
3. Resolve conflicts with known nodes and keep the blockchain up to date

---

## Screenshots

### Pic. 1 - Generate Wallet:
![](screenshots/Selection_061.png?raw=true "Generate Wallet")

### Pic. 2 - Make transaction:
![](screenshots/Selection_062.png?raw=true "Title")

### Pic. 3 - Successful transaction submission:
![Alt text](screenshots/Selection_063.png?raw=true "Title")

### Pic. 4 - List of transactions and the blockchain (before mining):
![Alt text](screenshots/Selection_064.png?raw=true "Title")

### Pic. 5 - List of transactions and the blockchain on the first node (after mining):
![Alt text](screenshots/Selection_065.png?raw=true "Title")

### Pic. 6 - Configuration of the blockchain nodes:
![Alt text](screenshots/Selection_066.png?raw=true "Title")

### Pic. 7 - Blockchain on the second node after conflict resolution:
![Alt text](screenshots/Selection_067.png?raw=true "Title")
