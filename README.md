# The System Design Interview Notes

## May 28th 2021

*CAP Theorem* - Can only have 2 at the same time out of consistency availability and partition tolerance.

* **Consistency** - what you just wrote you read back i.e. you never read stale data
* **Availability** - you always return a value never fail the request
* **Partition Tolerance** - continue to work even if some servers fail some routers fail whatever network failure happens basically

You have to have partition tolerance because there is no way to guarantee all the servers work 100% of the time. So if your system fails if network failures happen then 
that system is not usable at all.

If you choose CP then you might get some timeouts, in general reads might be slower. Good for atomic read write type of operations.

AP is good when you are okay with reads being stale i.e eventual consistency. 

3 types of consistency - weak (dont care if miss some writes forever), eventual, strong.

2 ways to support high availability - failover (have back up server ready to take up load if one goes down or have two servers who divide traffic between themselves) or replication (mainly makes sense for data replication, store the same data in several places so that in case one goes down you can still serve from other)






