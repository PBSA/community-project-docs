# Quick Setup notes

This is a quick document which assumes that the user has experience in setting up various Graphene blockchains before. The following link can be a good refresher: [https://www.peerplays.tech/witnesses/becoming-a-witness](https://www.peerplays.tech/witnesses/becoming-a-witness)

### Prepare the server

```text
sudo apt-get -y install gcc g++ cmake make\
 libbz2-dev libdb++-dev libdb-dev libssl-dev\
 openssl libreadline-dev autoconf libtool git
```

### Download SON executable

TODO Download a latest JOBID from Gitlab

### Building Peerplays SON \(optional\)

These steps can be used if you want to build and deploy the SON

```text
cd $HOME/src
export BOOST_ROOT=$HOME/src/boost_1_67_0
git clone https://github.com/peerplays-network/peerplays.git
cd peerplays
git checkout feature/SONs-base# --> replace with most recent tag
git submodule update --init --recursive
git submodule sync --recursive
cmake -DBOOST_ROOT="$BOOST_ROOT" -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)

make install # this can install the executable files under /usr/local
```

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

