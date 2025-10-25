---
title: UNDERSTANDING IP, ENCAPSULATION, TCP/IP AND PORTS
date: 2025-10-23
source type: video
tags:
  - source
  - Networkfoundations
  - networking
  - ports
---



### CONCEPT
Understanding the basics of the IP protocol and encapsulation, alongside the importance of order of communications through the existence of ports

### KEY TAKEAWAYS
Data is not sent to the web at random. The way that a ***payload***(data sent through the web) is directed to it's objective is through the use of *encapsulation*. The payload is encapsulated by the Transport protocol (either *TCP* or *UDP* ). The Transport protocol becomes then encapsulated by the IP protocol, and, finally, whenever the packet reaches a router, it receives a Data Link Protocol through an Ethernet Header and Trailer, which get stripped on the next router, and encapsulated once more.

This process is reversed on the receiver device.

The responsible protocols for the correct delivery of data are *TCP* and *UDP*, which are two *[[The OSI Model|Layer 4 ]]* protocols that control the way that the payload gets sent through the network. There are, however, key differences between the two of them:

---
#### TCP VS UDP


|                    | TCP                                                                                                                                                                                                                            | UDP                                                                                   |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| Type of connection | It is *connection oriented* communication, it always asks to begin a communication and to fully close it                                                                                                                       | Connection-less, it simply sends, it doesn't open or close communications             |
| Control flow       | It constantly checks the information that it sends and receives, so depending on the amount received correctly and incorrectly, and if blotting happens, it can reduce the amount or raise, slow the sends or speed them, etc. | There is no flow control to speak of, it simply sends and however it reaches, reaches |
| Speed              | Fast                                                                                                                                                                                                                           | Much faster than TCP                                                                  |
| Use cases          | Downloading a Game, Downloading a PDF                                                                                                                                                                                          | Video streaming, or any kind of streaming in general                                  |

---
#### Ports
***Ports are numbers that designate the protocol to be used by a payload***.

**Ports are not made for security, but mainly for communication**. Once the destination is arrived, they inform the payload where to go/by whom it will be used. Since, yet again, they are not made for security, they can be changed from both server and client side. Not only that, but it would not help security as much as getting a firewall would. That said, **most services use permanent ports to be able to connect with the wider part of devices**, since changing the port would require all of the other clients connected to change theirs as well. However, that is not a rule, since at the end of the day they are just numbers.

There are in total ***65535 ports***, **1023 of which are called permanent or non-ephemeral**, and the rest temporal or ephemeral. That said, **UDP and TCP each their own 65535 ports in parallel to each other**, making it possible to use two ports "80" simultaneously.

From the client to the server:

|             |      Example IP      |       Port Used        | Data type |
| :---------: | :------------------: | :--------------------: | :-------: |
| From client | Source IP = 10.0.0.1 | TCP source Port = 3000 | Http data |
|  To server  |  Dest IP = 10.0.0.2  |   TCP dest Port = 80   | Http data |

And the answer is:

|             |      Example IP      |      Port Used       | Data type |
| :---------: | :------------------: | :------------------: | :-------: |
| From server | Source IP = 10.0.0.2 | TCP source Port = 80 | Http data |
|  To client  |  Dest IP = 10.0.0.1  | TCP dest Port = 3000 | Http data |


---
### INSIGHT
It is interesting to notice yet again the pattern/repetition of a theme, but this also shows to be an struggle between control (TCP) and comfort (UDP). The more comfortable option, however, is still extremely relevant on it's own uses, and while it is true that we don't have to manually set-up TCP, unlike UDP, if an error arises it can completely break the communications depending on how the communications are set-up. It also shows the importance of order in communications, both through the use of TCP, and the existence of ports in on themselves. Even though UDP is based on constant communications being "thrown", it needs to know the port and protocol to be used in a proper manner.

I also noticed that this video only used it as a passing glance, however it doesn't truly delve into the importance of encapsulation (Why it is important to know it). I will have to investigate that later on my own. My guess would be troubleshooting and understanding, but i want to reach a deeper meaning.

---
##### QUESTIONS
- What are the main differences between TCP and UDP?
- What exactly means encapsulation, and why it is important regarding communication?
- What is a port, and why are they important.

---
**Linked Notes:**
#ControlvsComfort 
[[20251022-Comfort and control]]

