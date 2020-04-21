# Faucet

### Add validation of all three public keys

Test Machine Client

ssh qa@96.46.49.25

### Important Note:

faucet machine, two, rq approach, removed ip repeate call check line, model.Active, re-insert in production

The config file and code at ubuntu@35.183.10.250 are edited for load test. Set them back.

config.yaml: time diff between call from same ip set to 0, to be set to 1

app/views.py, line 40,41, \#prevent massive account regisration is commented out for testing. Enable it soon.



## Asynchronous Speedup Solution: 

### Solution

The major operations in the faucet signup are

1. Validation of usernames,
2. Validation of keys
3. Make sure there is no username duplication.
4. Create account
5. Initialise funds in the account if required.
6. Email if balance is below the threshold for the registrar

### Problem

It takes 1 second to create an account on dickchain and 5 seconds for an account on beatrice.

Expects a quick response from the faucet.

### Root cause

All block chain interactions take time.

### Proposed Approach

Keep the peerplays connection initialized. Do not intend to create upon receiving a call from the client.

When a request for user creation is received, 

1. Validate incoming request parameters.
2. Check if user exists on the chain.
3. Validate public keys \(Note done\)
4. If all okay, move the actual account creation to an worker queue.
5. Return a positive confirmation to the client.

### Impact Discussion

Issue 1: Assume the actual account creation takes 10 seconds. What happens if two repeat request to create same user name is received. 

Solutions:

1. How about if there is time restriction of 10 seconds between two signup calls from same IP
2. How about having a cache of all the user ids registered on the chain and user ids from new  requests and do the check for existing user id with the cache. This approach completely eliminates user id duplication. In addition this approach speeds up account creation further as one more blockchain interaction is reduced.

Issue 2: What happens to the peerplays connection which is initialized in the starting of the faucet server, in case of a network failure for say, 5 minutes.



### Test with 20K simultaneous users

![](../../.gitbook/assets/image%20%2815%29.png)

![](../../.gitbook/assets/image%20%288%29.png)

![](../../.gitbook/assets/image%20%2839%29.png)

With no load, no account creation and no validation, 12 K out of 20 K simultaneous signups are processed.  
  
Possible issues are   
1. Upload bandwidth bottleneck at 4 Mbps at the faucet server 2.

2. Client machine process and bandwidth limit.





### Grafana Metrics

[http://localhost:3001/d/fsLXrY2Wz/dick?orgId=1](http://localhost:3001/d/fsLXrY2Wz/dick?orgId=1)   Dick chain

[http://localhost:3001/d/rYdddlPWk/dick-faucet?orgId=1](http://localhost:3001/d/rYdddlPWk/dick-faucet?orgId=1) Dick faucet

Monitroning servers with Grafana, look at the following link.

{% embed url="https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/347439128/Monitoring+Servers+with+Grafana" %}

### Streamers Edge, AWS metrics

[https://us-east-1.signin.aws.amazon.com/oauth?response\_type=code&client\_id=arn%3Aaws%3Aiam%3A%3A015428540659%3Auser%2Fcloudwatch&redirect\_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fcloudwatch%2F%3F%26isauthcode%3Dtrue&forceMobileLayout=0&forceMobileApp=0](https://us-east-1.signin.aws.amazon.com/oauth?response_type=code&client_id=arn%3Aaws%3Aiam%3A%3A015428540659%3Auser%2Fcloudwatch&redirect_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fcloudwatch%2F%3F%26isauthcode%3Dtrue&forceMobileLayout=0&forceMobileApp=0)





### Performance

![10 parallel processes, 600 calls, 0.66 seconds per account creation on an average.](../../.gitbook/assets/image%20%2832%29.png)

It took me 960 seconds to create 800 accounts with 80 parallel calls.



### 

Debug python3 manage.py runserver -h 0.0.0.0 -p 5000

### Create account 

[https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/82935851/HowTo+Cli+Wallet+Account+Creation+with+Brain+Key](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/82935851/HowTo+Cli+Wallet+Account+Creation+with+Brain+Key)[11:26](https://peerplays-official.slack.com/archives/DSCF8004X/p1586282179000500)

### On Keys

[https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/201228402/Using+password+generated+in+GUI+wallet+in+cli+wallet](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/201228402/Using+password+generated+in+GUI+wallet+in+cli+wallet)





### For Testing

**D-Chain Blockchain: ubuntu@35.182.93.168**

**D-Chain Faucet: ubuntu@35.183.10.250**

New IP 35.183.11.136

Two core faucet: ubuntu@35.182.6.94  
**In env, python3** [**manage.py**](http://manage.py/) **install**

**sudo systemctl restart faucet**  
urlBase = '[https://dick-faucet.peerplays.download](https://dick-faucet.peerplays.download)' 

api = '/api/v1/accounts'



### Confluence notes on testing Faucet by Manu

{% embed url="https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/121143389/Create+bookie+user+account+using+faucet+through+postman" %}



