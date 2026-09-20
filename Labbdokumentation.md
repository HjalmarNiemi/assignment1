# Labbdokumentation: Labbmiljö, Git, CLI och AI
**Namn:** Hjalmar Niemi  
**Datum:** 15 september 2026,  
**Kurs:** Introduktion till yrkesrollen och grunderna i IT-infrastruktur

## 1. Titel och introduktion:

### Introduktion

Denna rapport dokumenterar uppsättningen och genomförandet av labbmiljön i uppgiften *Labbmiljö, Git, CLI och AI*. Syftet med denna laboration är att praktiskt tillämpa och demonstrera färdigheter inom nätverkskonfiguration, kommandon i Linux och Windows, versionhantering med Git samt kritisk granskning av AI

### Labbmiljö
Labbmiljön består av följande:
- **Linux-miljö:** Virtuell maskin med Ubuntu som körs via VirtualBox.
- **Windows-miljö:** Virtuell maskin med Windows11 som körs via VirtualBox.
- **Git/Github:** Versionshantering.
- **Visual Studio Code:** Dokumentation i Markdown.

### Nätverkstabell  
| Hostname | Operativsystem | IP-adress | Subnätmask | Standard Gateway |
| -------- | -------------- | --------- | ---------- | ---------------- |
| Ubuntu-Server-Lab | Ubuntu 26.04.1 LTS | 192.168.1.50 | 255.255.255.0 | Ej tillämpbart |
| Windows11-Lab | Windows 11 Home 25H2 | 192.168.1.51 | 255.255.255.0 | Ej tillämpbart |

## Kommandoradsarbete & Felsökning
### Linux
1. Skapa mappen /var/systementor/konsultdata och filen anteckningar.txt:
`sudo mkdir -p /var/systementor/konsultdata && sudo touch /var/systementor/konsultdata/anteckningar.txt`  

2. Skapa ny grupp `sudo groupadd konsulter`  
Gör gruppen konsulter till ägare över mappen /var/systementor/konsultdata samt alla filer/undermappar & ändra rättigheter:  
```
sudo chown -R :konsulter /var/systementor/konsultdata
sudo chmod 750 /var/systementor/konsultdata
sudo chmod 640 /var/systementor/konsultdata/anteckningar.txt
```
Nu kan vi se att gruppen *konsulter* är ägare och rättigheterna ändrats:

![rättigheter](images/rättigheterlinux.png)

![pingawindows](images/ping-test1.png)

### Windows
1. 