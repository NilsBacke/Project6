## Approach
The approach we took for this project was to follow the section that generally laid out steps.
Following these steps provided a logical flow to follow during development. After following this
we tackled individual bugs we found during testing.
## Testing
To test our program we used the provided .json specs to run through all of the possible 
conditions our store would be facing. Different tests yielded different results and exposed
holes in our logic until we were able to solve everything and fully implement the required
Raft principles.
## Obstacles
We met a few obstacles, the first being understanding what went into the transaction log to ensure that everything was correct across replicas. Building off of this, the largest obstacle we had was facing a certain series of actions where a partition happens followed by an election where the leader was a member of the minority partition and its state was behind. This ended up being a simple issue where the wrong log was being sent to the replicas to update them.