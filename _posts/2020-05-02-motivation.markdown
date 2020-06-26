---
layout: paper
title:  "Motivation"
date:   2020-05-04 17:26:41 +0900
categories: bookmark
---

<h4>3.0.1  Preventing unnecessary forwarding</h4>
![Figure 1](/master_thesis/assets/img/problem.png)

 One of the side effects of the forwarder mechanism is unnecessary forwarding. Unnecessary forwarding uses network resources, which prevents the transmission from the legitimate packet. Thus, leading to performance degradation. As LPWA already offers broader coverage, the forwarder mechanism is only useful in certain conditions (see figure 1). 

Therefore, forwarders in LPWA should consider unnecessary forwarding if the gateway already receives the packet. To prevent this, we present a feedback messages like SACK acknowledgment contains all currently received packets to the relay. Therefore, relay only forward the missing packets after receiving the packets state from the network server.

<h4> 3.0.2  Reliability in uncertain wireless conditions </h4>

![Figure 2](/master_thesis/assets/img/wirelessconditions.png)

As the wireless link is unstable, figure 2 shows possible transmission and reception between end-devices, relays, and gateway. Suppose that R1 and R2 receives the message, while R3 fails due to the propagation problem. If fixed-path routing assumes that R3 is the best forwarder, the packet cannot be delivered to the destination. Thus, we require re-transmission from the sender again. However, unnecessary retransmission reduces network resources.
    
We employ opportunistic forwarding that allows any relay to forward the overheard packet by scheduling or priority mechanism to prevent packets duplication between relays. Based on the figure 2, R2 can forward the packet after notice that R3 as the higher priority fails to deliver the packet. Therefore, we can achieve better reliability and throughput compared to fixed-path forwarding.

<h4> 3.0.3  Bottle neck in opportunistic forwarding </h4>

On-demand mechanisms create a long queue in the relay that causing a bottleneck problem. Furthermore, although opportunistic forwarding improves reliability between the sender and intermediate nodes, the transmission from intermediate nodes to the gateway may fail. The network coding approach not only increases the throughput but also increases the reliability by the concept of encoding and decoding multiple packets.

<h4>3.0.4 Header overhead of RLNC in LPWA</h4>

Based on the LoRaWAN study, the available LoRaWAN payload size varies between 51-250 Bytes with the header of 13-28 Bytes depends on the data-rate settings. Because RLNC has header overhead of n log<sub>2</sub> q bits, where n is the number of packets q is bit size in GF(2<sup>q</sup>), we cannot implement RLNC directly in a massive IoT. 
    
For example, relay use GF(2<sup>4</sup>) to encode 100 packets with 30-bytes of packet size resulted in 50-bytes of header overhead in RLNC. Therefore, we adopt overhead header compression to solve packet size limitation in typical LPWA. 