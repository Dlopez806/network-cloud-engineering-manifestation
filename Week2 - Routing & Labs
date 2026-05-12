# Week 2 — Routing Protocols + GNS3 Lab
### May 11–15, 2026

## What I Learned This Week
This week I went from understanding routing in theory to actually 
building a working multi-router network with my own hands. Spoiler: 
it broke. Multiple times. And that ended up being the best part.

## The Concepts
There are 3 ways a router learns about networks:
- **Directly connected** — physically plugged in, no setup needed
- **Static routes** — a human manually types them
- **Dynamic routing protocols** — routers talk to each other and 
  share what they know automatically

Two main dynamic protocols I learned about:
- **OSPF** — used INSIDE a company. Routers share a complete map 
  of the network with each other and calculate the shortest path 
  to every destination.
- **BGP** — used BETWEEN companies. This is literally what holds 
  the internet together. Every ISP, every cloud provider speaks 
  BGP. It's policy-driven, not distance-driven, meaning it picks 
  paths based on business rules and contracts, not just shortest 
  distance.

Key thing that stuck with me: OSPF is called an IGP (Interior 
Gateway Protocol), BGP is called an EGP (Exterior Gateway Protocol). 
Interior = inside your network. Exterior = between networks.

## The Lab — Building 3 Routers with OSPF
Spent way longer than expected getting GNS3 set up. Learned a 
ton about VMs, NAT vs Host-Only adapters, DHCP servers, and why 
binding to localhost vs a network IP matters. None of that was 
in the original plan but I'm honestly glad it happened.

Once GNS3 was running I built this topology:
