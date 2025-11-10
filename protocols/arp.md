# Address Resolution Protocol (ARP)

Is a [communication protocol](https://en.wikipedia.org/wiki/Communication_protocol "Communication protocol") for discovering the [link layer](https://en.wikipedia.org/wiki/Link_layer "Link layer") address, such as a [MAC address](https://en.wikipedia.org/wiki/MAC_address "MAC address"), associated with an [internet layer](https://en.wikipedia.org/wiki/Internet_layer "Internet layer") address, typically an [IPv4 address](https://en.wikipedia.org/wiki/IPv4_address).

# How ARP Works?

![How-Address-Resolution-Protocol-ARP-works---gif-opt-(1)](https://media.geeksforgeeks.org/wp-content/uploads/20240212121108/How-Address-Resolution-Protocol-ARP-works---gif-opt-(1).gif)

1. ****ARP Cache:**** After resolving the MAC address, the ARP sends it to the source where it is stored in a table for future reference. The subsequent communications can use the MAC address from the table.
2. ****ARP Cache Timeout:**** It indicates the time for which the MAC address in the ARP cache can reside.
3. ****ARP request:**** This is nothing but broadcasting a packet over the network to validate whether we came across the destination MAC address or not.
   * The physical address of the sender.
   * The IP address of the sender.
   * The physical address of the receiver is FF:FF:FF:FF:FF: FF or 1’s.
   * The IP address of the receiver
