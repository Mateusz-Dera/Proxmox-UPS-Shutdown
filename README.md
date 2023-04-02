# Proxmox UPS Shutdown
## Info:
- A simple systemd service that shuts down all virtual machines and containers if the UPS battery level drops below a specified percentage value.
- [![Version](https://img.shields.io/badge/0.5.4_Alpha-Current_Version-green.svg)](https://github.com/Mateusz-Dera/https://github.com/Mateusz-Dera/Proxmox-UPS-Shutdown)
## Installation:
```
curl -o /etc/systemd/system/proxmox-ups.service -L -O https://raw.githubusercontent.com/Mateusz-Dera/Proxmox-UPS-Shutdown/main/proxmox-ups.service
curl -o /bin/proxmox-ups -L -O https://raw.githubusercontent.com/Mateusz-Dera/Proxmox-UPS-Shutdown/main/proxmox-ups
curl -o /bin/proxmox-shutdown -L -O https://raw.githubusercontent.com/Mateusz-Dera/Proxmox-UPS-Shutdown/main/proxmox-shutdown
```

Edit configuration in /bin/proxmox-ups file

```
chmod +x /bin/proxmox-ups
chmod +x /bin/proxmox-shutdown
systemctl daemon-reload
systemctl enable proxmox-ups
systemctl start proxmox-ups
```
