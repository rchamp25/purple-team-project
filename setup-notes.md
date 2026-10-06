# Lab Setup Notes

## Environment
- Host: Windows 11, 16 GB RAM
- Docker Desktop (WSL2 backend)
- VirtualBox 7.2.20

## Docker Targets
- Juice Shop: host port 3000
- DVWA: host port 8080
- Both currently bound to `127.0.0.1` (localhost only)

## Host-Only Network
- Name: VirtualBox Host-Only Ethernet Adapter (shows up as Ethernet 2 on my pc)
- Host (my PC) address: 192.168.56.1/24
- DHCP server: 192.168.56.100
- DHCP pool: 192.168.56.101 - 192.168.56.254

### Why a host-only network?
- We are usign deliberately vulnerable apps and attack tools so we want to guarentee that nothing outside can touch the lab and nothing inside the lab can reach outside. 

## Gotchas
- VirtualBox 7.2 doesn't list Network Manager in the Tools menu. It's the
  Network icon in the left sidebar, which also works as a shortcut (Ctrl+H).
- The installer had already created a host-only network, so I didn't need to make one.