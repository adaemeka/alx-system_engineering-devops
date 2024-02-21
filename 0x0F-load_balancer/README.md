Load balancer will distribute the work-load of your system to multiple individual systems,
or group of systems to to reduce the amount of load on an individual system,
which in turn increases the reliability, efficiency and availability of your enterprise application or website.

The following are the advantages of load balancing your application:

Reduced the work-load on an individual server.
Large amount of work done in same time due to concurrency.
Increased performance of your application because of faster response.
No single point of failure. In a load balanced environment,
if a server crashes the application is still up and served by the other servers in the cluster.
When appropriate load balancing algorithm is used, it brings optimal and efficient utilization of the resources,
as it eliminates the scenario of some server’s resources are getting used than others.
Scalability: We can increase or decrease the number of servers on the fly without bringing down the application
Load balancing increases the reliability of your enterprise application
Increased security as the physical servers and IPs are abstract in certain cases.

On a high level, there are two types of load balancers, which implements different types of scheduling algorithms and routing mechanisms.

Software load balancer
Hardware load balancer

I. Software Load Balancers
Software load balancers generally implements a combination of one or more scheduling algorithms.

The following are the three different basic algorithms used by load balancers.
Most modern load balancers use combination of these algorithms to reach high performance
and to set a trade off between various parameters.

1. Weighted Scheduling Algorithm
Work is assigned to the server according to the weight assigned to the server.
For different types of the server in the group different weights are assigned thus the load gets distributed.

2. Round Robin Scheduling
Requests are served by the server sequentially one after another.
After sending the request to the last server, it starts from the first server again.

3. Least Connection First Scheduling
Requests are served first to the server which is currently handling least number of persistent connections.

Software Load Balancer Examples

The following are few examples of software load balancers:

HAProxy – A TCP load balancer.
NGINX – A http load balancer with SSL termination support. (install Nginx on Linux)
mod_athena – Apache based http load balancer.
Varnish – A reverse proxy based load balancer.
Balance – Open source TCP load balancer.
LVS – Linux virtual server offering layer 4 load balancing

II. Hardware Load Balancers
Load balancing hardwares are often referred as specialized routers or switches
which are deployed in between the servers and the client.
It can also be a dedicated system in between the the client and the server to balance the load.

The hardware load balancers are implemented on Layer4 (Transport layer) and
Layer7 (Application layer) of OSI model so prominent among these hardwares are L4-L7 routers.

1. Layer4 Hardware Load Balancing
These kind of load balancers work on transport layer of OSI model and make use of TCP, UDP and SCTP transport layer protocol
details to make decision on which server the data is to be sent.

Layer 4 load balancers are mostly the network address translators (NATs)
which shares load to the different servers getting translated to by these loadbalancer.
These routers hide multiple servers behind them and translate every response data packets coming from the server
to be coming from same ipaddress.

Similarly, when there is a request they reverse translate the request using the mapping table
and distributes it among the multiple servers.

2. Layer7 Hardware Load Balancing
This type of load balancers makes the decision according to the actual content of the message
(URLs, cookies, scripts) since HTTP exists on the layer7.
These layer7 hardware actually form a ADN (Application delivery network)
and they pass-on request to the servers as per the type of the content.

For example, the request for image will go to an image server,
request for PHP scripts may to another server, HTML, js
and css like static content may go to another one and request to any media content may go to yet another server.

So, here a load balancing effect is achieved by distributing load according to the type to content requested.
