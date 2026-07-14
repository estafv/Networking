## DNS (Domain Name System)

**DNS** translates **domain names** (e.g., `google.com`) into **IP addresses**, allowing computers to find and connect to websites. Think of DNS as the **Internet's phonebook**.

**Example:**
```text
youtube.com → 142.x.x.x
```

### Key Facts
- 🌐 Resolves domain names to IP addresses.
- 📡 Uses **Port 53** (TCP/UDP).
- 🔍 `nslookup` is used to look up a domain's IP address.
- 📝 Local DNS entries can be added in `/etc/hosts`.
- ⚙️ DNS servers are configured in `/etc/resolv.conf` (Linux).

### Common Top-Level Domains (TLDs)

| TLD | Purpose |
|:---:|---------|
| `.com` | Commercial |
| `.edu` | Educational |
| `.gov` | Government |
| `.mil` | Military |
| `.net` | Networks / ISPs |
| `.org` | Organizations |
| `.int` | International Organizations |
| `.arpa` | DNS infrastructure |

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
| **CNAME** | Alias for another domain |
| **MX** | Mail server |
| **NS** | Authoritative name server |
| **TXT** | Stores text information (verification, security, etc.) |
