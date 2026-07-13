# ARP (Address Resolution Protocol)

Mapping of a L3 address to a L2 address

ARP is used when the IP address of a device is known, but the MAC address needs to be discovered for communication on the local network.

<img width="800" height="493" alt="image" src="https://github.com/user-attachments/assets/4b30ed62-047d-4492-a73e-dc41d5c54ec2" />

> [!NOTE]
> # ARP (Address Resolution Protocol)
>
> ARP is a protocol used to find the **MAC address** of a device when you already know its **IP address**.
>
> - ARP works by mapping a **Layer 3 (IP) address** to a **Layer 2 (MAC) address**.
> - The IP address is already known, but the MAC address is what we need to discover.
> - This allows devices on the same network to communicate with each other.

> # Terms to remember
>
> - ARP = IP address → MAC address mapping
> - ARP Request = Broadcast (`FF:FF:FF:FF:FF:FF`)
> - ARP Reply = Unicast response
> - ARP mappings are stored in the ARP Table/Cache
> - ARP only works on the local network
> - Local destination → ARP for the target device
> - Remote destination → ARP for the default gateway
