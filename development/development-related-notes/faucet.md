# Faucet

### Important Note:

The config file and code at ubuntu@35.183.10.250 are edited for load test. Set them back.

config.yaml: time diff between call from same ip set to 0, to be set to 1

app/views.py, line 40,41, \#prevent massive account regisration is commented out for testing. Enable it soon.



### Peformance

![10 parallel processes, 600 calls, 0.66 seconds per account creation on an average.](../../.gitbook/assets/image%20%2830%29.png)

It took me 960 seconds to create 800 accounts with 80 parallel calls.



### 

### Python Load Test

### 

### Try on Fred

Issue \#1 faucet

Nginx,

Debug python3 manage.py runserver -h 0.0.0.0 -p 3000

### 

### 

### Create account 

[https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/82935851/HowTo+Cli+Wallet+Account+Creation+with+Brain+Key](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/82935851/HowTo+Cli+Wallet+Account+Creation+with+Brain+Key)[11:26](https://peerplays-official.slack.com/archives/DSCF8004X/p1586282179000500)

### On Keys

[https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/201228402/Using+password+generated+in+GUI+wallet+in+cli+wallet](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/201228402/Using+password+generated+in+GUI+wallet+in+cli+wallet)





For Testing

**D-Chain Blockchain: ubuntu@35.182.93.168**

**D-Chain Faucet: ubuntu@35.183.10.250**  


urlBase = '[https://dick-faucet.peerplays.download](https://dick-faucet.peerplays.download)' 

api = '/api/v1/accounts'



Confluence notes on testing Faucet by Manu

{% embed url="https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/121143389/Create+bookie+user+account+using+faucet+through+postman" %}



