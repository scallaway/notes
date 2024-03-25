# Setup

## Firewall rules

### Network Isolation

If you want to maintain as much network isolation as possible, then a secure
way to set this up is through the following two rules:

1. A rule that allows access to the DNS server on the LAN interface
  - Interface -> LAN
  - Protocol -> TCP/UDP
  - Source -> LAN net
  - Destination -> LAN address
  - Destination port range -> from: DNS

2. A rule that passes through connections that _aren't_ on the network that
   you're trying to secure
  - Interface -> LAN
  - Source -> LAN net
  - Destination/Invert -> checked
  - Destination -> {your alias}

ENSURE THAT THE DNS ENTRY IS FIRST IN THE LIST!
