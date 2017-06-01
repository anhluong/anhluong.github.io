---
title: "Non-invasive Breathing Monitoring"
excerpt: ""
header:
  image: 
  teaser: /assets/images/rub/IMG_3065.JPG
---

In many applications, such as search and rescue, where you want to quickly find entrapped victims in a collapsed building. With DFL, I show that it is possible to locate people. However, it would be extremely beneficial to monitor the conditions of the victims so that we could optimize rescue efforts. Breathing is normally the first indicator of vitality. Recent research has shown that we can monitor breathing with rf sensing networks. In this work, I build the first RSSI-based real-time breathing monitoring system based on the work of Kaltiokalio and his colleagues. I demonstrate this at IPSN and received a lot of feedbacks. However, I did received a lot of questions like "why not use WiFi or UWB". These are fantastic solutions, WiFi and UWB provides much better channel information compares to RSSI. However, these solutions would come with a very high cost, bandwidth and device cost. 

This inspired me to build this next system, sub-dB. On the left is the prototype I built. Traditionally, RSSI has been use as signal quality indicator for transmission. 1~dB is more than adequate. In application like breathing monitoring, gesture recognition, the changes in the channel are very small and cannot be detected with this quantization level. Thus, we would oversample and/or utilize multiple channels. In subdB, We utilize a feature provided by the TI CC1200, IQ Sample to compute our own estimated received signal strength. More details are provided in the paper and/or dissertation. In short, we were able to achieve 0.013 dB median error compared to 0.25 dB of the standard 1dB step size. In addition, we found that we reach the point of diminishing returns  for breathing monitoring with RSSI step size less than 0.625~dB or sampling rate more than 29 hz. On top of that, we were able to achieve the same perform as this paper with 6000 times less bandwidth.

[[IPSN '15 Demo](http://span.ece.utah.edu/uploads/IPSN_2015_DEMO_Breathing_print.pdf), [HotWireless '16](http://www.ece.utah.edu/~npatwari/pubs/luong2016rss.pdf)]