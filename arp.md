# ARP (Address Resolution Protocol)

Mapping of a L3 address to a L2 address

ARP is used when the IP address of a device is known, but the MAC address needs to be discovered for communication on the local network.

<img width="800" height="493" alt="image" src="https://github.com/user-attachments/assets/4b30ed62-047d-4492-a73e-dc41d5c54ec2" />

> [!NOTE]
> # ARP (Address Resolution Protocol)
>
> ARP is a network protocol used to map a **Layer 3 (IP) address** to a **Layer 2 (MAC) address**.
>
> - When using ARP, the **IP address is already known**.
> - The goal is to discover the device's **MAC address**.
> - ARP allows devices on the same network to communicate by finding the correct hardware address.
>
> ---
>
> ## ARP Process: Same Network Communication
>
> **Scenario:**
>
> - Host B wants to communicate with Host A.
> - Host B knows Host A's IP address.
> - Host B does not know Host A's MAC address.
>
> **Steps:**
>
> 1. Host B sends an **ARP Request**.
> 2. The request asks:
>
>    "Who has this IP address? Send me your MAC address."
>
> 3. The ARP Request is sent as a **broadcast** to all devices on the local network.
> 4. All devices receive the request, but only the device with the matching IP responds.
> 5. Host A sends an **ARP Reply** containing its MAC address.
> 6. Host B stores the IP-to-MAC mapping in its **ARP Table/Cache**.
>
> **Rule:**
>
> Same network → ARP discovers the destination device's MAC address.
>
> ---
>
> ## ARP Process: Different Network Communication
>
> **Scenario:**
>
> - Host B wants to communicate with a device on another network.
> - The traffic must pass through a router.
>
> **Steps:**
>
> 1. Host B checks the destination IP address.
> 2. Host B determines the destination is on a different network.
> 3. Instead of finding the remote device's MAC address, Host B finds the **default gateway's MAC address**.
> 4. Host B sends an ARP Request for the router's IP address.
> 5. The router replies with its MAC address.
> 6. Host B stores the gateway's IP-to-MAC mapping in its ARP table.
> 7. Traffic is sent to the router, which forwards it to the remote network.
>
> **Rule:**
>
> Different network → ARP discovers the default gateway's MAC address.
>
> ---
>
> ## Important Concepts
>
> - ARP Request = **Broadcast** (`FF:FF:FF:FF:FF:FF`)
> - ARP Reply = **Unicast**
> - ARP mappings are stored in an **ARP Table/Cache**
> - ARP only works on the **local network**
> - Local destination → ARP for the target device
> - Remote destination → ARP for the default gateway
