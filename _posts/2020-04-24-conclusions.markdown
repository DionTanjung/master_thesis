---
layout: paper
title:  "Conculusions"
date:   2020-04-24 17:26:41 +0900
categories: bookmark
---

In this thesis, we present feedback based opportunistic forwarding (FO) and feedback based opportunistic forwarding with network coding (FONC) as a forwarder mechanism to increase the LoRaWAN coverage, reliability, and scalability with better transmission efficiency. We propose this approach to overcome the limitation of one-hop star-of-stars in providing scalable long-range communication. Compared to the previous studies, we consider unnecessary forwarding as one of the drawbacks of a typical relay forwarder. In our mechanism, relay only forward when the packet is lost due to coverage limitation or obstacle problem (both temporal and permanent) that blocked a direct transmission to the gateway. 
Both FO and FONC show better reliability performance in increasing network coverage and suppressing unnecessary transmission compared to fixed-path forwarding. The multi-reception approach, feedback message, and network coding is the main mechanism to improve reliability. Whereas, the feedback approach prevents unnecessary forwarding. In fast data rate settings, the reliability is still stable around 99% for traffic load G=2.1 (1200 number of end-devices). On the other hand, the performance in slow data rate degrades faster. We present minimum RSSI and maximum RSSI based adaptive data rate (ADR) to overcome the scalability issue in LoRa network. The result shows that minADR selection gives better performance for end-devices below 600 owing to exploitation on multi-reception. Otherwise, maxADR is preferred because the result is more stable above 70% although we increase the end-device up to 1200.  
