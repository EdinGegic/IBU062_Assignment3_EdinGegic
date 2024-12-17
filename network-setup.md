# Network Setup Documentation

## Devices in the Network

### Router:
- Model: Cisco 1941
- Interfaces: 
  - GigabitEthernet0/0: 168.90.0.1/16
  - GigabitEthernet0/1: 210.3.14.1/24

### Switches:
- Switch 1: Cisco Catalyst 2960
- Switch 2: Cisco Catalyst 2960

### Devices Connected to Switch 1:
- PC1: IP Address: 168.90.0.2 (assigned by DHCP)
- PC2: IP Address: 168.90.0.3 (assigned by DHCP)
- Laptop: IP Address: 168.90.0.4 (assigned by DHCP)
- Server1: IP Address: 168.90.0.5 (assigned by DHCP)
- PC4: IP Address: 168.90.0.6 (assigned by DHCP)

### Devices Connected to Switch 2:
- PC3: IP Address: 210.3.14.2 (assigned by DHCP)
- Server2: IP Address: 210.3.14.3 (assigned by DHCP)
- PC5: IP Address: 210.3.14.4 (assigned by DHCP)

## DHCP Configuration on Router

### DHCP Pool for Network 168.90.0.0/16 

Router(config)# ip dhcp pool LAN1
Router(config-dhcp)# network 168.90.0.0 255.255.0.0
Router(config-dhcp)# default-router 168.90.0.1
Router(config-dhcp)# dns-server 168.90.0.1
Router(config-dhcp)# exit

### DHCP Pool for Network 210.3.14.0/24
Router(config)# ip dhcp pool LAN2
Router(config-dhcp)# network 210.3.14.0 255.255.255.0
Router(config-dhcp)# default-router 210.3.14.1
Router(config-dhcp)# dns-server 210.3.14.1
Router(config-dhcp)# exit
