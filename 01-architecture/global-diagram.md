# 🌍 Global Network Diagram

```
                           INTERNET
                               │
                           Box FAI
                     (192.168.X.0/24)
                               │
                        vmbr1 (WAN)
                               │
                        pfSense (VM 100)
                        WAN: 192.168.42.254
                               │
         ┌─────────────────────┼
         │                     │                     
     vmbr2 (LAN)          (Future DMZ)
     10.0.0.0/16          
         │                     
   ┌─────┼──────────┐          
   │     │          │          
 Windows  Clients   CrowdSec   
 Server
 (AD)
```

> L’ensemble des machines virtuelles est hébergé sur Proxmox VE.
> La segmentation réseau est assurée via des bridges dédiés (vmbr).
