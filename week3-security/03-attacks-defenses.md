# Attacchi e Difese di Rete

## Attacchi Livello 2

### ARP Poisoning / Spoofing
- ARP e stateless, accetta risposte non richieste
- Attaccante invia risposte ARP false, sostituendo il MAC del gateway
- Risultato: on-path attack (man-in-the-middle)
- Contromisura: Dynamic ARP Inspection (DAI) - verifica corrispondenza con tabella DHCP

### MAC Flooding
- Attaccante riempie la MAC address table dello switch con MAC falsi
- Switch in overflow fa flooding su tutte le porte (si comporta da hub)
- Contromisura: Port Security - limita MAC accettati per porta

### VLAN Hopping
- Switch Spoofing: attaccante negozia trunk port con lo switch
- Double Tagging: doppio tag 802.1Q per saltare tra VLAN
- Contromisura: cambiare native VLAN da 1, disabilitare trunking automatico

## Attacchi Livello 3

### DoS / DDoS
- DoS: singolo attaccante
- DDoS: botnet distribuita
- SYN Flood: richieste TCP SYN incomplete, esaurisce connessioni
- Ping of Death: pacchetti ICMP malformati
- Amplification attack: sfrutta DNS/NTP per amplificare traffico

### DNS Spoofing / Poisoning
- Modifica cache resolver con record falsi
- Contromisura: DNSSEC (firme digitali sui record DNS)

## Difese di Rete

### ACL - Access Control List
- Regole valutate dall'alto verso il basso, prima corrispondenza vince
- Deny all implicito in fondo

| Tipo | Filtra per | Posizionamento |
|------|-----------|----------------|
| Standard ACL | Solo IP sorgente | Vicino alla destinazione |
| Extended ACL | Sorgente + destinazione + protocollo + porta | Vicino alla sorgente |

### NAC - Network Access Control
- Verifica stato di salute del dispositivo prima di permettere accesso
- Controlli: antivirus, patch OS, certificati, dominio
- Dispositivi non conformi -> quarantine VLAN

### Segmentazione di rete
- DMZ / Screened Subnet: zona tra internet e rete interna per server pubblici
- Architettura: Internet -> Firewall esterno -> DMZ -> Firewall interno -> Rete interna
- Altre VLAN di segmentazione: IoT, Guest, BYOD, OT/SCADA

## Lab AD Security
- Verificate GPO su OU Marketing con Group Policy Modeling
- GPO applicate: Blocco Pannello di Controllo Marketing, Blocco Schermo Marketing
- Concetto: le GPO si applicano solo agli oggetti dentro l'OU collegata
