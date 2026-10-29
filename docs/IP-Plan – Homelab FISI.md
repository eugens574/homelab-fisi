# IP-Plan – Homelab FISI

**Netz:** 192.168.100.0/24
**Gateway (Hyper-V Host):** 192.168.100.1
**DNS/Domänencontroller:** 192.168.100.20 (srv-win01)

| Hostname | IP-Adresse | Rolle | Betriebssystem |
| :--- | :--- | :--- | :--- |
| srv-win01 | 192.168.100.20 | AD DS, DNS | Windows Server 2022 |
| srv-linux01 | 192.168.100.10 | Fileserver (Samba) | Debian 13 |
| client01 | 192.168.100.50 | Domänen-Client | Windows 11 Pro |
| Ubuntu | 192.168.100.60 | Linux Domänen-Client | Ubuntu |