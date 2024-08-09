## ARP (Address Resolution Protocol)

A protocol used to discover a device's physical (MAC) address from its IP address within a local network. It operates at the Data Link Layer.

Step by step: → When a device needs to send a packet to another device on the same local network, it knows the destination IP address but not the MAC address. The device sends a **broadcast ARP request** to the entire network, asking: "What is the MAC address associated with IP X.X.X.X?"

→ The device that has the requested IP address responds with an **ARP reply**, providing its MAC address. → The device that made the ARP request updates its ARP table with the matching IP and MAC address. This allows it to send packets directly to the destination device using the MAC address.