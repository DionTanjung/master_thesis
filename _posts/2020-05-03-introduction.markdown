---
layout: paper
title:  "Introduction"
date:   2020-05-04 17:26:41 +0900
categories: bookmark
---
LPWA technologies have gain more attention in various IoT service as it provides long transmission range between devices to devices with low power consumption. Compared to WiFi and Bluetooth that use 2.4-GHz for short-range com-munication, LPWA works on the  sub-GHz band, allowinglonger transmission range up to 20km in LOS. Although thedata rate is only 0.3 kbit/s to 50 kbit/s [1], it enough for IoT applications such as smart  city or telemetry services thatsend small packet over wider coverage.

There are several LPWA technologies provided in the market based on licensed band  (LTE-M [2] and NB-IoT[3]) and unlicensed band(Sigfox[4] and LoRa[5]). Amongthem, LoRa or long-range radio, using a CSS (Chirp Spread Spectrum) modulation technique, is a popular LPWA radiotechnology adopted worldwide. LoRaWAN[6] is a MAClayer specification to build a network based on LoRa radio.As LoRaWan is an open standard, it becomes  popular because allowing researchers and developers to improve and modify the specification to their needs.

 LoRaWAN adopts a one-hop star-of-star topology where an end-device transmits its packet to one or more gateways by LoRa modulation. Gateways linked with internet access to forward the packet to the network server via IP connection. To extend coverage in this simple topology, LoRaWAN utilize data-rate settings based on spreading factor SF (7-12) and Bandwidth BW (125 kHz, 250 kHz, and 500 kHz)[6]. As we increase the SF and decrease the BW, we can achieve longer coverage. However, this approach still suffers from coverage and reliability issues. 

 Many researchers have studied LoRa performance under this topology. Field test in [7] shows that SF 12 is required to achieve 90\% of PDR in the coverage below 3 km. However, the scalability test in [8] tells that LoRa can only support 120 number of end-devices using this lower data rate settings. This low scalability performance is not surprising because LoRa transmission is based on the Aloha protocol.