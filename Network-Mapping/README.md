# Lab 5 — Ping & Traceroute Network Mapping

## Purpose

The purpose of this lab is to demonstrate how to test network connectivity and analyse network paths using the `ping` and `tracert` commands. These tools are used to identify whether connectivity issues occur on the local network, at the ISP level, or further along the route to an external destination. This is a core troubleshooting skill used in IT support and networking roles.

---

## Tools Used

- Windows 11  
- Command Prompt  
- Draw.io (for network diagram)

---

## Steps Performed

### 1. Tested Network Connectivity Using Ping

I used the `ping` command to test basic network and DNS connectivity:
"ping 8.8.8.8"
"ping google.com"
"ping cloudflare.com"

These tests confirmed:
- The local network was reachable
- DNS resolution was functioning correctly
- The system could successfully communicate with external internet hosts

---

### 2. Mapped Network Hops Using Traceroute

I ran the following traceroute commands to analyse the network path to multiple external destinations:
"tracert google.com"
"tracert cloudflare.com"
"tracert openai.com"

From the output, I recorded:
- The total number of hops
- Latency values at each hop
- Points where latency increased significantly

This helped identify where delays occurred along the network path.

---

### 3. Identified the Local Network Gateway

In each traceroute result, the first hop was identified as the default gateway (local router), for example:
"192.168.x.x"

This confirmed that the device was correctly communicating with the local network before traffic was routed externally.

---

### 4. Created a Simple Network Diagram

Using Draw.io, I created a simple network diagram showing:
- My local device
- The home router (default gateway)
- The ISP
- Intermediate network hops
- The final destination (Google / Cloudflare / OpenAI)

The diagram is saved in the `diagram` folder.

---

## Screenshots

All screenshots are stored in the `screenshots` folder and include:

1. Ping to 8.8.8.8  
2. Ping to google.com  
3. Traceroute to google.com  
4. Traceroute to cloudflare.com  
5. Traceroute to openai.com  

---

## What I Learned

- How to use `ping` to test basic network and DNS connectivity  
- How `tracert` displays the path traffic takes across the internet  
- How to distinguish between local and external network issues  
- How latency increases over distance and number of hops  
- How to document and visualise network paths for troubleshooting purposes  

---

## Why This Lab Matters

Ping and traceroute are essential tools for diagnosing network issues in real-world IT environments. They are commonly used to identify slow connections, routing problems, and service outages, making them fundamental skills for IT support and networking roles.
