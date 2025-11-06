![1762415372063](images/theory/1762415372063.png)

# Physical layer (l1)

The physical layer is responsible for the transmission and reception of unstructured raw data between a device, such as a [network interface controller](https://en.wikipedia.org/wiki/Network_interface_controller "Network interface controller"), [Ethernet hub](https://en.wikipedia.org/wiki/Ethernet_hub "Ethernet hub"), or [network switch](https://en.wikipedia.org/wiki/Network_switch "Network switch"), and a physical [transmission medium](https://en.wikipedia.org/wiki/Transmission_medium "Transmission medium"). It converts the digital bits into electrical, radio, or optical signals (analogue signals). Layer specifications define characteristics such as voltage levels, the timing of voltage changes, physical data rates, maximum transmission distances, modulation scheme, channel access method and physical connectors.

# Data link layer (l2)

The data link layer provides [node-to-node data transfer](https://en.wikipedia.org/wiki/Node-to-node_data_transfer "Node-to-node data transfer")—a link between two directly connected nodes. It detects and possibly corrects errors that may occur in the physical layer. It defines the protocol to establish and terminate a connection between two physically connected devices. It also defines the protocol for [flow control](https://en.wikipedia.org/wiki/Flow_control_(data)) between them.

## Medium Access Control (MAC) (l2 sublayer)

Responsible for controlling how devices in a network gain access to a medium and permission to transmit data.

## Logical Link Control (LLC) (l2 sublayer)

Responsible for identifying and encapsulating network layer protocols, and controls error checking and frame synchronization

# Network Layer (l3)

The network layer provides the functional and procedural means of transferring [packets](https://en.wikipedia.org/wiki/Network_packet "Network packet") from one node to another connected in "different networks". A network is a medium to which many nodes can be connected, on which every node has an *address* and which permits nodes connected to it to transfer messages to other nodes connected to it by merely providing the content of a message and the address of the destination node and letting the network find the way to deliver the message to the destination node, possibly [routing](https://en.wikipedia.org/wiki/Routing "Routing") it through intermediate nodes.

# Transpor Layer (l4)

The transport layer provides the functional and procedural means of transferring variable-length data sequences from a source host to a destination host from one application to another across a network while maintaining the quality-of-service functions. Transport protocols may be connection-oriented or connectionless.

# Session Layer (l5)

The session layer creates the setup, controls the connections, and ends the [teardown](https://en.wikipedia.org/wiki/Teardown_(communications)) between two or more computers, which is called a "session". Common functions of the session layer include user logon (establishment) and user logoff (termination) functions. Including this matter, authentication methods are also built into most client software, such as FTP Client and NFS Client for Microsoft Networks. Therefore, the session layer establishes, manages and terminates the connections between the local and remote applications.

# Presentation Layer (l6)

The presentation layer establishes data formatting and data translation into a format specified by the application layer during the encapsulation of outgoing messages while being passed down the [protocol stack](https://en.wikipedia.org/wiki/Protocol_stack "Protocol stack"), and possibly reversed during the deencapsulation of incoming messages when being passed up the protocol stack. For this very reason, outgoing messages during encapsulation are converted into a format specified by the application layer, while the conversion for incoming messages during deencapsulation are reversed.

# Application Layer (l7)

The application layer is the layer of the OSI model that is closest to the end user, which means both the OSI application layer and the user interact directly with a software application that implements a component of communication between the client and server, such as [File Explorer](https://en.wikipedia.org/wiki/File_Explorer "File Explorer") and [Microsoft Word](https://en.wikipedia.org/wiki/Microsoft_Word "Microsoft Word").
