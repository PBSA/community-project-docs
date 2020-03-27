---
description: This document is under development. You are welcome to share your thoughts.
---

# Development Notes BOS

## Issues

1. JobTimeoutException when trying to approve proposals: Solved
   1. The issue is solved and details are given below under the heading BOS-AUTO\#12
   2. This issue is already open in Github, issue \#12, bos-auto and BOS-208 in JIRA
   3. The issue can be solved by making sure that no proposals are pending approval by the witness when the witness starts proposing or approving a new incident.
2. BOS-AUTO takes about 12 minutes to propose soccer events: Solved
   1. Soccer has 8 betting market groups
   2. And with TEST and BTF coins, it \(soccer\) has 34 betting markets. 
   3. The time taken for betting market increases with each created betting market in a proposal. For example it takes 1 second for creating the first betting market, where as it takes about 30 seconds for creating the 34th betting market.
3. None type object is not iterable, error:
   1. _Details to be reproduced and added._
   2. This is a bos-sync issue.
4. There is a cache error, occurring at times.
5. Through out a proposal creating the CPU usage is 100%. : Discarded

## Root cause exploration

1. The present code doesn't ensure that approval is called after making a proposal. 
2. bookied\_sync/lookup.py, def update\(\) is the method where the time bottleneck is. The reason for time taken is it takes time to look up for items in chain and buffers.
3. bookied\_sync/bettingmarket.py, def propose\_new\(\). This method has a reference to a class variable. Any reference to this variable takes significant time per betting market and time taken per betting market increases as number of betting market increases.
4. bookied\_sync/bettingmarket.py, def find\_id\(\) method has self.parent.get\_id. This in turn calls lookupy, def get\_id\(\) and which inturn sport.py, def find\_id\(\). A recursive call is found at this level and the recursion makes multiple calls to the chain continuously. This is a major location for making the code efficient.

## Possible solutions

1. Ensure that approval is called before and after an event proposal
2. How about increasing timeout to 12 minutes?

## Notes on completed development tasks

1. graphenecommon/blockchainobject.py, line 175, getfromcache error, investiagate:  
   1. The issue is found to be not repeating when all libraries are new version.
2. Running a two core machine looks better.

### BOS-AUTO \#12 and Reducing time taken per proposal

There is a for loop in method createBmgs in bookied/triggers/create.py

Check time taken for each BMG creation and exit createBmg for loop and trigger if time exceeds, say 10 seconds.

Upon exiting createBmgs, set\_incident\_status to "midway"

In scheduler, bookied/scheduler.py, check for "midway" events and add them to rq queue for work.process.

add approval prior and after each work.process and ensure they are called in order with depends\_on argument of rq.

Trigger the flask server with --scheduler option

It works!



