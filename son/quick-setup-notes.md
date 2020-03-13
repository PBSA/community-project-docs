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

### Create  Peerplays Accounts

### Register SON

### Configuration files

TODO

### Starting the node

```text
witness_node 
# If you need the logs, the following can be helpful
# witness_node 2>&1 peerplays.log
```

