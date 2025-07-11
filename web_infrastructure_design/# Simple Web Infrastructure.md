# Simple Web Infrastructure
![Simple Web Stack](https://i.imgur.com/6cYPaK8.png)
## Main Components
### Server  
A computer that stores and runs the website, responding to user requests
### Domain Name  
An friendly name like www.foobar.com that points to the server’s IP address via DNS
### DNS Record  
The www part is typically linked with an a record which maps the name to the server’s IP
### Web Server  
Handles browser requests and serves web pages, images, and other files
### Application Server  
Processes user actions communicates with the database
### Database  
Stores the website’s data
### Client Communication  
The browser and server communicate using the TCP/IP protocol over the internet
---
## Limitations
### SPOF 
If one component fails the whole website goes down
### Downtime  
Any updates on code or restarts make the site temporarily unavailable
### Scalability 
One server can't handle heavy traffic which may cause slowdowns or crashes
---