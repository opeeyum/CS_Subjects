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
 
 ## Responsibilities of Data Link Layer

`To be continued...`
