# Faucet

### Important Note:

faucet machine, two, rq approach, removed ip repeate call check line, model.Active, re-insert in production

The config file and code at ubuntu@35.183.10.250 are edited for load test. Set them back.

config.yaml: time diff between call from same ip set to 0, to be set to 1

app/views.py, line 40,41, \#prevent massive account regisration is commented out for testing. Enable it soon.



### Grafana Metrics

[http://localhost:3001/d/fsLXrY2Wz/dick?orgId=1](http://localhost:3001/d/fsLXrY2Wz/dick?orgId=1)   Dick chain

[http://localhost:3001/d/rYdddlPWk/dick-faucet?orgId=1](http://localhost:3001/d/rYdddlPWk/dick-faucet?orgId=1) Dick faucet

Monitroning servers with Grafana, look at the following link.

{% embed url="https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/347439128/Monitoring+Servers+with+Grafana" %}

Streamers Edge, AWS metrics

[https://us-east-1.signin.aws.amazon.com/oauth?response\_type=code&client\_id=arn%3Aaws%3Aiam%3A%3A015428540659%3Auser%2Fcloudwatch&redirect\_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fcloudwatch%2F%3F%26isauthcode%3Dtrue&forceMobileLayout=0&forceMobileApp=0](https://us-east-1.signin.aws.amazon.com/oauth?response_type=code&client_id=arn%3Aaws%3Aiam%3A%3A015428540659%3Auser%2Fcloudwatch&redirect_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fcloudwatch%2F%3F%26isauthcode%3Dtrue&forceMobileLayout=0&forceMobileApp=0)





### Performance

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

Two core faucet: ubuntu@35.182.6.94  
**In env, python3** [**manage.py**](http://manage.py/) **install**

**sudo systemctl restart faucet**  


urlBase = '[https://dick-faucet.peerplays.download](https://dick-faucet.peerplays.download)' 

api = '/api/v1/accounts'



Confluence notes on testing Faucet by Manu

{% embed url="https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/121143389/Create+bookie+user+account+using+faucet+through+postman" %}



