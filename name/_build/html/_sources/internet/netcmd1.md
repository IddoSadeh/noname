# Network Commands 1

## Getting Started with Linux Networking Commands

Now that we have a basic understanding of how the internet works, let's explore some common tools and commands on Linux that help us interact with the network.

1. **`ifconfig` / `ip`**:
   - These commands are your first step into viewing and configuring the network settings on your Linux machine. With `ifconfig` or `ip`, you can view your IP address, MAC address, and other network-related information about your Network Interface. It's like checking your mailbox and seeing your building's nameplate and color in the internet city.

2. **`ping`**:
   - The `ping` command helps you check if another building (device) in the internet city is reachable. It's like shouting across the street to see if your friend can hear you. When you use `ping`, you send a small message to another device and wait for a response.

3. **`arp`**:
   - Recall the Address Resolution Protocol (ARP) that helps find a building's color (MAC Address) using its nameplate (IP Address). The `arp` command displays and modifies the ARP table in your machine, helping you see the mapping between IP addresses and MAC addresses.

4. **`netstat`**:
   - The `netstat` command provides a peek into your building's interactions with other buildings. It shows all the connections to and from your machine, and the ports that are being used for these communications. It's like having a log of all the visitors to your building and the doors (ports) they used.

5. **`route`**:
   - The `route` command helps you view and modify the routing table. The routing table is like a map in your car that helps guide your packets (cars) on which roads to take to reach other buildings.

## Exercises

Now, let’s dive into some exercises to help familiarize ourselves with these commands and see them in action.

### Exercise 1: Exploring Network Interfaces

1. Open your terminal.
2. Type `ifconfig` or `ip addr` and hit *Enter*.
   - Observe the list of network interfaces and their associated IP and MAC addresses.
   
### Exercise 2: Checking Connectivity

1. In the terminal, type `ping 8.8.8.8` and hit *Enter*.
   - You are sending packets to Google's public DNS server to check if it's reachable. Hit *Ctrl+C* to stop the ping.
   
### Exercise 3: Exploring ARP

1. In the terminal, type `arp -a` and hit *Enter*.
   - Observe the ARP table showing the mapping of IP addresses to MAC addresses.

### Exercise 4: Viewing Connections and Ports

1. Type `netstat -an` and hit *Enter*.
   - This will show all active connections and the ports being used.

### Exercise 5: Exploring the Routing Table

1. Type `route -n` or `ip route` and hit *Enter*.
   - Observe the routing table and identify the gateway IP address.

