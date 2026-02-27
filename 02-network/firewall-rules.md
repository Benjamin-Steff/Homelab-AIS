# Firewall Rules

L’ensemble du filtrage est centralisé sur pfSense.
La politique appliquée est basée sur le principe : *autoriser uniquement ce qui est nécessaire*.

---

## WAN Rules

| Action | Protocol | Source | Destination | Port | Description |
|--------|----------|--------|------------|------|------------|
| Block  | *        | Bogon networks | Any | * | Block bogon networks |
| Allow  | UDP      | Any    | WAN address | 1194 | OpenVPN remote access |

---

## LAN Rules

| Action | Protocol | Source | Destination | Description |
|--------|----------|--------|------------|------------|
| Allow  | *        | LAN address | 443, 80, 9922 | Anti-lockout rule |
| Allow  | IPv4     | LAN subnets | Any | Default allow LAN to any |
| Allow  | IPv6     | LAN subnets | Any | Default allow LAN IPv6 |

---

## OpenVPN Rules

| Action | Protocol | Source | Destination | Description |
|--------|----------|--------|------------|------------|
| Allow  | IPv4     | Any | Any | OpenVPN remote-access wizard |

---

## Diagram – Current Firewall Configuration

![Firewall Rules](../assets/diagrams/firewall-rule.png)
