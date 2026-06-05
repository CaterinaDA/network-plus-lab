# OSI Model

## Obiettivo
Comprendere i 7 livelli OSI, le PDU e i protocolli per livello.

## Livelli

| Livello | Nome | PDU | Esempi |
|---------|------|-----|--------|
| 7 | Application | Data | HTTP, HTTPS, FTP, DNS, DHCP |
| 6 | Presentation | Data | SSL/TLS, JPEG, ASCII |
| 5 | Session | Data | NetBIOS, RPC |
| 4 | Transport | Segmento/Datagramma | TCP, UDP |
| 3 | Network | Pacchetto | IP, ICMP, OSPF |
| 2 | Data Link | Frame | Ethernet, MAC, ARP |
| 1 | Physical | Bit | RJ45, fibra, 802.11 |

## Concetti chiave
- Encapsulation: i dati scendono lo stack OSI, ogni livello aggiunge un header
- Decapsulation: i dati risalgono lo stack OSI, ogni livello rimuove il proprio header
- ARP: traduce IP (L3) in MAC (L2)
- SSL/TLS opera a L6, non a L7

## Mnemonico
Please Do Not Touch Steve's Pet Alligator
(Physical, Data link, Network, Transport, Session, Presentation, Application)
