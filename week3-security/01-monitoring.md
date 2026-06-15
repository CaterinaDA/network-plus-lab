# Network Monitoring

## SNMP
- Manager (NMS): software centrale che raccoglie dati - Nagios, PRTG, SolarWinds
- Agent: software su ogni dispositivo monitorato
- MIB: database di OID (Object Identifier) - standard per identificare le informazioni

## Porte SNMP
| Porta | Direzione | Uso |
|-------|-----------|-----|
| 161 UDP | Manager -> Agent | Query |
| 162 UDP | Agent -> Manager | Trap (allarmi spontanei) |

## Versioni SNMP
| Versione | Sicurezza |
|----------|-----------|
| SNMPv1 | Community string in chiaro - obsoleto |
| SNMPv2c | Community string in chiaro - diffuso |
| SNMPv3 | Autenticazione + cifratura - raccomandato |

## Syslog
- Porta 514 UDP (6514 TLS)
- Log centralizzati da tutti i dispositivi

## Livelli di severita Syslog (0-7)
| Livello | Nome |
|---------|------|
| 0 | Emergency |
| 1 | Alert |
| 2 | Critical |
| 3 | Error |
| 4 | Warning |
| 5 | Notice |
| 6 | Informational |
| 7 | Debug |

Mnemonico: Every Awesome Cisco Engineer Will Need Ice Daily

## Port Mirroring (SPAN)
- Copia il traffico di una o piu porte su una porta dedicata
- Usato per collegare IDS/analyzer senza interferire col traffico

## NetFlow
- Raccoglie metadati del traffico (chi parla con chi, quanto, quando)
- Leggero, usato per monitoraggio continuo
- Wireshark cattura pacchetti completi - piu pesante, usato per analisi puntuale
