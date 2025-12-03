# Lab 5 — Ping & Traceroute Network Mapping

## Purpose
This lab helps me understand how my computer reaches external websites by using the `ping` and `tracert` commands. It shows the network hops between my device, my router, my ISP, and the target website. This is useful for diagnosing network slowdowns and connectivity issues.

## Tools Used
- Windows 11
- Command Prompt
- Draw.io (for network diagram)

## Steps Taken

### 1. Testing Connectivity with Ping
I used the `ping` command to test basic connectivity:
- `ping 8.8.8.8` (Google DNS)
- `ping google.com`
- `ping cloudflare.com`

This helped me confirm whether DNS and internet connectivity were functioning properly.

### 2. Using Traceroute to Map Network Hops
I ran the following commands:

`tracert google.com`  
`tracert cloudflare.com`  
`tracert openai.com`

I recorded:
- Number of hops
- Latency at each hop
- Points where latency increased

### 3. Identifying Local Network Hop
In every traceroute, the first hop is my **default gateway** (my router):
Example:
`192.168.x.x`

This confirms that my device can reach the local network.

### 4. Creating a Simple Network Diagram
I drew a simple map showing:
- My device  
- My router  
- My ISP  
- Intermediate hops  
- Final destination (Google / Cloudflare / OpenAI)

The diagram is saved in the `diagram` folder.

## Screenshots
Screenshots are saved in the `screenshots` folder:
1. Ping to 8.8.8.8  
2. Ping to google.com  
3. Traceroute to google.com  
4. Traceroute to cloudflare.com  
5. Traceroute to openai.com  

## What I Learned
- How to use `ping` to test DNS and network connectivity  
- How traceroute shows the path traffic takes across the internet  
- How to identify local vs external network issues  
- How latency increases over distance and number of hops  
- How to document and visualise network paths  
