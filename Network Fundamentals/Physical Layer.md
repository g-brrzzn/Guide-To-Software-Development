Responsible for the transmission of raw bits over a physical medium. Hardware-based.

It interfaces the TCP/IP model with various types of networks (e.g., Ethernet).

Finally, it transmits frames over the physical medium (which can range from cables to wireless systems).

Some devices operating at this layer:

- **Hubs**: Simply retransmit electrical signals to all connected devices. They do not process data or addresses. Any message sent by one computer will also reach the others. However, only the destination computer will respond to the message. This process leads to congestion problems.
- **Repeaters**: Repeat and amplify signals to cover greater distances without any additional processing.

## Encapsulation - PDU (**Protocol Data Unit**)

- **Application**: Data
- **Transport**: Segment (TCP) or Datagram (UDP)
- **Network**: Packet
- **Data Link**: Frame
- **Physical**: Bits