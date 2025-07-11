# . Secured and monitored web infrastructure
![Distributed Web Stack](https://i.imgur.com/omoNaEG.png) 
 # Main Components
  ### Firewalls:
Added to filter incoming and outgoing traffic. Firewalls block unauthorized connections and help protect servers from attacks.
 ### SSL Certificate:
Added so the website serves traffic over HTTPS. This encrypts data between the user’s browser and the server, keeping it private.
 ### Monitoring Clients :
Added to collect data from each server. The monitoring tool (like Sumologic or other) tracks server health, performance, and logs.
 ### firewalls :
Firewalls act as a security barrier. They allow only safe, allowed connections and block harmful or unwanted traffic.
 ### Why is traffic served over HTTPS
HTTPS encrypts the connection so data can’t be read or changed by attackers during transfer. This protects user information like passwords and personal data.
 ###  What monitoring is used for
Monitoring checks if servers and services are working correctly. It shows problems early like high CPU usage, errors, or downtime , so you can fix them fast.
### How the monitoring tool collects data
A monitoring client (agent) runs on each server. It collects metrics (CPU, memory, logs) and sends this data securely to a monitoring service (like Sumologic, Datadog, or NewRelic).
### How to monitor web server QPS
To monitor Queries Per Second (QPS) on the web server, configure the monitoring tool to track web server logs or metrics. This shows how many HTTP requests the server handles each second.
# Issues 
   ### Terminating SSL at the load balancer:
If SSL ends at the load balancer, traffic between the load balancer and backend servers is unencrypted inside the network .
   ### Only one MySQL server accepts writes :
Having only one Primary (Master) database means if it fails, you cannot write new data until it is fixed or a new Primary is promoted. This creates a SPOF for writes.
   ###  Same components on all servers :
Having every server run web server with app server with  database can waste resources. It makes scaling harder and managing databases more complicated. It’s better to split roles so each server does one job well.
