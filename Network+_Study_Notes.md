**OSI Model Open systems interconnection model**

What is OSI?
Osi is a reference that we use to understand and explain networking concepts. We use it to make our and other workers life easier. It shows us how a connection occurs, what happens in a connection, what are the steps. It also helps us when we are trying to fix something broken.

These are the layers..
7- Application
6- Presentation
5- Session
4- Transport
3- Network
2- Data link
1- Physical

The Physical Layer
The bits live here, it includes physical and raw connection.
Hub is in this layer too because it is dumb, technically it is a dumb switch.
Ethernet, cat cables,wifi,hub.

The data link layer
In this layer we use the mac addresses on our devices and hosts. The NIC (Network interface card) in our devices have a mac address, the first 3 octets show the manufacturer and the last 3 octets are random. fyi. we can change our mac addresses. Generally we use switches in this layer because switches use mac addresses to identify hosts and bring packets to them.

The network layer
The protocol we use in this layer is the internet protocol (ip). This layer includes routers. Routers use ip's to identify hosts on a local or public internet. Everyone has a unique ip address in a LAN and every modem has a unique public ip provided by their isp's. We can say that this isnt physical anymore.

The transport layer
In this layer we use ports. Also we use the TCP and UDP protocols for sending and receiving packets. TCP is a slower but reliable way to send and receive packets. UDP is way faster but not too reliable, means that the packet may be dropped or the integrity of it may be broken. This also helps us identify the host in a better way.

The session layer
This layer opens ,maintains and closes the connection between hosts like a telephone call. It handles the connection.

The presentation layer
This layer has SSL/TLS protocols. It encrypts and decrypts data. This layer works with the application layer and this is the layer that happens prior to what we see on our screen.

The application layer
This layer is what we see with our eyes on the screen. This layer has protocols like http, ftp, smtp, pop3.

NETWORKING DEVICES

When we enter a database station we see a lot of racks with devices on them, these are network devices. Network devices are used for a lot of things. We can install new technology devices in our system but also can install the same devices too. But it takes some time to remove the devices.

Switch
This device works with mac addresses, it is in the layer 2 of the osi model. It allows us to send packets in our LAN. There is also something we call L3 switch. Basically it is a switch with a router built into it. It is in both layer 2 and the layer 3 in the osi model. It has a power over ethernet module. Also it works with the hardware built into it called asic (Application specific integrated circuit)

Router
This device works with ip addresses and it is in layer 3 of the osi model. Routers allow us to send data to different ip subnets. It could be an ip subnet next to our lan in the datacenter or it could be an ip subnet in the other side of the world.

Firewall
Firewalls are used to control network traffic. Traditional firewalls use the tcp and udp ports to control incoming and outgoing traffic. Traditional firewalls only look at the headers of the packets. New generation firewalls, the ones used in the modern day use the application layer protocols while controlling what is going in and out. traditional firewalls use up to layer 3-4 on the osi model while ngfw's use the layers up to 7. They also use ip's to make decisions on which packets to filter. They stand between the lan and wan, ingress and egress. ngfw's also have a vpn built in to encrypt data and connect to other firewalls across the internet. They also have ids/ips built in too alongside the nat protocol which transforms our private ip's of our devices to public ip which the isp gives us. Public ip's are unique.

Ids/Ips
Ids and ips is used to detect intrusions and malwares sent to our systems. Ids is a passive system, it creates an alert when an intrusion or malware is detected but it doesnt prevent it from entering the system. Ips on the other hand is an inline system. Every packet must go through the ips system. It stands in the network and stops the malware or the threat actor before stepping in our network. They do this by signatures. These signatures have attack patterns and known exploits in them. If an ips or ids system matches those signatures to incoming packets they do what they have to do.

Methods
Signature based: matches traffic agains a DB of knowsn attack patterns
Anomaly based: Looks how normal traffic looks like and alerts when something weird happens
Policy based:  Alerts when violates a defined rule

Internet => Firewall => IPS >= Network
                    IDS

Load balancer
Load balancers are used to prevent server outages by distributing the users into different servers called server pool or server farm. When one of those servers go out of service due to some issue, load balancers can detect the server that is down, take that out of the list and continue to balance the usage of servers. Load balancers also use algorithms to determine which server gets the next request. Load balancers also include Tcp, ssl offloading, caching content switching and prioritizing.

