# Installation script overview

This is a quick introduction on how to use the installation script\(run.sh\) to install, maintain and monitor Peerplays Blockchain.

## 1.1 Installation modes

The script supports three modes:

1. witness node as a service on Ubuntu Server
2. witness node as a docker container
3. SON as docker container

### 1.1.1 Witness node as a service on Ubuntu Server

This mode involves building BOOST and Peerplays binaries from source code and therefore it is time consuming. To install follow the following steps

```text
wget https://gitlab.com/PBSA/PeerplaysIO/tools-libs/peerplays-docker/-/raw/feature/install_fixes/run.sh
chmod +x run.sh
./run.sh witness_install

Note: Branch names to be used:
mainnet: master
testnet: beatrice
```

### 1.1.2 Witness node as a docker container

This mode installs the witness node as docker container which can be run on any x86 platform. To install follow the following steps

```text
wget https://gitlab.com/PBSA/PeerplaysIO/tools-libs/peerplays-docker/-/raw/feature/install_fixes/run.sh
chmod +x run.sh
./run.sh witness_docker_install

Note: Tag name to be used:
Latest: latest
Other available tags: 1.5.1, Beatrice
```

### 1.1.3 SON as a docker container

This mode installs the SON as docker container which can be run on any x86 platform. To install follow the following steps

```text
wget https://gitlab.com/PBSA/PeerplaysIO/tools-libs/peerplays-docker/-/raw/feature/install_fixes/run.sh
chmod +x run.sh
./run.sh son_docker_install

Note: Branch names to be used:
Available tags: son-dev
```

## 1.2 Common commands

### 1.2.1 Viewing Peerplays blockchain logs

```text
./run.sh logs
```

### 1.2.2 Replaying Peerplays blockchain logs

You can replay the Peerplays blockchain when witness node is installed as a service, docker container OR SON docker container.

```text
./run.sh replay
```

### 1.2.3 Uninstall Peerplays blockchain

You can uninstall Peerplays blockchain when witness node is installed as a service, docker container OR SON docker container.

```text
./run.sh uninstall
```

## 1.3 Docker container commands

### 1.3.1 Start the witness/SON docker container

```text
./run.sh start
```

### 1.3.2 Stop the witness/SON docker container

```text
./run.sh stop
```

### 1.3.3 Kill the witness/SON docker container

```text
./run.sh kill
```

### 1.3.4 Restart the witness/SON docker container

```text
./run.sh restart
```

### 1.3.5 View status of witness/SON docker container

```text
./run.sh status
```

