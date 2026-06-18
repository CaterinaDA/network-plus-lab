# Network Operations e Security Aggiuntivi

## FHRP - First Hop Redundancy Protocol
- Crea un gateway virtuale (VIP) condiviso tra due router
- Se il router attivo cade, quello in standby prende il controllo
- I client non si accorgono del failover

| Protocollo | Sviluppatore | Note |
|------------|-------------|------|
| HSRP | Cisco | Hot Standby Router Protocol |
| VRRP | Standard aperto | Virtual Router Redundancy Protocol |
| GLBP | Cisco | Aggiunge load balancing tra router |

## Subinterfaces - Router on a Stick
- Una sola interfaccia fisica gestisce piu VLAN
- Il trunk porta tutte le VLAN al router
- Il router usa subinterface virtuali per inter-VLAN routing

## MTU e Jumbo Frames
- MTU default Ethernet: 1500 bytes
- Jumbo Frames: 9000 bytes, usati in datacenter
- MTU mismatch: pacchetti scartati o frammentati, connessione intermittente

## PoE - Power over Ethernet
| Standard | Potenza |
|----------|---------|
| 802.3af | 15.4W |
| 802.3at (PoE+) | 30W |
| 802.3bt (PoE++) | 60-100W |

## Documentation
- Physical diagram: posizione fisica dispositivi
- Logical diagram: connessioni logiche, IP, VLAN
- Rack diagram: dispositivi nel rack in unita U
- Cable map: ogni cavo documentato
- Asset inventory: lista dispositivi con seriale e posizione
- IPAM: gestione indirizzi IP
- SLA: accordo livelli di servizio
- Wireless survey: mappa copertura WiFi

## Life-cycle Management
- EOL: End of Life - non venduto, no aggiornamenti sicurezza
- EOS: End of Support - no supporto tecnico ne patch
- Decommissioning: ritiro dispositivo, cancellazione dati, smaltimento

## Disaster Recovery
| Metrica | Descrizione |
|---------|-------------|
| RPO | Recovery Point Objective - quanti dati si possono perdere |
| RTO | Recovery Time Objective - tempo massimo di ripristino |
| MTTR | Mean Time To Repair - tempo medio di riparazione |
| MTBF | Mean Time Between Failures - affidabilita sistema |

| Sito DR | Costo | RTO |
|---------|-------|-----|
| Cold site | Basso | Giorni/settimane |
| Warm site | Medio | Ore/giorni |
| Hot site | Alto | Minuti/ore |

## VPN
- Site-to-site: collega due sedi permanentemente
- Remote access: utente singolo si connette da remoto
- Protocolli: IPSec, SSL/TLS, OpenVPN, WireGuard

## Security Aggiuntivi

### PKI
- CA: emette e firma certificati digitali
- CRL: lista certificati revocati
- OCSP: verifica validita certificato in tempo reale

### RADIUS vs TACACS+
| | RADIUS | TACACS+ |
|--|--------|---------|
| Standard | Aperto | Cisco proprietario |
| Protocollo | UDP | TCP |
| Uso | WiFi 802.1X, VPN | Gestione dispositivi Cisco |

### SAML
- SSO federato: un login per piu servizi
- Identity Provider: autentica utente (Active Directory)
- Service Provider: servizio a cui si accede (Salesforce)

### Deception Technologies
- Honeypot: server falso vulnerabile per studiare attaccanti
- Honeynet: rete intera di honeypot

### Social Engineering
- Phishing: email false
- Spear phishing: phishing mirato
- Vishing: phishing via telefono
- Smishing: phishing via SMS
- Dumpster diving: cercare info nei rifiuti
- Shoulder surfing: spiare lo schermo
- Tailgating: seguire qualcuno attraverso porta sicura

### Compliance
- PCI DSS: standard per dati carte di credito
- GDPR: protezione dati personali EU, notifica breach 72 ore
- Data locality: dati devono rimanere in giurisdizione specifica

## Cabling e Physical Issues
### Tipi di cavo
- Straight-through: dispositivi diversi (PC-Switch, Switch-Router)
- Crossover: dispositivi uguali (Switch-Switch, PC-PC)
- Auto-MDI/MDIX: rileva automaticamente il tipo di cavo

### Duplex
- Half-duplex: un dispositivo alla volta trasmette, collisioni possibili
- Full-duplex: trasmissione e ricezione simultanea, nessuna collisione
- Duplex mismatch: connessione lenta, contatori errori in aumento

### Port Status
| Status | Significato |
|--------|-------------|
| Up/Up | Tutto ok |
| Up/Down | Fisicamente connessa, protocollo non funziona |
| Down/Down | Nessun cavo o dispositivo spento |
| Administratively down | Disabilitata manualmente |

### Performance Issues
- Congestion: troppo traffico per la banda disponibile
- Latency: ritardo nella trasmissione
- Packet loss: pacchetti non arrivano a destinazione
- Jitter: variazione nella latenza, critico per VoIP
- Wireless interference: microonde, altri AP, ostacoli fisici
