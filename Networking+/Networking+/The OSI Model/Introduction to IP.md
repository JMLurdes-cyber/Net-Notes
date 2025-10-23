### CONCEPT
Getting a basic understanding of how the IP protocol works alongside an introduction to the principle of encapsulation in networking

### KEY TAKEAWAYS
Data is not sent to the web at random. The way that a ***payload***(data sent through the web) is directed to it's objective is through the use of *encapsulation*. The payload is encapsulated by the Transport protocol (either *TCP* or *UDP* ), then it is encapsulated once again by the *IP protocol*, and finally, by whatever *Data Link layer protocol* is used, through the topology laid for it to reach it's destination

The responsible protocols for the correct delivery of data are *TCP* and *UDP*, which are two *[[The OSI Model|Layer 4 ]]* protocols that control the way that the payload gets sent through the network. There are, however, key differences between the two of them:

|                    | TCP                                                                                                                            | UDP                                                                                   |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| Type of connection | Connection Oriented: It always checks on the information that its being sent, and there are formal agreements of each transfer | Connection-less, it simply sends, it doesn't open or close communications             |
| Control flow       | It can use control flow, setting priorities, breaks, speed differentiation and recovery in case of an error                    | There is no flow control to speak of, it simply sends and however it reaches, reaches |
| Speed              | Fast                                                                                                                           | Much faster than TCP                                                                  |
| Use cases          | Downloading a Game, Downloading a PDF                                                                                          | Video streaming, or any kind of streaming in general                                  |
