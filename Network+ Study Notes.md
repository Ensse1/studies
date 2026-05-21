OSI Model Open systems interconnection model

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
This layer opens maintains and closes the connection between hosts like a telephone call. It handles the connection.

The  presentation layer
This layer has SSL/TLS protocols.

The application layer
This layer is what we see with our eyes. for example the website or the app. We can also interact with it.