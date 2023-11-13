# The Internet

The internet is a complex subject that can takes years to understand. This chapter summarizes the big ideas of the internet. If you are a visual learner, The following resources are excellent for building a conceptual understanding of the internet are [The Odin Project](https://www.theodinproject.com/lessons/foundations-how-does-the-web-work) and [Harvard's CS50](https://cs50.harvard.edu/ap/2024/curriculum/technology/weeks/internet/).



## Internet 101
In short, you can think of the internet like a city:

- Buildings are computers.
   - Servers are also computers.
- Buildings and people have addresses.
   - In a city, your address and your homes address are the same. Computers are a bit different:
      - The address of a building is a **MAC Address**. This never changes as long as the building (computer) exists.
      - The address of a person is a **IP Address**. This will change often, even if you log on from the same computer in the same location twice.
         - There are two types of IP addresses (IPv4 and IPv6) explained in the next section.
      - The Address Resolution Protocol (**ARP**) maps these two addresses one to another.
- A buildings mailbox is a **Network Interface**.
- Buildings have different doors/enterances, computers have different **ports**.
   - Different ports have different utilities.
- Roads are the network paths (cables) that alow for the flow of information between two computers.
- As with people flow in cities with cars, information flows through the internet in **packets**.
   - For many reasons, information is broken apart to many packets and reassambled at the destination.
- Humans may use a GPS to navigate a city, Packets stop at **gateways** throughout their journey to get directions to their endpoint.
   - Each gateway stop is called a **Hop**.
- A cities traffic rules or care safety regulations can are called protocols in the internet.
   - The **TCP/IP** model allows for computers to communicate with each other.
      - These protocols are about standardizing communication, not necessarly about safety.



## More Important Concepts

Some more terms you may hear get thrown around a lot:

- Just like most businesses in a city will have a name and a address, websites have a domain name and an address. 
   - Browsers use a Domain Name System (**DNS**) to translate the domain name of the website (www.google.com) to the address (8.8.8.8).
- Computers, servers, software and hardware all use **Cache**. Cache is like a small notebook you keep handy with information you may need readily available.
- A Virtual Private Network (**VPN**) is a alternate network you can use to ensure your information is secured.
- **Firewalls** are programs that make sure any information going in and out of your computer is safe.









