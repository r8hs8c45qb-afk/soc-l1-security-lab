# Network Topology

## Network Segments

LAN Network: 192.168.128.0/24  
Gateway (pfSense LAN): 192.168.128.1  

## Hosts

- Kali Linux — Attack Simulation
- Parrot OS — Blue Team / Monitoring
- Ubuntu Server — Protected Asset

## Traffic Flow

Client → pfSense (Firewall) → WAN → Internet

This segmentation allows traffic control, monitoring, and incident simulation.
