# DNS Tools: DIG

------

> (2026-02-27) 
> Nicolas Antoniello (@65007)

------



## Lab Topology (Group X) 



![lab-topo-resolver-authoritative](../DNS-Resolver_Lab_script-pics/grpX_network_topology.png)



```
  DEVICE NAME        IPv4 ADDRESS              IPv6 ADDRESS
+--------------+-----------------------+-----------------------------+
| grpX-cli     | 100.100.X.2 (eth0)    | fd8c:c9b5:X::2 (eth0)       |
+--------------+-----------------------+-----------------------------+
| grpX-resolv1 | 100.100.X.67 (eth0)   | fd8c:c9b5:X:64::67 (eth0)   |
+--------------+-----------------------+-----------------------------+
| grpX-resolv2 | 100.100.X.68 (eth0)   | fd8c:c9b5:X:64::68 (eth0)   |
+--------------+-----------------------+-----------------------------+
| grpX-rtr     | 100.64.1.X (eth0)     | fd8c:c9b5:X::1 (eth1)       |
|              | 100.100.X.65 (eth2)   | fd8c:c9b5:X:64::1 (eth2)    |
|              | 100.100.X.193 (eth4)  | fd8c:c9b5:X:192::1 (eth4)   |
|              | 100.100.X.129 (eth3)  | fd8c:c9b5:X:128::1 (eth3)   |
|              | 100.100.X.1 (eth1)    | fd8c:c9b5:0:1::X (eth0)     |
+--------------+-----------------------+-----------------------------+
```

During this practice we are going to access the following equipment:

* **grpX-cli** : client
* As a pre-requisite we will need **grpX-resolv1** and **grpX-resolv2** resolvers already configured and running.



# DNS queries and debugging using DIG tool

We use the container "*cli" (recursive server) [**grpX-cli**].

