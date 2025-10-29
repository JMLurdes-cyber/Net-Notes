### CONCEPTS
Understanding the use of CDNs, VPNs, QOS and TTL and how do they form a self-regulating network.

### KEY TAKEAWAYS
To make a network work autonomously without constant human input, a series of functions can be implemented for self-regulation and added control over the traffic movement.

### DEVICE LIST

| FUNCTION                       | DESCRIPTION                                                                                                                                                                                                                           | USE CASE                                                                                                                                                                                                                  |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CDN - Content Delivery Network | Basically web servers, they are the "local server" that a lot of services has, to lower the wait time until a service is granted                                                                                                      | A lot of video games separate their servers basing them on location, for example.                                                                                                                                         |
| VPN - Virtual Private Network  | They are systems that encrypt all of the data that passes through them until it gets to the objective. They can also be used to hide one's origin IP address. They can be software of hardware depending on the scale of the network. | To work from home without compromising the security of the network.                                                                                                                                                       |
| QOS - Quality of Service       | Combination of settings -which route to take, how many hops to make,  which kind of information to send-   that makes up a network.                                                                                                   | If a lot of devices are connected to a network in a hospital, for example, all of the directly related to health/medicine (computers containing logs, for example) should take priority over a single doctor's telephone. |
| TTL - Time To Live             | Countdown that drops the packet sent when it hits 0. In networking, it can either count hops (amount of times passing through a router) or time.                                                                                      | If a packet is not going forward, we probably don't want it to keep trying for eternity, but to stop and try to fix whatever causes it to **not** go forward.                                                             |
| Routing Loops                  | Event that happens when a bunch of routers form a circle motion instead of a line to follow to the objective, going in a loop only stoppable manually or by TTL                                                                       | If i set up the router 10.1.0.1 to be followed by the router 10.2.0.1, and that router is set to send packages to 10.1.0.1                                                                                                |

### INSIGHT
For a network to be sound, it needs to be able to perform as intended both with or without constant input and correction, which is a condition fulfilled through the correct use of the right [[Networking Devices|devices]] and functions.

#NetworkTroubleshooting #Networkfoundations


#### QUESTIONS
- What are the key signs that a network lacks autonomy?
- How do VPNs and CDNs each contribute to perceived network reliability?