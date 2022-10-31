# The OSI Model (Open Systems Interconnection )

#### Nodes:

A node is a physical electronic device hooked up to a network, for example a computer, printer, router, and so on. If set up properly, a node is capable of sending and/or receiving information over a network.

### Links

Links connect nodes on a network. Links can be wired, like Ethernet, or cable-free, like WiFi.

### Protocol

A protocol is a mutually agreed upon set of rules that allows two nodes on a network to exchange data.

### Networks

A network is a general term for a group of computers, printers, or any other device that wants to share data.

### Topology

Topology describes how nodes and links fit together in a network configuration, often depicted in a diagram. Here are some common network topology types:

### what’s a layer?

A layer is a way of categorizing and grouping functionality and behavior on and of a network.
In the OSI model, layers are organized from the most tangible and most physical, to less tangible and less physical but closer to the end user.

### there is 7 OSI layer:

Physical Layer
Data Link Layer
Network Layer
Transport Layer
Session Layer
Presentation Layer
Application Layer

## OSI Layer 1 (Physical Layer)

The data unit on Layer 1 is the bit.
There’s a lot of technology in Layer 1 - everything from physical network devices, cabling, to how the cables hook up to the devices.

Nodes (devices) and networking hardware components. Devices include hubs, repeaters, routers, computers, printers, and so on.

Cable types. Options include shielded or unshielded twisted pair, untwisted pair, coaxial and so on. Learn more about cable types here.

#### How to Troubleshoot OSI Layer 1 Problems?

1. Defunct cables, for example damaged wires or broken connectors
2. Broken hardware network devices, for example damaged circuits

## OSI Layer 2 (Data Link Layer)

Layer 2 defines how data is formatted for transmission, how much data can flow between nodes, for how long, and what to do when errors are detected in this flow.

1. Line discipline. Who should talk for how long? How long should nodes be able to transit information for?
2. Flow control. How much data should be transmitted?
3. Error control - detection and correction. All data transmission methods have potential for errors, from electrical spikes to dirty connectors.
4. Media Access Control (MAC): the MAC sublayer handles the assignment of a hardware identification number, called a MAC address, that uniquely identifies each device on a network.
5. Logical Link Control (LLC): the LLC sublayer handles framing addressing and flow control.
6. Header: typically includes MAC addresses for the source and destination nodes.
7. Body: consists of the bits being transmitted.

## OSI Layer 3 (Network Layer)

This is where we send information between and across networks through the use of routers.
Instead of just node-to-node communication, we can now do network-to-network communication.

The data being transmitted in a packet is also sometimes called the payload.

Layer 3 transmissions are connectionless, or best effort - they don't do anything but send the traffic where it’s supposed to go. More on data transport protocols on Layer 4.

## OSI Layer 4 (Transport Layer)

This where we dive into the nitty gritty specifics of the connection between two nodes and how information is transmitted between them.

This layer is also responsible for data packet segmentation

## OSI Layer 5 (Session layer)

This layer establishes, maintains, and terminates sessions.

A session is a mutually agreed upon connection that is established between two network applications. Not two nodes! Nope, we’ve moved on from nodes. They were so Layer 4.

1. Client and server model: the application requesting the information is called the client, and the application that has the requested information is called the server.
2. Request and response model: while a session is being established and during a session, there is a constant back-and-forth of requests for information and responses containing that information or “hey, I don’t have what you’re requesting.”

#### How to Troubleshoot OSI Layer 5 Problems

1. Servers are unavailable
2. Servers are incorrectly configured, for example Apache or PHP configs
3. Session failure - disconnect, timeout, and so on.

## OSI Layer 6 (Presentation layer)

This layer is responsible for data formatting, such as character encoding and conversions, and data encryption.

The operating system that hosts the end-user application is typically involved in Layer 6 processes.

Layer 6 makes sure that end-user applications operating on Layer 7 can successfully consume data and, of course, eventually display it.

##### three fata formating methods to know

1. American Standard Code for Information Interchange (ASCII): this 7-bit encoding technique is the most widely used standard for character encoding.
2. Extended Binary-Coded Decimal Interchange Code (EBDCIC): designed by IBM for mainframe usage.
3. Unicode: character encodings can be done with 32-, 16-, or 8-bit characters and attempts to accommodate every known, written alphabet.

## OSI Layer 7 (application layer)

this is the layer that is ultimately responsible for supporting services used by end-user applications.

Applications include software programs that are installed on the operating system, like Internet browsers (for example, Firefox) or word processing programs (for example, Microsoft Word).