Proxies
When a host want to connect to a server and sen packets to it, the packet is first sent to the proxy server, then the proxy server sends that packet to the server on their(proxies) behalf. Also proxy servers check for malicious code or exploits in incoming packets so it kinda acts like a firewall too. We can also use it to set username and passwords to connect to the internet with the access control list. Forward proxies sit between the hosts and the internet, reverse proxies sit between the internet and internal servers. We can give load balancers as an example to a reverse proxy. There are two types of proxies transparent and  non transparent, when we are using a transparent proxy the user doesnt really know that they are using a proxy, they think that they are connecting to the internet directly but thats not the case, usually our isp provider implements this in our network. On the other hand, the user knows that they are using a proxy when there is a non-transparent proxy. Also a proxy terminates our connection and opens a new seperate connection to the  destination. 

NAS Network attached storage
It is a storage technique used to store documents, files.. in datacenters. The downside of this is when we want to change something in a file we need to copy the whole while to our system. That takes up a lot of space and takes a lot of time when the file is huge.

SAN Storage area network
It is used to store blocks. the main difference from nas is we have block-level access to files. What this means is that we dont need to copy the whole file to change something in it, we can copy the block of where we want to make a change. This comes in very handy when we are dealing with big files.
Also on both nas and san, since we need very high bandwith for them, we might want to use an isolated network and high speed network topologies.
We can think of san as a virtually attached hard drive and nas as a filesystem 

Access point
Access points are used in enterprise organizations or big buildings to connect devices to the wireless network across everywhere in the building. It only has a single purpose, to provide wireless connection. It is not a wireless router like the ones in our houses which is a router and an access point at the same time. AP is in the layer 2 of osi.  The access point is a bridge between the wired and wireless network. It extends the wired network to wireless network. 

NETWORKING FUNCTIONS

CDN (Content Delivery Network)
When we are using the internet and go into a website. We usually arent going to the website server directly. We are going into the server cached in a cdn. But there is an exception for this which is if the server is not cached in the cdn we need to go back to the origin server and after we do that the cdn caches that website and when we want to access that website again we can see that there is a big difference in latency. For example im in Turkey and want to access to a site in Usa, Instead of going all the way to that server im going to the cdn which is closer to me and get a faster connection and delay.

VPN (Virtual Private Network)
Vpn's create a virtual private network tunnel between us and the destination. In this tunnel the data we sent is encrypted which makes our data content unreadable to threat actors, isp's etc. But still our isp can see that we are connected to a vpn and how much data we are sending. At the end of this tunnel our data is decrypted and got to the destination successfully. The hardware that do the encryption and decryption is contentrator or head-end. When we visit a website by using a vpn, the website sees the ip of the vpn server we are using instead of our public ip address which makes us more private. We also use vpn's to connect to enterprise networks. We may use a hardware to use a vpn if there are a lot of users who are going to use the vpn, but if we are in a small business or just using vpn in our home wifi we may use the manufacturers software to do so. Operating systems also come with default built in vpn clients.

QoS (Quality of Service)
QoS allows us to set the bandwith usage and queue priority on services. The higher prority services need more bandwith usage, so we give those services more priority. Lower priority services get lower bandwith usage and in return work slower. We can configure these on our routers, switches and firewalls. For example there's a udp video player and a tcp mailing service we are using. In order for our video player to function efficiently with minimum packet dropping we need to give it more priority in terms of bandwith usage. Our tcp service can work with lower levels of resources because if a packet gets dropped or fails to go to its destination the tcp service can still reacquire that missing packet without needing to start the connection from the beginning .

TTL (Time To Live)
As we may know computers are super efficient at automating tasks on a level which humans cant really do on their own. But there is a side effect to this which the the system might get into a loop and repeat the same task over and over again. To prevent this we have built a function called ttl. What this does is it drops the packet or stops the process when the process iterate a certain number of times, we may also select a duration time. It may also be used to clear a cache after a desired amount of time passes.
In ip we use ttl to drop the packet after a certain amount of hops. If the maximum amount of hops are reached the packet is dropped. default ttl on linux is 64 and 128 on windows. ttl gets decreased by the router on each hop that happens.
In dns ttl functions different. It is measured by the duration of the ip address that stays in our local cache. When we go into a website using the dns protocol, dns looks up the ip address of the domain name and allows us to access that website without having to remember the ip adress of that website. So after accessing that website the dns record of it is stored in our cache which allows us to access to that website faster in the until the duration that is set by the ttl is over. 