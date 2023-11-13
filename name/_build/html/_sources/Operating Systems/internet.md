# The Internet

There's a lot to know about the internet, and a lot of terminology to learn. It's okay not to rememebr everything at once. Included is a story to help you make connections between all the terminology, followed by a list of the the terms.
**The Internet imagined as a city**

The internet can be imagined as a giant city with many buildings. Each building has a different functionality; some are homes (your computer), and some are places you can learn or buy things (Wikipedia or Amazon).

Every building in this city has a permanent, unique address known as a MAC Address. This is like the building's permanent identity, no matter who lives there it remains the same. 

Similarly, every person or business in the city has a unique address called the IP Address. In a real city, the house or business address and the building address are the same. But in the internet city, there's a separation - the MAC Address identifies the building, while the IP Address identifies the person or business inside.

Now, traveling within this city is like data moving around on the internet. The city has a network of roads that help everyone get from point A to point B, similar to network cables on the internet. People get around the city using cars, akin to packets on the internet. And just like how cars might need to stop at gas stations on a long journey, packets make stops known as hops to continue their journey on the internet. These hops are like the big intersections in the city, known as Gateways, that guide cars (packets) to the correct roads, leading them to their destinations, whether within the same part of the city or a different part.

Each home (your computer) in this city has a special mailbox called a Network Interface. This is where all letters (data) are received and sent out. The city's postal service uses the IP Address on the letters to know which building to deliver them to. But the postal service initially doesn't know the color (MAC Address) of the building associated with a nameplate (IP Address). So, it asks a local directory service known as the Address Resolution Protocol (ARP). ARP helps find the color (MAC Address) of the building using the nameplate (IP Address), ensuring the letter reaches the right mailbox (Network Interface).

Sometimes, you might want to send a letter to every building on your street, like inviting everyone to a big party. For this, you use a special address known as the Broadcast Address, which is like addressing the invitation to "Everyone on Elm Street."

In our city, there are clubs you can join, each with a unique name called an ESSID, and a special entrance known as an Access Point. You need to know the club's name and find its entrance to be part of the club and enjoy its activities.

As letters move around, they sometimes need to go through special doors in the buildings to reach the right person or business. These special doors are called Ports, and different types of letters use different ports.

The city’s postal service sometimes keeps a handy notebook known as Cache. In this notebook, they jot down addresses they deliver to often, so they can find them faster next time.

Lastly, to venture out onto the city’s network of roads, each home needs a special tool called a Network Adapter. This is like having a car that allows you to drive on the city’s roads, visiting different places, and sending or receiving letters.

**List of Terms**

1. **Network Interface:**
   - The special mailbox for your home (computer) in the internet city, where letters (data) are received and sent out.

2. **IP Address:**
   - The unique nameplate of your home or business in the internet city, telling others where you are located.

3. **Netmask:**
   - A rule that helps separate the street name from the house number in your IP address, similar to how a real city differentiates between streets and house numbers.

4. **Broadcast Address:**
   - A special address for sending letters (data) to every building on your street at once, like writing "Everyone on Elm Street" on an invitation.

5. **ESSID:**
   - The unique name of a club in the internet city, which you need to know to join and enjoy its activities.

6. **Access Point:**
   - The special entrance to a club (wireless network), where you can join if you know the club's name (ESSID).

7. **MAC Address:**
   - The unique color of your building in the internet city, a permanent identifier for your network interface.

8. **Packet:**
   - Cars in the internet city, carrying people (data) from one place to another.

9. **Hop:**
   - Stops like gas stations on a long journey where cars (packets) refuel to continue their journey on the internet.

10. **Address Resolution Protocol (ARP):**
    - The helpful local directory service that matches a building's nameplate (IP Address) to its color (MAC Address) for the postal service.

11. **Cache:**
    - A handy notebook where the postal service jots down frequently delivered addresses to find them faster next time.

12. **Ports:**
    - Special doors in buildings where different types of letters come in and go out, depending on their purpose.

13. **Gateway:**
    - Major intersections in the internet city that guide cars (packets) to the correct roads, leading them to their destinations.

14. **Network Adapter:**
    - A special tool like a car, enabling you to venture out onto the city’s network of roads, visiting different places and sending or receiving letters.
