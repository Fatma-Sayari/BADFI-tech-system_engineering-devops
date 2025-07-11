![Scale up  Web Infrastructure ](https://i.imgur.com/zmZOcZp.png) 
 # Main Components
 ##  What’s added 
 ### More Server:
Added to split components into separate machines.
Each server now does one job only (web server, app server, or database).
This makes scaling easier and uses resources better.
###  More Load Balancer (HAproxy):
Added to make a load balancer cluster.
If one load balancer fails, the other takes over.
This removes the single point of failure at the LB level.
### Split Components:
Web Server: Has only the web server (Nginx).

Application Server: Runs only backend code.

Database Server: Runs only MySQL.
