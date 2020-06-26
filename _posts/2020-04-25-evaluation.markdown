---
layout: paper
title:  "Evaluation"
date:   2020-04-25 17:26:41 +0900
categories: bookmark
---

<h4>1. Studying LoRaWAN Reliability</h4>
![Figure 1](/master_thesis/assets/img/LBTstudy.png)

The evaluation shows that applying capture effect increase LoRa’s reliability. Furthermore, LBT-ALOHA also shows better reliability than Pure-ALOHA around 12%. LBT-ALOHA reduces collision by scanning the medium before transmission. Thus, prevent end-devices from transmitting a packet at the same time. Based on this result, we apply LBT-ALOHA with capture effect for evaluating FO and FONC approach. 


<h4>2. Increasing LoRaWAN Coverage </h4>

![Figure 2](/master_thesis/assets/img/evalcoverage.png)

In the FDR scenario, all packet forwarding mechanisms achieve more than 90% of PDR, although we increase the number of end-devices up to 1200. However, both FO and FONC perform better with around 99% of PDR compared to FP, with only around 92% of PDR. On the other hand, reliability result in SDR scenario for all mechanism is decreasing. Even when SDR scenario is used to serve hundreds of end-devices, it only gets reliability results around 88%. This result shows that the difference in transmission time between SDR and FDR scenario affect the collision probability. As more end-devices join in the contentions, LoRaWAN performance degrades faster. Especially when most of end-devices use SDR settings to provide wider range. Hence, we conclude that single star-of-stars topology in massive IoT has scalability issues because it has to rely on slow data-rate to support transmission from far away end-devices.   

<h4>3. Improving LoRaWAN Scalability </h4>

![Figure 3](/master_thesis/assets/img/adr.png)

ADR mechanism usually tends to maximize the data rate configurations to achieve faster transmission time. However, faster data rate settings increase receiver sensitivity that decreases transmission coverage. Consequently, we may not get the full benefit over multi-reception if end-device only reaches a single relay. In this paper, we present ADR comparison based on the strong/maximum RSSI and weak/minimum RSSI of relay candidates to study the best data-rate settings. Relay candidates are selected based on the possible relays that can be reached in SDR transmission

According to the results, both minADR and maxADR outperform SDR with slower performance degradation. The minADR shows better reliability compared to maxADR for below 600 number of end-devices. For FO and FONC, minADR can achieve more than 90% of PDR when serving hundreds of end-devices. It shows that multi-reception has a contribution to increasing the LoRaWAN reliability.  However, as we increase the number of end-devices, higher collisions cannot be avoided. On the other hand, maxADR shows better performance than minADR for a large number of end-devices. MaxADR on FO and FONC also shows more stable performance and degrade slower than maxADR on FP. It also shows the benefit over multi-reception because several end-devices still reach both relay candidates, although using maxADR approach. 


<h4>4. Preventing Unnecessary Forwarding</h4>
![Figure 4](/master_thesis/assets/img/unnecessaryre.png)

![Figure 5](/master_thesis/assets/img/unnecessaryam.png)

The reasons behind the performance degradation in fixed-path are unnecessary forwarding. Both FO and FONC succeed in suppressing unnecessary transmission because of the feedback-based mechanism. Moreover, both relays can coordinate each other to suppress the duplicate packet between relay forwarding. On the other hand, fixed-path forwarding suffers from performance degradation because of packet collisions, caused by unnecessary forwarding. In FDR scenario, the number of unnecessary forwarding is stable around 38%-44% because of low packet collision. If we look at the reliability performance and the number of unnecessary forwarding, we can assume that fixed-path relay forwarding may increase the reliability by unnecessary forwarding. However, evaluation in SDR scenario shows low performance. The number of unnecessary forwarding also degrades because of packet collision. 