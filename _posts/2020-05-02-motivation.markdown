---
layout: paper
title:  "Motivation"
date:   2020-05-04 17:26:41 +0900
categories: bookmark
---

<h4>3.0.1  Preventing unnecessary forwarding</h4>

One of the side effects of the forwarder mechanism is unnec-essary  forwarding.  Unnecessary  forwarding  uses  networkresources,  which  prevents  the  transmission  from  the  legit-imate  packet.  Thus,  leading  to  performance  degradation.As  LPWA  already  offers  broader  coverage,  the  forwardermechanism  is  only  useful  in  certain  conditions  (see  figure1). Therefore, forwarders in LPWA should consider unneces-sary forwarding if the gateway already receives the packet.To  prevent  this,  we  present  an  on-demand  mechanism  bysuch  feedback  messages  like  SACK  acknowledgment  con-tains  all  currently  received  packets  to  the  relay.  Therefore,relay  only  forward  the  missing  packets  after  receiving  thepackets state from the network server.

<h4> 3.0.2  Reliability in uncertain wireless conditions </h4>

Fig. 3: Uncertainty of wireless environmentAs the wireless link is unstable, figure 3 shows possibletransmission  and  reception  between  end-devices,  relays,and gateway. Suppose that R1 and R2 receives the message,while R3 fails due to the propagation problem. If fixed-pathrouting  assumes  that  R3  is  the  best  forwarder,  the  packetcannot be delivered to the destination. Thus, we require re-transmission from the sender again. However, unnecessaryretransmission reduces network resources.We  employ  opportunistic  forwarding  that  allows  anyrelay  to  forward  the  overheard  packet  by  scheduling  orpriority mechanism to prevent packets duplication betweenrelays.  Based  on  the  figure  3,  R2  can  forward  the  packetafter  notice  that  R3  as  the  higher  priority  fails  to  deliverthe packet. Therefore, we can achieve better reliability andthroughput compared to fixed-path forwarding.

<h4> 3.0.3  Bottle neck in opportunistic forwarding </h4>

On-demand  mechanisms  create  a  long  queue  in  the  relaythat  causing  a  bottleneck  problem.  Furthermore,  althoughopportunistic  forwarding  improves  reliability  between  thesender  and  intermediate  nodes,  the  transmission  from  in-termediate  nodes  to  the  gateway  may  fail.  The  networkcoding approach not only increases the throughput but alsoincreases  the  reliability  by  the  concept  of  encoding  anddecoding multiple packets.

<h4>Header overhead of RLNC in LPWA</h4>

Based  on  the  LoRaWAN  study  [7,  33],  the  available  Lo-RaWAN payload size varies between 51-250 Bytes with theheader  of  13-28  Bytes  depends  on  the  data-rate  settings.Because RLNC has header overhead ofn log2qbits, wheren is the number of packets q is bit size inGF(2q, we cannotimplement RLNC directly in a massive IoT.For  example,  relay  useGF(24)to  encode  100  pack-ets  with  30-bytes  of  packet  size  resulted  in  50-bytes  ofheader  overhead  in  RLNC.  Therefore,  we  adopt  overheadheader compression to solve packet size limitation in typical LPWA