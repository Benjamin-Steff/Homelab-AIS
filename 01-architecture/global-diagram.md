# 🌍 Global Network Diagram

                     INTERNET
                         │
                    Box FAI
              (192.168.X.0/24)
                         │
                 WAN – pfSense
                192.168.42.254
                         │
               ┌─────────┴─────────┐
               │                   │
              LAN               (Future DMZ)
         10.0.0.0/16
               │
        ┌──────┼───────────────┐
        │      │               │
   Windows   Windows        CrowdSec
   Server     Clients
   (AD)
