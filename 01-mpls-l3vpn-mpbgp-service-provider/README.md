
# MPLS L3VPN Service Provider Network using OSPF, MPLS LDP and MP-BGP

## Overview

This project demonstrates the implementation of a Service Provider MPLS Layer 3 VPN architecture using Cisco IOSv and MikroTik CHR routers in GNS3.

The lab simulates a real-world ISP environment where multiple customer networks share the same provider backbone while remaining logically isolated through VRF segmentation.

The provider core uses OSPF Area 0 as the Interior Gateway Protocol (IGP), MPLS LDP for label distribution, and MP-BGP VPNv4 for VPN route exchange between Provider Edge (PE) routers.

---

## Objectives

* Build an MPLS-enabled Service Provider backbone
* Configure OSPF Area 0 across provider routers
* Enable MPLS and LDP label distribution
* Configure MP-BGP VPNv4 sessions between PE routers
* Implement VRFs for customer isolation
* Connect multiple customer sites across the MPLS backbone
* Verify end-to-end connectivity between customer branches

---

## Technologies Used

### Routing Protocols

* OSPF Area 0
* MP-BGP VPNv4

### MPLS Technologies

* MPLS
* LDP
* VRF

### Platforms

* Cisco IOSv
* MikroTik CHR
* GNS3

### Networking Concepts

* Service Provider Architecture
* Customer Edge (CE)
* Provider Edge (PE)
* Provider Core (P)
* Route Distinguishers (RD)
* Route Targets (RT)

---

## Network Architecture

Customer Networks:

* BANK_A
* BANK_B
* BANK_C

Provider Components:

* PE1
* PE2
* PE3
* PE4

Core Components:

* P1
* P2
* P3
* P4

Provider AS:

AS65000

---

## MPLS Core Design

The provider backbone uses OSPF Area 0 for loopback reachability.

All core links participate in MPLS LDP to distribute labels across the network.

MPLS forwarding allows traffic to traverse the provider network without exposing customer routes inside the core.

---

## MP-BGP VPNv4 Implementation

MP-BGP VPNv4 sessions are established between PE routers.

Responsibilities:

* Exchange VPNv4 routes
* Preserve customer route separation
* Distribute VRF information
* Maintain end-to-end VPN connectivity

---

## VRF Segmentation

Each customer network is assigned to a dedicated VRF.

Benefits:

* Overlapping IP support
* Traffic isolation
* Multi-tenant architecture
* Secure customer separation

---

## Verification

### OSPF Adjacencies

Verified full OSPF neighbor relationships across provider core routers.

### MPLS LDP

Verified MPLS label exchange between all provider routers.

### MP-BGP

Verified VPNv4 route exchange between PE routers.

### End-to-End Reachability

Successfully tested:

* Bank A to Bank A remote site
* Bank B to Bank B remote site
* Bank C to Bank C remote site

ICMP success rate:

100%

---

## Key Learnings

* MPLS forwarding architecture
* Label distribution using LDP
* MP-BGP VPNv4 route exchange
* VRF implementation
* Service Provider network design
* End-to-end VPN troubleshooting

---

## Future Enhancements

* MPLS Traffic Engineering
* RSVP-TE
* BGP Route Reflectors
* Dual-homed customer connectivity
* EVPN/VXLAN integration
* Segment Routing MPLS
* MPLS Fast Reroute
---

## Author

**Mohammad Sajjad**
**Network Engineer | CCNA & DevNet Certified | Aspiring Cloud Network Automation Engineer**
