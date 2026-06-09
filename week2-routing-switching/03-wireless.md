# Wireless

## Standard WiFi

| Standard | Nome | Frequenza | Velocità max |
|----------|------|-----------|--------------|
| 802.11a | WiFi 1 | 5 GHz | 54 Mbps |
| 802.11b | WiFi 2 | 2.4 GHz | 11 Mbps |
| 802.11g | WiFi 3 | 2.4 GHz | 54 Mbps |
| 802.11n | WiFi 4 | 2.4/5 GHz | 600 Mbps |
| 802.11ac | WiFi 5 | 5 GHz | 3.5 Gbps |
| 802.11ax | WiFi 6 | 2.4/5/6 GHz | 9.6 Gbps |

## Frequenze e canali
- 2.4 GHz: portata maggiore, più interferenze, canali non sovrapposti: 1, 6, 11
- 5 GHz: più veloce, meno interferenze, molti canali non sovrapposti
- Regola: AP vicini devono usare canali non sovrapposti

## Sicurezza wireless

| Protocollo | Stato | Problema |
|------------|-------|---------|
| WEP | Broken | RC4 debole, craccabile in minuti |
| WPA | Deprecato | Ancora vulnerabile |
| WPA2 | Accettabile | Vulnerabile a KRACK |
| WPA3 | Raccomandato | SAE, forward secrecy |

## Modalità autenticazione
- Personal (PSK): password condivisa, reti piccole
- Enterprise (802.1X): credenziali individuali, server RADIUS

## Tipi di rete
| Tipo | Descrizione |
|------|-------------|
| IBSS | Ad-hoc, senza AP |
| BSS | Un solo AP |
| ESS | Più AP collegati |
| MBSS | Rete mesh |

## Antenne
- Omnidirezionale: segnale 360°, uso generale
- Direzionale: segnale concentrato, punto-punto tra edifici

## Attacchi wireless
- Evil Twin: AP falso con stesso SSID
- Rogue AP: AP non autorizzato collegato alla rete
- Deauthentication attack: disconnette forzatamente i client

## Lab completato
- Analisi rete WiFi con netsh wlan show networks mode=bssid
- Rete rilevata: WPA2-Personal, 802.11ac, 5GHz, canale 149
