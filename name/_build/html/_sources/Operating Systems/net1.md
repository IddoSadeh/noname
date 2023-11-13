# Common Network Commands

In this section we will talk about basic networking commands.

The new commands we will introduce are:


| Command | Use | Notes |
|---------|-----|-------|
|ifconfig|shows us some information about our connection|-----|
|iwconfig|similar to ipconfig|-----|
|ping|we talk over ICMP and try to communicate to another machine|---|
|arp|map IP to MAC|----|
|netstat|display all connections in listening ports|||
|route|display routing table|----|


## ifconfig
The `ifconfig` command is used in Linux to display network configuration details such as IP address, subnet mask, and default gateway for all network adapters.

- **Usage:** 
   - Display network configurations: `ifconfig`
- **Output:** 
   - Active network interfaces, their respective IP addresses, subnet masks, and other network-related configurations.
   - Example: `eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500 inet 192.168.1.2  netmask 255.255.255.0  broadcast 192.168.1.255`
- **Notes:** 
   - The `ifconfig` command is considered deprecated, and `ip` is preferred for modern systems.

## iwconfig
`iwconfig` is a command specific to Linux that displays and manipulates wireless network interface configurations.

- **Usage:**
   - Display wireless network details: `iwconfig`
- **Output:**
   - Information about wireless network interfaces, such as the SSID, channel, and encryption status.
   - Example: `wlan0     IEEE 802.11  ESSID:"Network"  Frequency:2.412 GHz  Access Point: 00:1A:2B:3C:4D:5E`
- **Notes:**
   - For non-wireless interfaces, the output will specify "no wireless extensions."

## ping
The `ping` command is utilized to test the reachability of a host on an IP network and to measure the round-trip time for messages sent from the originating host to a destination computer.

- **Usage:**
   - Ping a host: `ping <hostname or IP address>`
- **Output:**
   - The round-trip time in milliseconds for packets sent to the target host, indicating the latency and reachability.
   - Example: `64 bytes from 192.168.1.1: icmp_seq=1 ttl=64 time=0.026 ms`
- **Notes:**
   - ICMP (Internet Control Message Protocol) is used by `ping` for sending echo request and echo reply packets.

## arp
The `arp` command displays and manipulates entries in the Address Resolution Protocol (ARP) cache, which maps IP addresses to MAC addresses.

- **Usage:**
   - Display ARP table: `arp -a`
- **Output:**
   - The ARP table showing IP addresses and their corresponding MAC addresses, along with the interface.
   - Example: `192.168.1.1 ether 00:1a:2b:3c:4d:5e C eth0`
- **Notes:**
   - Useful for network troubleshooting and ensuring proper IP to MAC mappings.

## netstat
`netstat` is a powerful command used to display network connections, routing tables, interface statistics, and more.

- **Usage:**
   - Display all active connections and listening ports: `netstat -a`
- **Output:**
   - Active connections, listing protocol, local address, foreign address, and state (for TCP), along with listening ports and associated addresses.
   - Example: `tcp        0      0 192.168.1.2:22        192.168.1.3:54321     ESTABLISHED`
- **Notes:**
   - A versatile tool for monitoring network configurations and activity.

## route
The `route` command is utilized to show and modify the IP routing table, which is crucial for directing network packets along the proper path.

- **Usage:**
   - Display the routing table: `route -n`
- **Output:**
   - The routing table including the destination, gateway, genmask, flags, metric, and interfaces used.
   - Example: `Destination     Gateway         Genmask         Flags Metric Ref    Use Iface`
- **Notes:**
   - Modern systems often use `ip route` instead of the traditional `route` command.

## Excercise

1. **Exploring Network Interfaces:**
   - Open your terminal and type `ifconfig` and hit *enter*. This command displays the network configuration of your system.
   - Observe the list of network interfaces and their respective configurations. Each network interface (e.g., `eth0` for wired connections, `wlan0` for wireless) has its own set of configurations like IP address, netmask, and broadcast address.

2. **Detailed Interface Information:**
   - Now, to see detailed information about a specific interface (e.g., `eth0`), type `ifconfig eth0` and hit *enter*. 
   - Note down the IP address, netmask, and broadcast address. The IP address is the unique address assigned to your device on the network, the netmask helps in identifying the network and host portion of the IP address, and the broadcast address is used to send data to all devices on the network.

3. **Wireless Configurations:**
   - Type `iwconfig` and hit *enter*. This command displays information about wireless network interfaces.
   - If a wireless interface is present, note down the ESSID (name of the wireless network) and the Access Point MAC address. MAC address is a unique identifier assigned to network interfaces.

4. **Testing Network Reachability:**
   - Type `ping -c 4 google.com` and hit *enter*. The `ping` command tests the connectivity between your device and the network host (in this case, google.com).
   - Observe the time taken for each packet to reach the destination and return. This is known as round-trip time and is measured in milliseconds.

5. **Exploring ARP Cache:**
   - Type `arp -a` and hit *enter*. The `arp` command displays the Address Resolution Protocol (ARP) cache which maps IP addresses to MAC addresses.
   - Note down any IP to MAC address mappings displayed.

6. **Viewing Network Connections:**
   - Type `netstat -a` and hit *enter`. The `netstat` command displays network connections, listening ports, and network statistics.
   - Observe the various active connections and listening ports. Active connections show the current connections to and from your machine, while listening ports show the network ports that are waiting for incoming connections.

7. **Exploring Routing Table:**
   - Type `route -n` and hit *enter*. The `route` command displays the routing table which is used to determine where to send network packets.
   - Note down the destination, gateway, and interface used for each route. The destination is where the packet is going, the gateway is the next hop in the network, and the interface is the network adapter used.

8. **Advanced Network Statistics:**
   - Type `ip addr show` and hit *enter* to see a detailed list of network interfaces and their configurations.
   - Type `ip route show` and hit *enter* to view the routing table.
   - The `ip` command provides a lot of information about network configurations and is the modern replacement for many traditional network commands.

