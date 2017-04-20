# CS480 Blockchain Application

Poll Creator using Blockchain API

### Blockchain

## Setup
https://www.ibm.com/developerworks/java/library/j-chaincode-for-java-developers/index.html

## IP address
http://172.16.198.132:7050

## Requirements Analysis

### Project Requirements
* Utilize a block-chain platform to achieve functionality

### Application Requirements
* Create a new poll
* Find existing polls to vote for
* Submit voting option selections to the poll
* Polls are valid only for a certain length of time
* Poll results are immutable once the deadline passes

### Execution of Steps
1. [Poll Creator] creates a new poll
2. [Poll Creator] inserts poll details
3. Application publishes poll
3a. User details

4. [Poll Voter] finds a poll
5. [Poll Voter] selects voting choices
5a. Voting selection transaction is verified by [Blockchain API]
6. [Blockchain API] adds vote selection to the blockchain

7. Poll expires and triggers generation of poll results
7a. Poll result analysis and statistics are generated


