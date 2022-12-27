# Switching in Network Layer

In the following article, we will discuss what switching is, its different types and where and how they are implemented. So, let's begin...

# Switching

Switching is done at the Network layer; this method is used to find the best possible route for data transmission. Switching is majorly classified into three types:

1. Circuit Switching
    
2. Packet Switching
    
    1. *Virtual Circuits*
        
    2. *Datagram*
        
3. Message Switching
    

## Circuit Switching

This switching type is not done on the network layer but on the physical layer. It is currently an obsolete method. Circuit Switching was used in telephone networks in the 1980s.

### Working on the Circuit Switching

![A connectin with B through manual physical wire connection with circuit switching](https://cdn.hashnode.com/res/hashnode/image/upload/v1672123914833/57a0a79c-ff1a-4afb-9966-2290533ba6d7.png align="left")

1. `A calls Telephone Operator I to call B.`
    
2. `The telephone operator keeps a log and doesn't connect the physical wire immediately.`
    
3. `Telephone Operator(TO) will contact the next TO in Telephone Exchange (TE) and the next TO in TE, who (let's say) finally calls B. They then set up the physical wire between the two people.`
    
4. `A and B are now able to talk.`
    

### Advantages of Circuit Switching

1. Headers are unnecessary because the entire track is laid down to transmit that message.
    
2. The data go in order, and hence no sequence orders are required.
    

### Disadvantages of Circuit Switching

1. Multiple people are required as Telephone or Data Operators to connect wires manually daily, making it costly.
    
2. The messages are interceptable at the Telephone Exchange points.
    
3. The messages don't get immediately sent and are usually stored in the log book for a while.
    
4. Setup time and Teardown time for the link is an additional requirements.
    

### Where can it be used?

In the case of very big/ bursty data, packet switching tends to be costlier than circuit switching. Packet Switching is better for small data.

For example, Google is trying to switch continents of their head office. They will tend to buy their network and connect to their old office to avoid multiple hops that usually lead to delays in data transmission.

Individuals will not buy wires to connect themself and their friends to communicate.

## Packet Switching

Also known as store and forward network, this switching employs multiplexers and demultiplexers to set packets dynamically.

### Pipelining or Packetization in Packet Switching

This method is based on pipelining, introduced by Henry Ford to reduce the time to manufacture a car from 6 to 7 months to just 21 days.

**For example: Let's say that a team takes 1 day to complete their tasks and 4 days to build a car. For a single car, the pipelining doesn't make a difference:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672126550526/a802badc-038f-47dd-87cb-eb1f51331943.png align="center")

*But for 100 cars without pipelining = 4x100 days = 400 days*

*And 100 cars with pipelining = 4 (to build the first car)+ 99x1 = 103 days*

Thus with pipelining, the number of average days comes closer to one day, bulkier the order gets. To address it as an example to explain when and at which parameters packetization is advantageous and where it isn't.

`Let Data that needs to be transmitted is 1000 bytes and Bandwidth given is 1 Mbps. The header size given is 100 bytes. Total no. of switches between the receiver and sender is 2.`

`Let's say we send the data without making smaller packets. So, the data that needs to be sent in the packet`

`= Size of data + Size of header = 1000 bytes + 100 bytes =1100 bytes.`

`For sake of simplicity, let's assume time for storing at the switch and then sending it to the wire (Tp)=0 ms`

`Transmission Time (Tt) = Packet size/Bandwidth = 1100 bytes/1 Mbps = 1100 b/10^6 bps = 1.1 ms`

`Thus to reach to the receiver`

`= No. of switches xTransmission Time = 3 x 1.1 ms = 3.3 ms`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672151900266/725f7781-cbaf-4534-9ab9-c92fc0036acd.png align="center")

`Now, let's say the packets are divided into smaller packets = 5.`

`Data is equally distributed among 5 packets = 1000/5 bytes = 200 bytes`

`So, the data that needs to be sent in the packet`

`= Size of data + Size of header = 200 bytes + 100 bytes =300 bytes.`

`For sake of simplicity, let's assume time for storing at the switch and then sending it to the wire (Tp)=0 ms`

`Transmission Time (Tt) = Packet size/Bandwidth = 300 bytes/1 Mbps = 300 b/10^6 bps = 0.3ms`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672156832248/c70cb9e5-e24c-4702-9f53-c182cb9ffbdb.png align="center")

`Thus to reach to the receiver for the 1st packet`

`= No. of switches x Transmission Time = 3 x 0.3 ms = 0.9 ms`

`And for the remaining packets to reach to the receiver`

`= No. of remaining packets x Transmission Time = 4 x 0.3 ms = 1.2 ms`

`Total time taken = (0.9 + 1.2) ms = 2.1 ms`

In this case, there is no wastage of waiting time for routers for 1000 bytes altogether. It can transmit receiving 300 bytes.

We can now say let's put the data together in smaller packets.

`Now, let's say the packets are divided into smaller packets = 10.`

`Data is equally distributed among 10 packets = 1000/10 bytes = 100 bytes`

`So, the data that needs to be sent in the packet`

`= Size of data + Size of header = 100 bytes + 100 bytes = 200 bytes.`

`For sake of simplicity, let's assume time for storing at the switch and then sending it to the wire (Tp)=0 ms`

`Transmission Time (Tt) = Packet size/Bandwidth = 200 bytes/1 Mbps = 200 b/10^6 bps = 0.2 ms`

`Thus to reach to the receiver for the 1st packet`

`= No. of switches x Transmission Time = 3 x 0.2 ms = 0.6 ms`

`And for the remaining packets to reach to the receiver`

`= No. of remaining packets x Transmission Time = 9 x 0.2 ms = 1.8 ms`

`Total time taken = (0.6 + 1.8) ms = 2.4 ms`

Initially, the time was reduced by packeting the big packet, but now it increased. There is a threshold on the size of small packets. The header size should not be equal to or dominate the packet size. In that case, the time is taken to packetize and send increases.

> In Internet, this packet size = 2^16 bytes.

### Advantages of Packet Switching

1. Setup time and Teardown time for the link are not required.
    
2. No manual intervention. More cost-effective. The entire thing is dynamically run in the store and forward network.
    

### Disadvantages of Packet Switching

1. The data doesn't go in order; hence, in their Network Layer headers, the packet number is marked as Sequence Numbers.
    
2. Headers are necessary because the entire track is not laid down to transmit that message. The path is instead found while the packet is sent from hop to hop.
    

We will discuss two types of Packet Switching in the next blog. Till then, thanks for reading! ❤️

If you are also into Computer Networks, let me know in the comments. Also, connect with me on my social: [LinkedIn](https://www.linkedin.com/in/sourajita-dewasi-52b3b4193/), [Twitter](https://twitter.com/SourajitaD) or GitHub!