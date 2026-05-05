# Week 1 — Subnetting + VPC Design
### May 1–5, 2026

## What is Subnetting?
Subnetting is dividing your network into smaller divided networks. 
Instead of one giant network where everything talks to everything, 
you carve it up into organized, purposeful sections. Each section 
has its own range of IPs and its own job.

## What I Built This Week
- Designed multiple VPCs from scratch with different tiers (Web, App, DB, Shared, Cache) across multiple Availability Zones
- Learned how to size subnets based on purpose not just math: right sizing for today's load and tomorrow's growth
- Solved 3 rounds of VPC design problems, going from overlapping subnets in Round 1 to a perfect 15/15 in Round 3
- Read my own machine's routing table live in the terminal to understand how a routing table looks and works.
- Learned how DNS actually works end to end
- Scored 16/20 on a 20 question Week 1 quiz

## Hardest Concept
Designing multiple large cloud networks and making sure subnets didn't overlap while keeping everything scalable. The breakthrough came when I simplified it down to understanding jumps AKA
how far each subnet moves in the IP range based on its CIDR size. Once that clicked, the rest fell into place.

## My Subnetting Breakthrough
One thing that really clicked for me this week was understanding jumps and how they connect to IP counts.

Here's how I think about Subnetting now:
The highest jump you'll ever see in an octect is 128. That's your anchor.... Here is what I mean by that.

Each octet has 8 bits. Octet 1 ranges includes CIDRs from /0 to /8, Octet 2 ranges are /9 to /16, Octet 3 ranges from /17 to /24 and 4th octet ranges from /25 to /32.

So lets say you have a CIDR of /13 - We know that CIDR falls into Octet 2 and is 3 away or 3 bits away from /16 AKA the end of the Octet 2. 
To calculate the jump: 2 to the power of 3 = 8. That subnet jumps by 8 in the 2nd octet.

In other words..... in this example we have an IP: (10.0.0.0 /13) - we know /13 falls in octet #2, this octet is where the network IP will begin to change with jumps/multiples of 8.
Network 1 IP Range: 10.0.0.0 - 10.7.255.255 /13
Network 2 IP Range: 10.8.0.0- 10.15.255.255 /13
Notice how the second octect jumps by multiples of 8 when starting a new range of IPs in that subnet? It is no different if we have a subnet that has a CIDR of /20. 

/20 CIDR falls into the 3rd octect so we know that is where the change of IPs is going to happen.
Example: We have 192.168.0.0 /20 ----- We know that '/24' is the end of the third octect, how far is /20 from /24?? Now that we know we have 4 or 4 bits, use the power of 2^4 to get your jump/multiple.
2^4 = 16..... so the third octet jumps by 16.

Network 1 IP Range: 192.168.0.0 - 192.168.15.255 /24
Network 2 IP Range: 192.168.16.0 - 192.168.31.255 /24
Network 3 IP Range: 192.168.32.0 - 192.168.47.255 /24

Once I understood that, subnet math stopped feeling like memorization and started feeling like logic. I can now work out jump sizes in my head without a calculator.

This week was also partly a refresh since I already have my 
Network+ certification. But subnetting is something I always 
struggled to fully apply in real scenarios. This week I feel 
like I finally own it.

The next step is taking everything I drilled this week and 
applying it in AWS. That starts Week 2.

## Key Rules Burned In This Week
- Always place largest subnets first. Check where they end. Then place smaller ones after.
- AWS reserves 5 IPs per subnet — not 2 like standard networking.
- Switches extend networks. Routers create boundaries.
- MAC addresses move data within a network. IP addresses move data between networks.
- Longest prefix match always wins in a routing table.
- Security Groups = stateful = instance level = allow only.
- NACLs = stateless = subnet level = allow AND deny.
- 0.0.0.0/0 = the default route. The catch-all. Last resort.
- Every router-to-router link is its own subnet.
- Point-to-point links always use /30 — 2 usable IPs.
- RFC 1918 defines private IP space — the only ranges you can use internally.

## Tools Used
- Claude AI — daily concept instruction and lab grading
- subnettingpractice.com — daily drills
- AWS Skill Builder — Module 5 Networking
- My own terminal — read a live routing table
- YouTube — NetworkChuck, Fireship, Jeremy's IT Lab

## Status
Week 1 Complete. Week 2 is set to cover 'Routing: How Packets Actually Move", wish me luck! 

## See The Work
If you made it this far and want to see the actual work behind everything written above, screenshots are below. 

### VPC Designs
![VPC Design 1](images/vpc-design-1.png)
![VPC Design 2](images/vpc-design-1.2.png)
![VPC Design 3](images/vpc-design-3.png)
![VPC Design 4](images/vpc-design-4.png)
