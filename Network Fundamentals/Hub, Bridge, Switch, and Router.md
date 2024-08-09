Essential devices in the construction and operation of local area networks (LANs).

### Hub
Operates at the Physical Layer.

Simply retransmits electrical signals to all connected devices. It does not process data or addresses. Any message sent by one computer will reach all others, but only the intended recipient will respond. This process can lead to congestion issues.

### Bridge
Operates at the Data Link Layer.

Connects two local networks (as long as they run the same protocols) and forwards frames based on MAC addresses. It processes MAC addresses to make forwarding decisions, isolating traffic between segments, reducing collisions, and improving performance. The bridge maintains a MAC address table to know which devices are on which segments, forwarding frames only to the correct segment, thereby reducing congestion and improving security by limiting the propagation of frames between segments.

### Switch
Designed for Star Topology.

Connects multiple computers within a network. Intelligently forwards data frames using a MAC address table.

- **Layer 2 Switches with VLANs**: Operate at the Data Link Layer to segment and isolate traffic within VLANs. Forward frames based on MAC addresses.
- **Layer 3 Switches with VLANs**: Add routing capabilities at the Network Layer to enable communication between different VLANs. Forward packets based on IP addresses and manage routing tables.

### VLAN
A VLAN is a protocol used to organize multiple devices within a single physical network without needing physical changes to the infrastructure. For example, it can be used to separate different departments within a company.

### Router
Operates at the Network Layer, routing packets between different networks based on IP addresses. It determines the best route for transmitting packets and maintains routing tables to manage data traffic. A router acts as a network gateway.

## Edge Router
A network device that connects an organization's internal network to the Internet or other external networks. It acts as the entry and exit point for traffic to the internal network, managing communication between different networks and ensuring secure and efficient data traffic.