### challenges of cluster computing
1. Node failure
	- for 1M nodes, there might me 1000 failures per day
	- if during computation one nodes fail, we have to do the computation again
1. network bottleneck
	- to move around 100 TBs of data in 1GBps bandwidth it'll take one day
2. hard to write programme
	- difficult for event the experienced programmers

### Map-reduce adresses this problems
1. Node failure
	- stores data redundantly
	- - keeps replicas of chunks in different racks
	- Chunk server and Master Node (aks Name Node in HDFS)
1. network bottleneck
	- moves computation close to data 
	
1. hard to write programme
	- simple programming model, map-reduce takes care of rest.

Client library for file access
- talks to master to find chunk server
- once connection is established it can directly talk to chunk server in later stages without the need of master , 
- data access happens in peer to peer fashion