## Blockchain Setup

### Prereq
* install Docker
* install Go
* set GOPATH to docker directory
    * (Unix):
    $: export PATH=$PATH:~/blockchain/

### Start Hyperledger Network Image in Docker
* in directory containing docker-compose.yml
    $: docker-compose up

### Start Blockchain Server
* Unix:
    * ChaincodeTutorial/build/distributions/ChaincodeTutorial/bin/ChaincodeTutorial

### Add to Chain
    send json request:
    {
    "jsonrpc" : "2.0",
        "method" : "invoke",
        "params" : {
            "type" : 1,
            "chaincodeID" : {
                "name" : "PollTableName"
            },
            "CtorMsg" : {
                "args" : ["log", "key", "log msg"]
            }
        },
        "id" : 2
    }
    json response:
    {
        "jsonrpc" : "2.0",
        "result" : {
            "status" : "OK",
            "message" : "hash..."
        },
        "id" : 2
    }

### Query Chain
    send json request:
    {
    "jsonrpc" : "2.0",
        "method" : "invoke",
        "params" : {
            "type" : 1,
            "chaincodeID" : {
                "name" : "PollTableName"
            },
            "CtorMsg" : {
                "args" : ["query", "key1", "key2"]
            }
        },
        "id" : 3
    }
    json response:
    {
        "jsonrpc" : "2.0",
        "result" : {
            "status" : "OK",
            "message" : "hash..."
        },
        "id" : 2
    }
