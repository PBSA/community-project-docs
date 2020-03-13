# Quick Setup notes

This is a quick document which assumes that the user has experience in setting up various Graphene blockchains before. The following link can be a good refresher: [https://www.peerplays.tech/witnesses/becoming-a-witness](https://www.peerplays.tech/witnesses/becoming-a-witness)

### Prepare the server

The following dependencies are necessary for a clean Ubuntu 18.04 LTS

```text
sudo apt-get install autoconf bash build-essential ca-certificates cmake \
     doxygen git graphviz libbz2-dev libcurl4-openssl-dev libncurses-dev \
     libreadline-dev libssl-dev libtool libzmq3-dev locales ntp pkg-config \
     wget
```

### Download SON executable

Go to [https://gitlab.com/PBSA/peerplays/-/jobs](https://gitlab.com/PBSA/peerplays/-/jobs) and find the job ID for the build you want to use. Build should have the following properties

* Job: features/SONs-base
* Stage: build
* Name: build

Example of such a job has ID 467332251:

{% embed url="https://gitlab.com/PBSA/peerplays/-/jobs/467332251" %}

To download executables, click Download button on the right side of the Job page, or execute the following command:  
`wget --content-disposition --show-progress` [`https://gitlab.com/PBSA/peerplays/-/jobs/467332251/artifacts/download`](https://gitlab.com/PBSA/peerplays/-/jobs/467332251/artifacts/download)\`\`

To unpack executables in current folder:

`unzip -j artifacts.zip programs/cli_wallet/cli_wallet -d ./  
unzip -j artifacts.zip programs/witness_node/witness_node -d ./`

### Building Peerplays SON \(optional\)

To build Peerplays from source, refer to the README.md file:

{% embed url="https://github.com/peerplays-network/peerplays/blob/feature/SONs-base/README.md" %}

### SON configuration

#### Prerequisites

* Your node is up and running and synced with the network.
* You have access to a bitcoin node, with RPC and ZMQ notifications enabled
* You have access to shared wallet used by all SONs \(prerelease requirement only\)

#### Configuration files

SON plugin is controlled by following parameters

```text
peerplays_sidechain plugin. <no description>
Options:
  --son-id arg                          ID of SON controlled by this node (e.g.
                                        "1.27.5", quotes are required)
  --son-ids arg                         IDs of multiple SONs controlled by this
                                        node (e.g. ["1.27.5", "1.27.6"], quotes
                                        are required)
  --peerplays-private-key arg (=["TEST6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV","5KQwrPbwdL6PhXujxW37FSSQZ1JiwsST4cqQzDeyXtP79zkvFD3"])
                                        Tuple of [PublicKey, WIF private key] 
                                        (may specify multiple times)
  --bitcoin-node-ip arg (=99.79.189.95) IP address of Bitcoin node
  --bitcoin-node-zmq-port arg (=11111)  ZMQ port of Bitcoin node
  --bitcoin-node-rpc-port arg (=22222)  RPC port of Bitcoin node
  --bitcoin-node-rpc-user arg (=1)      Bitcoin RPC user
  --bitcoin-node-rpc-password arg (=1)  Bitcoin RPC password
  --bitcoin-wallet arg                  Bitcoin wallet
  --bitcoin-wallet-password arg         Bitcoin wallet password
  --bitcoin-private-key arg (=["02d0f137e717fb3aab7aff99904001d49a0a636c5e1342f8927a4ba2eaee8e9772","cVN31uC9sTEr392DLVUEjrtMgLA8Yb3fpYmTRj7bomTm6nn2ANPr"])
                                        Tuple of [Bitcoin public key, Bitcoin 
                                        private key] (may specify multiple 
                                        times)
  
```

These parameters are available from both command line and config file:

```text
# ==============================================================================
# peerplays_sidechain plugin options
# ==============================================================================

# ID of SON controlled by this node (e.g. "1.27.5", quotes are required)
son-id = "1.27.0"

# IDs of multiple SONs controlled by this node (e.g. ["1.27.5", "1.27.6"], quotes are required)
son-ids = []

# Tuple of [PublicKey, WIF private key]
peerplays-private-key = ["TEST6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV", "5KQwrPbwdL6PhXujxW37FSSQZ1JiwsST4cqQzDeyXtP79zkvFD3"]

# IP address of Bitcoin node
bitcoin-node-ip = 99.79.189.95

# ZMQ port of Bitcoin node
bitcoin-node-zmq-port = 11111

# RPC port of Bitcoin node
bitcoin-node-rpc-port = 22222

# Bitcoin RPC user
bitcoin-node-rpc-user = 1

# Bitcoin RPC password
bitcoin-node-rpc-password = 1

# Bitcoin wallet
bitcoin-wallet = son-wallet

# Bitcoin wallet password
bitcoin-wallet-password = 9da115c9fa6fe7fd09390841ac91aee4

# Tuple of [Bitcoin public key, Bitcoin private key] (may specify multiple times)
bitcoin-private-key = ["02d0f137e717fb3aab7aff99904001d49a0a636c5e1342f8927a4ba2eaee8e9772","cVN31uC9sTEr392DLVUEjrtMgLA8Yb3fpYmTRj7bomTm6nn2ANPr"]

```

### Becomming a SON

Becomming a SON is very similar to becoming a witness. You will need:

* Active user account which will be the owner of SON account
* Create two vesting balances \(types son and normal\) of 50 core assets, and get its IDs
* Create Bitcoin address for SON account in shared SON wallet
* Create SON account, and get its ID
* Set the signing key for a son account \(usually, its a signing key of owner account\)
* Set the bitcoin address as a sidechain address for a SON account
* Restart the witness with peerplays\_sidechain plugin enabled

### Starting the node

```text
witness_node 
# If you need the logs, the following can be helpful
# witness_node 2>&1 peerplays.log
```

