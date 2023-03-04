## IOS - OSI model
- It stands for international organisaton for standardization - open system interconnect.
- Consist of seven layers
   1. Physical layer
   2. Data link layer
   3. Networking layer
   4. Transport layer
   5. Session layer
   6. Presentaion layer
   7. Application layer
- Application and Physical layer do not add any header to a packet.
- Presentation, Session, Transport and Network layer adds only header to the packet.
- Data link layer adds header as well as tail header into the packet.

## Responsibilties of Physical layer
1. Physical characteristics of media i.e Copper, glass plastic and its type i.e. wired or wireless
2. Representation of bits -> Encoding i.e Manchester or Differential Manchester encoding.
3. Data rate / transmission rate -> Number of bits transmitted per second / bit duration -> How long bit last on transmssion media
4. Synchronisation -> Sender and reciever clock should be synchronised on a bit level
5. Line configuration i.e Point to Point, Multi Point
6. Physical topology -> How a network is laid out i.e Mesh, Bus, or ring topolgy
7. Transmission modes
    - Simplex -> Unidirectional
    - Duplex -> Bi-directional but one at a time
    - Full Duplex -> Bi-directional.
   
## Types of Addresses
Physical Address
  - Unique within a LAN
 
Logical Address
  - Unique in internet
  
Port
  - Unique within Machine for differnet processes
<table>
  <tr>
    <th>IP Address</th>
    <th>MAC Address</th>
  </tr>
  <tr>
    <td>Internet Protocol Address</td>
    <td>Media Access Control Address</td>
  </tr>
  <tr>
    <td>Implementation of Logical Address</td>
    <td>Implementation of Physical Address</td>
  </tr>
  <tr>
    <td>32 bit</td>
    <td>48 bit</td>
  </tr>
  <tr>
    <td>Unique in Internet</td>
    <td>Unique in Internet</td>
  </tr>
  <tr>
    <td>Stored IN RAM</td>
    <td>Atored in ROM of NIC card</td>
  </tr>
  <tr>
    <td>Header of Network Layer contain IP</td>
    <td>Header of Data Link Layer contains MAC</td>
  </tr>
 </table>
 
 ## Data Link Layer
 Data link layer is responsible for node to node (or **Hop tp Hop**) delivery of packets called **Frames**.
 - Functions:
   1. **Framing** -> DLL add header and tail to the datagram received from network layer and resulting packet is called frame.
   2. **Physical addressing** -> Header of the frame contains physical address of both dender and receiver if both are in same network but if both are in different network then it may contain physical address of intermediate node also.
   3. **Flow control** -> Amount of data that can be sent from sender to receiver before receiving acknowledgement.
   4. **Error Control** -> 2 strategies Error detection & Retransmission (Prefered technique), Error Correction.
   5. **Access Control** -> Who can access the shared channel and When?

## Network Layer
N/W layer is responsible for **Host to Host** delivery of packets called **DataGram**.
- FUnctions:
   1. **Logical Addressing** -> Header of N/W layer contain logical address of both sender and receiver.
   2. **Routing** -> Routing means to route the packet to final destination we have various routing protocols which work at N/W layer.
   3. **Quality of Service** -> Quality is a subjective term, so to measure quality quatitatively we have to consider the certain parameters **Reliability, Delay, Jitter, Bandwidth**. `Jitter: Variation in timing of receiving packets.`
   4. **Congestion Control** -> If number of packets present in the N/W is greater than teh number of packets it can handle then we say congestion has occurred.
   5. **Fragmentation** -> If datagram size is more than MTU of the N/W then fragmentation is done. `MTU: Maximum transmission unit`.

## Transport Layer
**End to End** delivery of entire message or process to process delivery.
- Function:
   1. **Secure Point Addressing** -> Header of transport layer contains port address of both sender and receiver.
   2. **Segmentaion and Reassembly** -> Transport layer divides stream of bits received from session layer into small packets called segments, each segments had segment number which help the transport layer at receiver end to reassemble the segments.
   3. **Connection Control** -> Transport layer can be connection-less or connection oriented.
   4. **Flow Control** ->
   5. **Error Control** ->
   6. **Congestion Control** ->
   7. **Multiplexing and Demultiplexing** ->  Multiplexing at sender side and demultiplexing at receiver side. 

## Session Layer
Session Layer is also known as N/W dialogue congestion.
- Function:
   1. **N/W dialouge controller** -> Seesion layer establishes, maintains, synchrinize & terminate the interaction b/w sender & receiver.
   2. **Synchronization of data** -> Session layer some synchronization bits to the message and these bits may used as a checkpoints.
   3. **Token Management** -> Cookies or token are generated at server side & sent to client so that in next session these cookies are showen by client to server and hence server can recognize the client.
   4. **Authentication & Authroization** -> N/W security.

## Presentation Layer
This layer mainly deals with syntax and semantics of information excanged b/w 2 systems.
- Funtions:
   1. **Translation** -> 
   2. **Encryption** ->
   3. **Compression** -> Compression at sender side and decompression at receiver side.
 
## Application Layer
This layer acts a an interface b/w user applications and N/W.
- Functions:
   1. **Interface**
   2. **FTAM** (File transmission access and Management)
   3. **Remote Login**
   4. **Directory Services** -> Accessing any kind of information from distributed databases.
   5. **Email services** -> Email forwarding and storage

## Why OSI model failed?

`To be continued...`
