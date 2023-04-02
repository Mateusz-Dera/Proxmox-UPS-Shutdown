# Proxmox UPS Shutdown
## Info:
- A simple systemd service that shuts down all virtual machines and containers if the UPS battery level drops below a specified percentage value.
- [![Version](https://img.shields.io/badge/0.4_Alpha-Current_Version-green.svg)](https://github.com/Mateusz-Dera/https://github.com/Mateusz-Dera/Proxmox-UPS-Shutdown)
## Installation:
```
wget -P /etc/systemd/system/ https://raw.githubusercontent.com/Mateusz-Dera/Proxmox-UPS-Shutdown/main/proxmox-ups.service
wget -P /bin/ https://raw.githubusercontent.com/Mateusz-Dera/Proxmox-UPS-Shutdown/main/proxmox-ups
wget -P /bin/ https://raw.githubusercontent.com/Mateusz-Dera/Proxmox-UPS-Shutdown/main/proxmox-shutdown
chmod +x /bin/proxmox-ups
chmod +x /bin/proxmox-shutdown
systemctl daemon-reload
systemctl enable proxmox-ups
systemctl start proxmox-ups
```