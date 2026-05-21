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
In this layer we use ports. Also we use the TCP and UDP protocols for sending and receiving packets. TCP is a slower but safer way to send and receive packets. UDP is way faster but not too safe. This also helps us identify the host in a better way.

The  session layer
This layer opens ,maintains and closes the connection between hosts like a telephone call. It handles the connection.

The  presentation layer
This layer has SSL/TLS protocols. In thıs layer the 

The application layer
This layer is what we see with our eyes. for example the website or the app. We can also interact with it.

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


