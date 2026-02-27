# Firewall Rules

## Règles générales

- Blocage par défaut entre segments
- Autorisation contrôlée des flux nécessaires

## Flux autorisés

| Source | Destination | Action | Description |
|--------|------------|--------|-------------|
| LAN1 | WAN | Allow | Accès Internet |
| LAN2 | WAN | Allow | Mises à jour |
| LAN1 | LAN2 | Allow (admin) | Administration |
| LAN2 | LAN1 | Deny | Protection infra |
