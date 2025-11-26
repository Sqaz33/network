# Domain Name System

The **Domain Name System** (**DNS**) is a hierarchical and distributed [name service](https://en.wikipedia.org/wiki/Name_service "Name service") that provides a naming system for [computers](https://en.wikipedia.org/wiki/Computer "Computer"), services, and other resources on the Internet or other [Internet Protocol](https://en.wikipedia.org/wiki/Internet_Protocol "Internet Protocol") (IP) networks.

## Funcion

An often-used analogy to explain the DNS is that it serves as the [phone book](https://en.wikipedia.org/wiki/Telephone_directory "Telephone directory") for the Internet by translating human-friendly computer [hostnames](https://en.wikipedia.org/wiki/Hostname "Hostname") into IP addresses.

An important and [ubiquitous](https://en.wikipedia.org/wiki/Ubiquitous_computing "Ubiquitous computing") function of the DNS is its central role in distributed Internet services such as [cloud services](https://en.wikipedia.org/wiki/Cloud_service "Cloud service") and [content delivery networks](https://en.wikipedia.org/wiki/Content_delivery_network "Content delivery network").^[[3]](https://en.wikipedia.org/wiki/Domain_Name_System#cite_note-3)^ When a user accesses a distributed Internet service using a URL, the domain name of the [URL](https://en.wikipedia.org/wiki/URL "URL") is translated to the IP address of a server that is proximal to the user

## Structure

### Domain name space

The domain name space consists of a [tree data structure](https://en.wikipedia.org/wiki/Tree_(data_structure)) "Tree (data structure)"). Each node or leaf in the tree has a *label* and zero or more *resource records* (RR), which hold information associated with the domain name.

The tree sub-divides into *zones* beginning at the [root zone](https://en.wikipedia.org/wiki/DNS_root_zone "DNS root zone"). A [DNS zone](https://en.wikipedia.org/wiki/DNS_zone "DNS zone") may consist of as many domains and subdomains as the zone manager chooses

![undefined](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Domain_name_space.svg/2560px-Domain_name_space.svg.png)

### Name servers

The Domain Name System is maintained by a [distributed database](https://en.wikipedia.org/wiki/Distributed_database "Distributed database") system, which uses the [client–server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model "Client–server model"). The nodes of this database are the [name servers](https://en.wikipedia.org/wiki/Name_server "Name server"). Each domain has at least one authoritative DNS server that publishes information about that domain and the name servers of any domains subordinate to it. The top of the hierarchy is served by the [root name servers](https://en.wikipedia.org/wiki/Root_name_server "Root name server"), the servers to query when looking up (*resolving*) a [TLD](https://en.wikipedia.org/wiki/Top-level_domain "Top-level domain").

### Authoritaticve name server

An *authoritative* name server is a name server that only gives [answers](https://en.wikipedia.org/wiki/Name_server#Authoritative_answer "Name server") to DNS queries from data that have been configured by an original source, for example, the domain administrator or by dynamic DNS methods, in contrast to answers obtained via a query to another name server that only maintains a cache of data.

An authoritative server indicates its status of supplying definitive answers, deemed *authoritative*, by setting a protocol flag, called the "*Authoritative Answer*" (*AA*) [bit](https://en.wikipedia.org/wiki/Bit "Bit") in its responses

## Operation

Domain name resolvers determine the domain name servers responsible for the domain name in question by a sequence of queries starting with the right-most (top-level) domain label.

![undefined](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Example_of_an_iterative_DNS_resolver.svg/2560px-Example_of_an_iterative_DNS_resolver.svg.png)
