# Distributed Web Infrastructure
![Distributed Web Stack](https://imgur.com/a/fB7dWGN.png)
 ## Main Components
### Load Balancer (HAproxy) :
  Added to split traffic between multiple servers. This helps handle more visitors and prevents a single server from being overloaded.
   
### Two Servers
Added for redundancy. If one server fails, the other keeps the site running
### Load Balancer Algorithm :
The load balancer uses a Round Robin algorithm.
It sends each new request to the next server in order, balancing the load evenly.
 ### Active-Active or Active-Passive :
 The load balancer works in an Active-Active setup.
Both servers handle requests at the same time. If one fails, all traffic goes to the other.

Active-Active = multiple active servers at the same time.
Active-Passive = one server is active, the other is on standby.
### Database Primary-Replica Cluster:
In this setup, there is a Primary (Master) database and a Replica (Slave) database.

Primary: Handles all writes and reads.

Replica:only handles read requests.
### The difference between the Primary node and the Replica node :
The Primary node accepts writes and updates the data.
The Replica node only receives data updates from the Primary and answers read-only requests.
 ###  Issues :
    SPOF: The load balancer is still a Single Point of Failure , if it goes down nobody can access the servers.
    Security: There is no firewall to block unwanted traffic and no HTTPS so traffic is unencrypted.
     No Monitoring: There is no system to check if servers are healthy or overloaded.