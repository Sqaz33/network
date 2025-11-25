# DHCP (Dynamic Host Configuration Protocol)

L7 ptorocol. The **Dynamic Host Configuration Protocol** (**DHCP**) is a [network management protocol](https://en.wikipedia.org/wiki/Network_protocol "Network protocol") used on [Internet Protocol](https://en.wikipedia.org/wiki/Internet_Protocol "Internet Protocol") (IP) networks for automatically assigning [IP addresses](https://en.wikipedia.org/wiki/IP_address "IP address") and other communication parameters to devices connected to the network using a [client–server](https://en.wikipedia.org/wiki/Client%E2%80%93server) architecture.

## Overview

DHCP operates based on the [client–server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model "Client–server model"). When a computer or other device connects to a network, the DHCP client software sends a DHCP [broadcast](https://en.wikipedia.org/wiki/Broadcasting_(networking)) "Broadcasting (networking)") query requesting the necessary information. Any DHCP server on the network may service the request.

### Dynamic allocation

A [network administrator](https://en.wikipedia.org/wiki/Network_administrator "Network administrator") reserves a range of IP addresses for DHCP, and each DHCP client on the [LAN](https://en.wikipedia.org/wiki/LAN "LAN") is configured to request an IP address from the DHCP [server](https://en.wikipedia.org/wiki/Server_(computing)) "Server (computing)") during network initialization. The request-and-grant process uses a lease concept with a controllable time period, allowing the DHCP server to reclaim and then reallocate IP addresses that are not renewed.

### Automatic allocation

The DHCP server permanently assigns an IP address to a requesting client from a range defined by an administrator. This is like dynamic allocation, but the DHCP server keeps a table of past IP address assignments, so that it can preferentially assign to a client the same IP address that the client previously had.

### Manual allocation

This method is also variously called *static DHCP allocation*, *fixed address allocation*, *reservation*, and *MAC/IP address binding*. An administrator maps a unique identifier (a *client id* or [MAC address](https://en.wikipedia.org/wiki/MAC_address "MAC address")) for each client to an IP address, which is offered to the requesting client. DHCP servers may be configured to fall back to other methods if this fails.

## Operation

The DHCP employs a [connectionless](https://en.wikipedia.org/wiki/Connectionless "Connectionless") service model, using the [User Datagram Protocol](https://en.wikipedia.org/wiki/User_Datagram_Protocol "User Datagram Protocol") (UDP). It is implemented with two UDP port numbers for its operations which are the same as for the bootstrap protocol ([BOOTP](https://en.wikipedia.org/wiki/BOOTP "BOOTP")). The server listens on UDP port number 67, and the client listens on UDP port number 68.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/DHCP_session.svg/330px-DHCP_session.svg.png)
