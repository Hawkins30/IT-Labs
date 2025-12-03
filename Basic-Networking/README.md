
This displayed:
- DNS servers  
- DHCP server  
- Complete network configuration  

### 3. Checking Network Settings (GUI)
I opened:
**Settings → Network & Internet → Properties (on active network)**

This showed:
- Connection type  
- IPv4 address  
- Gateway  
- DNS server  

### 4. Testing Internet Connectivity
I used the following commands:

`ping 8.8.8.8` — Tests connection to Google DNS  
`ping google.com` — Tests DNS and internet connection  

### 5. Testing Gateway Reachability
I pinged my gateway:

`ping <gateway IP>`  
(e.g., `ping 192.168.1.1`)

If the gateway responds, the local network is working.

## Screenshots
Screenshots are included in the `screenshots` folder:
1. `ipconfig` output  
2. `ipconfig /all` showing DNS  
3. Network & Internet Properties window  
4. Successful ping to 8.8.8.8  
5. Successful ping to google.com  
6. Ping to gateway  

## What I Learned
- How to find my IP address, DNS servers, and gateway  
- The difference between internal LAN connectivity and internet connectivity  
- How DNS works and how to test if it’s failing  
- How to troubleshoot basic network problems using ping and ipconfig  
