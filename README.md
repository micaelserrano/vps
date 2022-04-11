# Bypassing a CGNAT with tailscale

## Overview
Before switching ISPs, I had a public IP that allowed me to use port forwarding on my router to pass traffic to services hosted on my internal network. 
My new ISP uses a CGNAT, so I had to find a workaround. I chose this path, because it keeps pretty much everything the same for my services.  
The main things I wanted to do with my setup were:
* Forward only traffic from the internet to my services.
* Provide my NPM (Nginx Proxy Manager) Server with clients real IPs (for fail2ban blocking purposes)
* Allow for traffic to flow to internal services that NPM doesn't manage
* Make my services egress traffic only via my own network and not via the cloud provider
