OSI(Open System Interconnection) Model defines and is used to understand, How Data is transferred from one computer to another, in a Computer Network. 

In the most basic form, Two computer connected to each other with LAN Cable and connectors and sharing their datas with help of NICs(Network Interface Cards). But IF one computer is based on Microsoft Windows and the other one ha Mac OS installed then how these two computers are going to communicate with eachother ? 

In order to accomplish a successful communication between computers,OSI Model was introduced.

It consist of 7 layers :- 
```
* Application Layer   |
* Presentation Layer  |-> Software Layer
* Session Layer       |
* Transport Layer  |-> Heart of OSI
* Network Layer       |
* Data Link Layer     |-> Harrdware Layer
* Physical Layer      |
```
| Trick|Layer|
------|-------
|Please|Physical Layer|
|Do|Data Link Layer|
|Not|Network Layer|
|Tell|Transport Layer|
|Secret|Session Layer| 
|Password|Presentation Layer|
|Anyone|Application Layer|

Each Layers are Package of Protocols.

# Application Layer:

* Application layer provide services to network applications.
   * Network application are those applications which uses internet e.g Crome, Firefox, Outlook, Skype and many more.
 
| Action|Protocol|
--------|---------
|For file transfer|FTP(File Transfer Protocol) is used|
|For  web surfing|HTTP/HTTPS (Hyper Text Transfer Protocol/Hyper Text Transfer Protocol Secure) is used|
|For  e-mails |SMTP (Simple Mail Transfer Protocol) is used|

# Presentation Layer:

* Presentation layer is responsible for three functions:
  * **Translation**
    *  Presentation layer receives data from application layer in form of alpha numeric characters.
    *  Presentation layer converts those characters into binary language.
  * **Data Compression**
     * Data compression reduces the size of file which result in faster data transmission.
  * **Encryption/Decryption**
     * To maintain the integrity of data, data is **encrypted** at senders side and **decrypted** in Receivers side. 
     * SSL(Secure Sockets Layer)is used in for data encryption and decryption.

## Session Layer:

* The primary objective of session layer is establishing, managing and terminating the sessions between source and destination.
* Session Layer is also responsible for :- 
   * **Check pointing** :- Enables us to restart the downloading from last checkpoint in case of failure.
   * **Authorization & Authentication**:-
       * Authentication confirms that users are who they say they are. 
       * Authorization gives those users permission to access a resource
   * **Synchronization** :- Like in movies audio and video syncronization.

# Transport Layer:

* At any given time on a user’s computer there might be many applications are open which are sending and receiving data from the Internet, and all that data is arriving in the form of 1’s and 0’s on to that computer’s NIC.
* Something has to exist in order to distinguish that which 1’s and 0’s belong to which application. That “something” is Transport Layer.
* Transport layer is responsible for distinguishing network streams through.
    * **Segmentation**
        * Here Data receiverd from Session layer is divided into small peices called segment.
        * Each segment contain, Source & Destination **Port number** and a **Sequence number**.
        * Port number help to direct each segment to its correct application.
        * Sequence number help to reassemble the sequence.

* Transport layer also responsible for controling the reliablity of communication through:
     * **Flow control**
     * **Error control**
 * In transport layer there are two methods for distinguishing the network streams.
    * Transmission Control Protocol (TCP)
    * User Datagram Protocol (UDP).
 
# Network Layer:

* Network Layer receive data **segments** from the Transport layer. 
* Network Layer is reponsibe for:
   * **Logical Addressing** :-  Adding IP address of sender and receiver computer in each Data-segment, after this data-Segment in Network Layer becames **Data-Packet**.
   * Logical addressing is responsible for packet delivery from end to end.
   * **Routing** :- Method to move data packet from source to destination.
   * **Path Determination** :- Choosing best path for deleivering  Data-packets from source to destination.
* Basically network layer help in transmission of the Data-packets from one computer to another computer.

# Data Link Layer:

* Data link layer receives **Data-packets** from network layer.
* Data link layer is responsible for:
    * **Mac addressing**:- The MAC addressing is used to identify each individual NIC, after this data-Packet in Data link Layer becames **Frame**.
    *  MAC addressing is responsible for packet delivery from hop to hop.
    * **Interfacing with the Physical layer** :- Pulling & Pushing 1’s and 0’s into transporting medium i.e wire etc.
* NICs(Network Interface Cards) work in this layer.

1️⃣***Between each Router, the MAC address header is stripped and regenerated to get it to the next hop therefore MAC headers handled the “hop to hop” delivery.***

2️⃣***The IP header generated by the first computer is only stripped off by the final computer therefore IP header handled the “end to end” delivery***

# Physical Layer:
* Physical layer receives **frames** from data link layer.
* Physical layer is the physical medium which is transporting data between two nodes. 
* Transporting medium can be  
    * LAN wire:- If it is a electrical signal.
    * Optical fiber:- If it is a light signal.
    * Air:- if it is a radio signal.
    * Basically anything that carries 0’s/1’s between two nodes.
* Physical layer is responsible for Transferring of bits. 

# At the receiver end:-
* Data Link Layer pull signal from physical layer as a Frame.
* Frame is further decapsulated as data moves through higher layers. 
* Finally,data is moved to Application Layer. 
* Application Layer Protocol makes the sender's message visible in the application in the receiver's computer screen.




In this way, OSI model is helping to transfer data between different hosts. So, these Seven Layers pf OSI model are lying behind the smooth functioning of Internet.
