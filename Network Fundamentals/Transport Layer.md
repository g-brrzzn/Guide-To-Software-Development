Responsible for end-to-end communication between devices. This layer is entirely software-based.

It ensures reliable data delivery, flow control, and error correction between end systems.

Transforms application data into segments or datagrams for transmission and ensures they arrive correctly at the destination.

Adds headers containing:

- Source and destination ports
- Sequence and acknowledgment numbers
- Flow control and congestion windows
- Integrity check (checksum)

Key functionalities:

- **Connection establishment and termination**: Creating and closing communication sessions between devices.
- **Flow control**: Ensures that the sender does not overwhelm the receiver with too much data at once.
- **Error correction**: Detects and retransmits lost or corrupted packets.
- **Multiplexing**: Allows multiple application processes to use the network simultaneously, differentiating them through port numbers.

Devices operating at this layer are **End Systems (hosts)**: These include computers, servers, and mobile devices that communicate over the network.

- **TCP (Transmission Control Protocol)**: A connection-oriented protocol that ensures reliable delivery, flow control, and retransmission of lost packets. Suitable for applications requiring high reliability, such as file transfer and web browsing.
- **UDP (User Datagram Protocol)**: A connectionless protocol offering fast delivery, without guarantees of delivery or order. Suitable for applications that can tolerate data loss, such as video streaming and online gaming.