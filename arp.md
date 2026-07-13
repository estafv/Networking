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
>
> ---
>
> # ARP Process: Same Network Communication
>
> ## Scenario
>
> Host B wants to communicate with Host A.
>
> - Host B already knows Host A's IP address.
> - Host B does not know Host A's MAC address.
>
> ## Steps
>
> 1. Host B creates an **ARP Request** asking:
>
>    "Who owns this IP address? Send me your MAC address."
>
> 2. The ARP Request is sent as a **broadcast**, meaning every device on the local network receives it.
>
> 3. Each device checks the requested IP address:
>    - If the IP does not match, the device ignores the request.
>    - If the IP matches, the device responds.
>
> 4. Host A sends an **ARP Reply** back to Host B containing its MAC address.
>
> 5. Host B saves the IP-to-MAC mapping inside its **ARP Table/Cache** so it does not have to ask again.
>
> ## Key Rule
>
> If the destination is on the **same network**, ARP finds the destination device's MAC address.
>
> ---
>
> # ARP Process: Different Network Communication
>
> ## Scenario
>
> Host B wants to communicate with a device on another network.
>
> - The destination is outside of the local network.
> - The traffic needs to go through a router.
>
> ## Default Gateway
>
> - The default gateway is the router that connects the local network to other networks.
> - Host B does not need the remote device's MAC address.
> - Instead, Host B needs the router's MAC address.
>
> ## Steps
>
> 1. Host B checks the destination IP address.
>
> 2. Host B determines the destination is on a different network.
>
> 3. Host B sends an ARP Request for the **default gateway's IP address**.
>
> 4. The router responds with its MAC address.
>
> 5. Host B stores the router's IP-to-MAC mapping in the ARP table.
>
> 6. Host B sends the traffic to the router, and the router forwards it to the destination network.
>
> ## Key Rule
>
> If the destination is on a **different network**, ARP finds the default gateway's MAC address, not the destination device's MAC address.
>
> ---
>
> # Terms to remember
>
> - ARP = IP address → MAC address mapping
> - ARP Request = Broadcast (`FF:FF:FF:FF:FF:FF`)
> - ARP Reply = Unicast response
> - ARP mappings are stored in the ARP Table/Cache
> - ARP only works on the local network
> - Local destination → ARP for the target device
> - Remote destination → ARP for the default gateway
