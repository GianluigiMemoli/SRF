---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
---

# Dynamic Aggregation and Scheduling in CoAP/Observe-Based Wireless Sensor Networks


---
## The IoT revolution 

The possibility of organizing an high number of sensors inside a network led to the opening of new perspectives among different fields (manifacturing, smart metering, e-health etc.).

---

### Enabling technologies 
The innovation is made possible by several key technologies:
- Cloud computing
- 6LoWPAN
- Protocols for constrained networks
[fig.1]

---

## Constrained Application Protocol
CoAP has been designed for constrained networks. 
- Built on top of UDP
- Reduced message overhead
- Based on REST architecture
- Less resource usage compared to HTTP

---

### CoAP/Observe
An extension that allow to introduce a publish/subscribe mechanism, giving the possibility of observe resource changes to the clients. 
- No polling to the servers
- Notifications on resource changes

---

### Observing resources
Observers must register separately to each subject of a CoAP server. 
The notifications may be:
- periodic (NON)
- threshold based (CON)


---

### Observing resources - Multiple registration steps
![bg contain](img/fig1.png)

---

### Observing resources - Optimization issues
- Energy
- Consistency
- Registrations and caching

Congestion control: 
- No more than one NON notification per RTT
- Wait for ack of a single CON
---
# Aggregation and scheduling 
## Definitions - Nodes 
- $N$: The set of WSN **Nodes**
- $N^S\subset N$: The set of **sources**
- $N^D\subset N$: The set of **destinations**
In a M2M $N^D$ will include each WSN node, in a monitoring application will contain the edge routers (connected to the Internet) only
---
## Definitions - Transmission plan
A node can have a transmission plan, containing a set of observation requests.
- $p^k_{n_i}$: A transmission plan at node $n_i$ 

The period, after all plan's data have been received, during which plan's data will be transmitted is defined **Transmission Window** of a plan.

---

## Definitions - Transmission plan window
Given the plan at node $n_i$ denoted $p^k_{n_i}$
- $W^L(p^k_{n_i}) \geq 0$: **Lower bound**
- $W^H(p^k_{n_i}) \geq 0$: **Upper bound**
- $T^{min}$: time that 1B takes to be transmitted

$W^L(p^k_{n_i})$ is the moment when all notifications are available

$W^H(p^k_{n_i})$ is the moment when all notifications have been sent out

