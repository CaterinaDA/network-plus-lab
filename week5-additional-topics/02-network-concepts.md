# Network Concepts Aggiuntivi

## Traffic Types
- Unicast: un mittente, un destinatario specifico
- Broadcast: un mittente, tutti i dispositivi della rete (non attraversa router)
- Multicast: un mittente, gruppo specifico di destinatari iscritti
- Anycast: un mittente, il server piu vicino tra un gruppo con stesso IP

## Transmission Media

### Fibra ottica
| | Single-mode (SMF) | Multi-mode (MMF) |
|--|-------------------|------------------|
| Colore | Giallo | Arancione/Aqua |
| Distanza | Lunga (km) | Corta (500m) |
| Uso | WAN, tra edifici | Datacenter |

### Altri media
- Coassiale: TV via cavo, connettori F-type (TV) e BNC (professionale)
- DAC: Direct Attach Cable, rame con SFP+ integrati, max 7m, economico per datacenter

### Wireless
- 802.11: WiFi (settimana 2)
- Cellular: 3G/4G LTE/5G - backup WAN aziendale
- Satellite: alta latenza GEO (500ms), bassa latenza LEO come Starlink (20-40ms)

## Transceivers e Connettori

### Transceivers (moduli hot-swappable)
- SFP: 1 Gbps
- SFP+: 10 Gbps
- QSFP: 40 Gbps
- QSFP+: 40/100 Gbps

### Connettori fibra
- SC: quadrato, push-pull, reti enterprise
- LC: piccolo, a clip, datacenter e SFP
- ST: rotondo, a baionetta, reti vecchie
- MPO: multi-fiber, datacenter ad alta densita

### Connettori rame
- RJ45: Ethernet standard
- RJ11: telefono analogico
- BNC: coassiale professionale
- F-type: coassiale TV/cable internet

## Network Topologies
- Star/Hub and spoke: tutti collegati a switch centrale
- Mesh: connessioni multiple tra nodi (full o partial)
- Point-to-point: collegamento diretto tra due dispositivi
- Spine and Leaf: datacenter moderni, max 2 hop tra server
- Three-tier: Core, Distribution, Access
- Collapsed core: Core e Distribution uniti, reti medio-piccole
- Hybrid: combinazione di piu topologie

## IPv4 Aggiuntivi
| Range | Uso |
|-------|-----|
| 127.0.0.1 | Loopback |
| 169.254.0.0/16 | APIPA - DHCP non raggiungibile |
| 224.0.0.0-239.255.255.255 | Classe D - Multicast |
| 240.0.0.0-255.255.255.255 | Classe E - Sperimentale |

## VLSM
Subnet di dimensioni diverse nella stessa rete
Esempio: /26 per 50 host, /27 per 20 host, /30 per collegamento router
