# Extending Sweeps

INTRODUCTION

The industry demands few new features to be added to our sweeps/5050 implementation. We will still continue to use the same RNG and draw mechanism to achieve the goals. The following are the list of new features to be added:

1. Variable Ticket Pricing
2. Ticket Bundling
3. Multiple Benefactors
4. Progressive Tickets
5. Represent Gross Gaming revenue on the chain

### VARIABLE TICKET PRICING

Right now Peerplays sweeps supports only a fixed price per draw. This limits the ability to create bundles and special offers. The clients generally use the variable pricing to create grouping of tickets and the groups are priced lower than individual tickets.

We should also support the scenario where all tickets sold for a draw can have different prices. Ie no two tickets should have the same price. This will give the seller the ultimate flexibility to sell tickets at price \(perhaps keeping a lower price point\)

### BUNDLES

Create Sets of tickets and normally sell ticket sets with higher number of items at a lower cost. We can think of all tickets with the same price and also use variable pricing. However the bundles will be used for giving multiple tickets and thus higher chance of winnign the prize at a lower total cost to the buyer.

### MULTIPLE BENEFECTATORS

We are already supporting multiple benefactors getting a share of the prize money. We need to test and ensure that this is working effectively.

* When someone is buying a ticket, he/she shall be able to choose from a list of beneficiaries
* If there is no beneficiary choosen one of them should be auto-selected. \(It will be better to handle this at the dApp side\)
* Any percentage of the sales can be allotted to a beneficiary

### PROGRESSIVE TICKETS

Progressive tickets resulting in a jackpot is a grouping of multiple draws into a single group. This group will have individual tickets and bundles belonging to multiple draws combined into another draw.

### HANDLING GROSS PRICING

* Create a new smart contract to calculate the 2% of gross gaming revenues for distribution to the token holders \(eg. 2% of 41% of Gross Gaming Revenue\)

