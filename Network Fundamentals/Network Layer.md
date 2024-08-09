Responsible for routing data packets between different networks.

Manages IP addresses, defines routing, and determines the best path for packets to travel through intermediary systems to the end system.

Transforms segments or datagrams (from the transport layer) into packets, adding specific headers and fragmenting them when necessary. Reassembles packets at the destination.

Adds headers containing:

- Source and destination IP addresses
- Control and fragmentation information
- Time to Live (TTL) to limit the number of hops a packet can make

Some devices operating at this layer:

- **Routers**: Route data packets between different networks using IP addresses and routing tables to determine the best path. They decide the next hop for the packet based on the routing table.
- **Firewalls (network level)**: Filter packets based on IP addresses and protocols, controlling incoming and outgoing traffic to protect the network.
- **Gateways**: Include routers and firewalls, acting as interface points between different networks and protocols, translating data between distinct networks and ensuring interoperability.

Key Protocols:

- **IP (Internet Protocol)**: The main protocol that defines the structure of packets and addressing for data delivery.
- **ICMP (Internet Control Message Protocol)**: Used for control messages and errors, such as the "ping" command to check connectivity.
- **IGMP (Internet Group Management Protocol)**: Manages multicast group members, allowing routers to know which devices want to receive multicast transmissions.