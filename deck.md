---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
---
# Connecting the web with the web of things: lessons learned from implementing a CoAP-HTTP proxy

Lorem ipsum 

---

# Introduction 

---

# Constrained Networks
## Overview

This kind of networks are characterized by:
- High packet loss: 5 - 10% 
- Low throughput: 10 kbit/s
- Complex routing
- Low resources nodes

--- 

## 6LoWPAN

One of the enabling technologies behind the IoT trend is the IPv6 over Low power Wireless Personal Area Networks (6LoWPAN) initially developed to be used with the low power wireless standard (IEEE802.15.4). 

---
## 6LoWPAN
One of the enabling technologies behind the IoT trend is the IPv6 over Low power Wireless Personal Area Networks (6LoWPAN) initially developed to be used with the low power wireless standard (IEEE802.15.4). 

- Small packet size
- Low bandwidth
- Support for mesh topologies
- Low power requirements 

---
## M2M Communication

The devices inside these networks need to realize M2M communication. 
The ideal approach would be to extend the same architecture used for the Web and communicate through web services

---
## M2M Communication

The devices inside these networks need to communicate between each others and also with other nodes outside the network.
The ideal approach would be to extend the same architecture used for the Web and communicate through web services

But to do so we must take in count the restrictions given by the environment we are considering 

--- 

## Web protocols 
