# OSI Model Overview
The "OSI model" stands for Open Systems Interconnect model and is a conceptual framework built to describe general network communications and the steps required to send and recieve data. It breaks network communication into seven layers with defined functions that separate them.

These layers enable those working with networks to narrow down the source of issues. The visual nature of the model can assist in organization and communication involving the application of software and technology and what aspects of a network they operate on. Best of all, the model can be used as a teaching tool and is a great representation of network functions.

![Layer Info](https://www.lifewire.com/thmb/v1ELh58tFZVN1RadeZxUO77eayo=/750x0/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/OSImodel-8d93f19d50e543348f82110aa11f7a93.jpg)

Layers are ordered from highest to lowest, top to bottom. This means our first layer is the Physical layer at the bottom, and our final seventh layer is the Application layer at the top. Each layer represents a specific stage in communication.

---
Upper layers:

-7: Application

-6: Presentation

-5: Session

These top three layers are considered the host layers which handle network services like data formatting, encryption, and connection management.

Lower layers:

-4: Transport

-3: Network

-2: Data Link

-1: Physical

The bottom four layers are called the media layers and handle hardware functions like routing, addressing, and flow control. 

---

Individual layers have specific tasks within the general functions of their layer groups. In the following pages, we will discuss the protocols and functions of each layer from top to bottom and how they interact with each other. This may seem counterintuitive initially, but the order is based on the direction data flows. Starting at layer seven, data travels from the user to layer one where it is then sent. We begin with the Application layer.

<details>
  <summary>Application Layer</summary>
<br>
The Application layer is the seventh layer and is our most user-facing layer. It's what allows user applications to communicate with each other.
  
![Application Layer](https://user-images.githubusercontent.com/75860671/206801965-4c6766aa-ec0e-4d3e-a343-c5ef076b2c80.png)
  
The Application layer handles and packages data recieved from the Presentation layer. It allows users to store, access, retrieve, recieve, and send data. Before data can be sent back to the Presentation layer to travel through to other end of the model, it must be packaged in the proper format. Likely the most familiar protocol, HTTP is one example that handles data required for web page content.

HTTP is only one protocol however.
Check out [this link](https://www.geeksforgeeks.org/protocols-application-layer/) for more.</details>
  
<details>
  <summary>Presentation Layer</summary>
<br>
The Presentation layer is the sixth layer and handles data representation, encryption, and compression. It recieves data from the Application layer to send to the Session layer and vice versa.
  
![Presentation Layer](https://user-images.githubusercontent.com/75860671/206810871-4fbf1760-4e6f-4454-a1bd-3ad2ee1bedda.png)
  
It encrypts data for secure travel, and it decrypts data recieved for processing. One of its largest responsibilities is the translation of data. It transforms data from a system-specific format into an intermediate form that can be exchanged between different systems while preserving accurate syntax. This is important to ensure that data is readable by many different machines.

Presentation layer protocols can be found [here](https://www.w3.org/People/Frystyk/thesis/Presentation.html).</details>

<details>
  <summary>Session Layer</summary>
<br>
The Session layer is the fifth layer and handles interhost communication.
  
![Session Layer](https://user-images.githubusercontent.com/75860671/206811816-de3e4850-3d3a-41f5-bd34-31e405afefa5.png)
  
When two devices need to communicate over a network, a session must be made that opens a window for such communication. Session creation involves setup, coordination, and termination. When those two devices need to communicate, a session will be started, communication commences in the form of requests and responses, delays are set and errors are managed, and the session is destroyed after communication is complete. The Session layer recieves service requests from the Presentation layer above, and it sends service requests to the Transport layer below.

Wikipedia has a good list of Session Layer protocols [here](https://en.wikipedia.org/wiki/Session_layer).</details>

<details>
  <summary>Transport Layer</summary>
<br>
The Transport layer is the fourth layer and handles the actual transport of data between hosts.

![Transport Layer](https://user-images.githubusercontent.com/75860671/206812345-5b4244ce-f7a4-4dc4-8248-bc2cf218003d.png)
)

This layer receives data from upper layers, segments it, addresses the source and destination ports, and sends it to the Network layer. Flow and error control ensure that data is transmitted successfully and to the right port. Data is transmitted in segments with headers that provide information about the data being transmitted. The Transport layer will acknowledge successful transmissions and re-transmit in the case of failure. When data arrives at its destination, the destination Transport layer will reassemble the segments of data into its whole form.
  
Connection-oriented services are generally handled by the Transmission Control Protocol (TCP), and connectionless services tend to be handled with the User Datagram Protocol (UDP). A chart with other Transport layer protocols can be found [here](https://www.router-switch.com/faq/transport-layer-osi-layer-4-popular-transport-layer-protocols.html).</details>

<details>
  <summary>Network Layer</summary>
<br>
The Network layer is the third layer and handles packet routing and logical addressing.  
  
![Network Layer](https://user-images.githubusercontent.com/75860671/206822236-8e3f7f6d-9bcd-4afd-974a-f05b2ffa555b.png)

Data is transmitted in packets. The Network layer determines the shortest route for these packets to travel to their destination and attaches the IP addresses of the sender and receiver while logging known addresses in logical addressing to aid in routing. This process allows the layer to translate between MAC and IP addresses (physical computer addresses and network addresses respectively) to ensure proper routing.

Network layer protocols can be found [here](https://en.wikipedia.org/wiki/List_of_network_protocols_(OSI_model)).</details>

<details>
  <summary>Data Link Layer</summary>
<br>
The Data Link layer is the second layer and handles the node-to-node delivery of data.
  
![Data Link Layer](https://user-images.githubusercontent.com/75860671/206824011-639784f5-2b75-4ec3-bece-558d74793d2e.png)

  
That means this layer is in charge of delivering the data from one network entity to another entity within the same network. This means adjacent switches, routers, and computers within the same local system. The Data Link layer controls the access those entities have to each other and to the broader network to be sent out to other networks to prevent collisions of data that can cause transmissions to fail. It also handles MAC addressing to log the physical addresses of devices on a network.

[This](https://osi-model.com/data-link-layer/) Data Link layer overview contains a list of Data Link layer protocols.</details>

<details>
  <summary>Physical Layer</summary>
<br>
The Physical layer is the first layer (and our last) layer is responsible for, you guessed it, the physical connections between devices.
  
![Physical Layer](https://user-images.githubusercontent.com/75860671/206825762-f4f0abe2-8043-4e40-904c-07d7ca1d6677.png)

  
The Physical layer handles data in bits, the smallest form of data represented in binary. When it receives data, it converts it into binary and sends it to the Data Link layer where it is put back together. When sending data, it is responsible for turning bits of information into electrical signals. This layer controls the rate of data transmission as well as how data is transmitted through physical hardware. It also defines the physical topology, or structure, of a network and its devices.

[Here](https://osi-model.com/physical-layer/) is a link to the protocols of the Physical layer.</details>

---


