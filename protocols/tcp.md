# TCP

TCP (Transmission Control Protocol) is a connection-oriented protocol that ensures reliable data transmission between devices over a network. It establishes a connection, manages data flow, checks for errors, and guarantees that packets arrive in the correct order

## TCP Implementation: The Role of the  OS

Most operating systems include a **TCP stack** within the kernel. This means:

**Application Layer Interaction**

* **System Calls**: Applications use calls like send() or write() to pass data to the kernel.
* **Under the Hood**: The OS kernels TCP layer takes care of packaging the data into segments and ensuring reliable transfer.

## "Virtual Connection"

Although theres no dedicated physical circuit, TCP maintains its **state** at each endpoint (e.g., sequence numbers, acknowledgements, window sizes), creating the illusion of a dedicated link. This stateful setup is established via the **three-way handshake**:

1. **SYN** — The client sends a synchronization request to start a connection.
2. **SYN+ACK** — The server acknowledges and sends its own SYN to the client.
3. **ACK** — The client acknowledges the server’s SYN, and the connection is established.

```cpp
  0                          15                         31  (bit positions)
  -------------------------------------------------------
 |        Source Port        |     Destination Port      |  (16 bits each)
  -------------------------------------------------------
 |                   Sequence Number                     |  (32 bits)
  -------------------------------------------------------
 |               Acknowledgment Number                   |  (32 bits)
  -------------------------------------------------------
 | Data |     |U|A|P|R|S|F|            Window            |  (16 bits)
 |Offset|Resvd|R|C|S|S|Y|I|   
  ------------------------------------------------------- 
 |           Checksum         |       Urgent Pointer     |  (16 bits each)
  -------------------------------------------------------
 |        Options (if any)                |   Padding    |
  -------------------------------------------------------
 |                       Data (Payload)                  |
  -------------------------------------------------------
```

# Connection-oriented, reliable, and bitstream-oriented

1. TCP is connection-oriented. Unlike UDP which sends data from one server to multiple servers, TCP establishes a connection between two specific servers.
2. TCP is reliable. TCP guarantees the delivery of the segments, no matter what the network condition is.
3. TCP is bitstream-oriented. With TCP, application layer data is segmented. The transport layer remains oblivious to the boundary of a message. In addition, the segments must be processed sequentially, and duplicated segments are discarded.

# Establishing a TCP connection: The 3-way handshake

![](https://substackcdn.com/image/fetch/$s_!e2fg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F781159a5-f60e-4c94-b815-c8abd8d73b12_1600x1442.png)

# Closing a TCP connection: The 4-way handshake

![](https://substackcdn.com/image/fetch/$s_!mOdv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e386fb3-7fc6-477a-aa50-c314a462a349_1600x1591.png)
