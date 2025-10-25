### CONCEPTS
>Understanding  how Cloud networking simulates physical infrastructure through VPCs, NFV and virtual security.

### KEY TAKEAWAYS
>Cloud computer is the answer to the cost/needs of a physical server, with its needs like space, maintenance and such, and making it into a more available option for all, even if it can come with costs of it's own.

### TRADE OFFS
- + Reduces the need of physical infrastructure, alongside its maintenance
- - Increases dependency in cloud providers
- - Reduces security based on dependency on multiple cloud enviroments

##### Objectives of the Cloud 
- An effective server that can be used **on demand**.
- An **elastic** server that can *scale* as needed, both up and down.
- A server that **can be accessed from everywhere** by a **multitude of people**

### CLOUD COMPONENTS
| Component                             | Function                                                                                                                                                                                                                                                                   | Example                                                                                                                                                    |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| VN - Virtual Network                  | A single (or group) of servers found on the cloud, taking the function of a physical server farm.                                                                                                                                                                          | A smaller business that wants to have a reliable network not having the funds/space to get a full working server farm.                                     |
| NFV - Network Function Virtualization | It emulates functions and devices usually found in physical networks, while commonly being controlled via hypervisors                                                                                                                                                      | A reliable network needs to have a solid topology/good connections. Without it, it would be like having a lot of servers directly connected to each device |
| VPC - Virtual Private Cloud           | Virtual spaces within the network which usually fulfill different objectives. To connect to each other, a *transit gateway* needs to be set in the middle of the VPCs. A common security method is to connect to the VPCs through the use of a [[Networking Devices\|VPN]] | They are basically Cloud VLANs, included the virtual subnets                                                                                               |
#### CLOUD CONNECTIONS
To set up the connections to the  ***VPCs***  there are a few devices that need to be fixed: 

| Device                                           | Function                                                                                                                                                                                                  | Use Case                                                                                                                                          |
| ------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| [[Networking functions\|VPN]]                    | Connects the client network to the VPC through the internet                                                                                                                                               | If using a VPC, an office can be connected directly to it using a VPN                                                                             |
| Virtual Private Cloud Gateway / Internet Gateway | Connects the VPC to the internet, for users to use if intended                                                                                                                                            | If there is a website setup in one of the servers which is meant to be public-facing                                                              |
| VPC NAT gateway                                  | It allows the VPC to get external resources, alongside translating the private IPs to public ones. Needs to be setup if there are intentions to get inbound connections, but not outbounds, or vice-versa | If there is a website set up and it needs to pull resources from wikipedia to get a reference source/backup                                       |
| VPC Endpoint                                     | It allows direct communications between two different cloud providers without needing to access the internet.                                                                                             | If a business is using two providers for [[Networking Devices\|load balancing]], and wants the primary to send backups to the secondary directly. |

#### CLOUD SECURITY

>Similar to a physical network, VPCs require of robust protection through the use of both NFVs and settings. Within those settings we can find the ***Security Groups*** and the ***Security Lists*** that help filter incoming connections.
>Even though both act as a whitelist that filters the allowed connections (inbound or outbound) basing themselves on ports, protocols or IP ranges (similar to a firewall), the Security ***Lists*** are meant to be rules that apply to the whole VPC, while the Security ***Groups*** apply only to a delimited set of groups within the VPC, giving more control and needing more administration. Basically, if  a VPC *is not meant to have any kind of access to Telnet*, a List could be used to block any connection to it, while if *a computer or a certain group is not meant to have access to web browsers*, they could instead make a group to do so. 


### INSIGHT

This section taught me the foundations of a solid cloud network, while explaining to me that, just like physical networks, a solid foundation is based on self-regulation, through the use of Network Functions and Virtual Private Clouds.

That said, it also shows that to win some you have to lose some, since most businesses won't be able to make Cloud Networks from and for themselves, which means that to a degree they will have to rely on their Cloud provider(s) to get the systems that they cannot get.


### QUESTIONS
- Describe a Virtual Private Network and it's components.
- Describe what does NFV mean.
- Explain the pros and cons of Cloud networking in comparison to a physical server
- Describe the foundations of a solid cloud framework.










**Linked Notes:**
[[2025-10-21-Autonomy-as-a-principle]]
#AutonomousSystems 