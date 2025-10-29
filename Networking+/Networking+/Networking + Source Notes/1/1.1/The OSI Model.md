2025-10-20

### CONTENT
>The OSI model is a standard of how a connection between the end device and the network works. It is meant to be used as a guide or global standard to ease communications when referring to/ troubleshooting anything network-related, be it physical or system-based.

### KEY TAKEAWAYS
>There are 7 layers:

| Layer           | Description                                                                       | Use Case                                                                                                                                                   | Protocols                               | Examples                                                                             |
| --------------- | --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------- | ------------------------------------------------------------------------------------ |
| 7- Application  | The layer we see and interact with                                                | Mostly visual, any application we use                                                                                                                      | DNS, HTTP/HTTPS, FTP, SSH               | Whatever you see on the screen right now                                             |
| 6- Presentation | The layer that translates information between machine and user                    | Encryption, Decryption, Translation between human-machine                                                                                                  | SSL, TLS                                | The fact that we do not read binary code                                             |
| 5- Session      | The layer that manages sessions between device&application/system                 | Tunneling, management systems                                                                                                                              | Control protocols, Tunneling Protocols* | The fact that whenever i use firefox, the tabs do not mix between each others        |
| 4- Transport    | The layer that manages the movement of the data                                   | It checks, corrects, resends and manages the data flow through the use of UDP and TCP                                                                      | TCP, UDP                                | Whenever we download something online                                                |
| 3- Network      | The layer that manages connections between networks, be it LAN with WAN or others | The fact that we can connect to the Internet without constant issues                                                                                       | IP                                      | A router connecting my home to the Internet                                          |
| 2- Data Link    | Manages and corrects issues in communications between local devices/connections   | The layer that manages the connections between the routing system/external information and guides it to the correct device, through the use of LLC and MAC | MAC, LLC                                | The fact that information coming to my computer doesn't end up in mother's telephone |
| 1- Physical     | All of the hardware in the system                                                 | Is the device itself, which we use                                                                                                                         | No protocols                            | The cpu of a computer                                                                |



[^Didn't remember the protocols for the Layer 5, look into it]