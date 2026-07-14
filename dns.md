## DNS (Domain Name System)

A **DNS (Domain Name System)** converts a **domain name** into an **IP address** allowing your device to locate and connect to the correct server. Since computers communicate using IP addresses rather than names DNS acts as the translator between the two.

**Example:**
```text
youtube.com → 142.x.x.x
```

### Key Facts
- Converts domain names into IP addresses.
- Uses **Port 53** over both **TCP** and **UDP**.
- `nslookup` is used to retrieve the IP address of a domain.
- Local DNS mappings can be added to `/etc/hosts`.
- On Linux, DNS servers are configured in `/etc/resolv.conf`.

### Common Domains (TLDs)

| TLD | Purpose |
|:---:|---------|
| `.com` | Commercial websites |
| `.edu` | Educational institutions |
| `.gov` | Government agencies |
| `.mil` | Military organizations |
| `.net` | Network providers and ISPs |
| `.org` | Organizations and non profits |
| `.int` | International organizations |
| `.arpa` | DNS and network infrastructure |

### Domain Structure

```text
www.sub.domain.com
│    │    │      └── Top-Level Domain (TLD)
│    │    └───────── Domain
│    └────────────── Subdomain
└─────────────────── Host
```

### Common DNS Record Types

| Record | Purpose |
|:------:|---------|
| **A** | Maps a domain to an IPv4 address |
| **AAAA** | Maps a domain to an IPv6 address |
| **CNAME** | Creates an alias for another domain |
| **MX** | Specifies the mail server for a domain |
| **NS** | Identifies the authoritative name server |
| **TXT** | Stores text-based information such as verification or security records |
