# Homelab – Kleines Firmennetz mit Hyper-V

## Projektziel
Aufbau einer Mini-Infrastruktur in Hyper-V zur Übung typischer Aufgaben eines Fachinformatikers für Systemintegration. Der Fokus lag auf Active Directory, DHCP, DNS, Filesharing und der Integration heterogener Betriebssysteme (Windows & Linux).

## Umgebung
- **Host:** Windows 11 mit Hyper-V
- **Netzwerk:** Interner Hyper-V-Switch `LAB-Intern` (192.168.100.0/24) mit NAT für Internetzugriff
- **VMs:** 
  - Windows Server 2022 (Domänencontroller)
  - Windows 11 Pro (Client)
  - Debian 13 (Linux Fileserver)
  - Ubuntu (Linux Domänen-Client)

## Umsetzung
1. **Active Directory:** Aufsetzen des DCs `srv-win01`, Domäne `firma.lan`, Anlegen von OUs (`IT`, `Vertrieb`), Benutzern und Gruppen.
2. **Netzwerk:** Einrichtung eines statischen IP-Plans, DNS-Weiterleitung und Hyper-V NAT.
3. **Fileserver:** Installation von Samba auf `srv-linux01` und Bereitstellung einer Freigabe für Windows-Clients.
4. **Heterogene Clients:** Beitritt eines Windows 11 Clients und einer Ubuntu-VM in die Active Directory Domäne (`realmd`/`sssd`).

## Verwendete Technologien & Skills
- **Windows:** Active Directory, DNS, PowerShell-Automatisierung
- **Linux:** Debian, Ubuntu, Samba, SSSD, Kerberos, Systemd
- **Virtualisierung:** Hyper-V, Virtual Switches, NAT

## Autor
Eugen – Umschulung Fachinformatiker Systemintegration
