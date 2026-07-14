# ARP (Address Resolution Protocol)

Mapping of a L3 address to a L2 address

ARP is used when the IP address of a device is known, but the MAC address needs to be discovered for communication on the local network.

<img width="800" height="493" alt="image" src="https://github.com/user-attachments/assets/4b30ed62-047d-4492-a73e-dc41d5c54ec2" />

> # Terms to remember
> - ARP = IP address → MAC address mapping
> - ARP Request = Broadcast (`FF:FF:FF:FF:FF:FF`)
> - ARP Reply = Unicast response
> - ARP mappings are stored in the ARP Table/Cache
> - ARP only works on the local network
> - Local destination → ARP for the target device
> - Remote destination → ARP for the default gateway
