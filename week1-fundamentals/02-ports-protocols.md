# Porte e Protocolli

## Obiettivo
Memorizzare le porte chiave per l'esame CompTIA Network+.

## Porte principali

| Porta | Protocollo | Servizio | Note |
|-------|-----------|---------|------|
| 20/21 | TCP | FTP | 20=dati, 21=controllo |
| 22 | TCP | SSH/SFTP | Sostituisce Telnet e FTP |
| 23 | TCP | Telnet | Non cifrato, insicuro |
| 25 | TCP | SMTP | Invio email |
| 53 | TCP/UDP | DNS | UDP query, TCP zone transfer |
| 67/68 | UDP | DHCP | 67=server, 68=client |
| 80 | TCP | HTTP | Web non cifrato |
| 110 | TCP | POP3 | Scarica email dal server |
| 123 | UDP | NTP | Sincronizzazione orario |
| 143 | TCP | IMAP | Sincronizza email |
| 161/162 | UDP | SNMP | 161=query, 162=trap |
| 389 | TCP | LDAP | Directory/Active Directory |
| 443 | TCP | HTTPS | Web cifrato TLS |
| 514 | UDP | Syslog | Log centralizzati |
| 636 | TCP | LDAPS | LDAP over SSL/TLS |
| 1433 | TCP | MS SQL | Database Microsoft |
| 3389 | TCP | RDP | Remote Desktop Windows |
| 5060/5061 | TCP/UDP | SIP | VoIP |

## Concetti chiave
- DNS usa UDP per query normali, TCP per zone transfer
- NTP porta 123 critico per Kerberos/Active Directory
- DHCP: client invia dalla 68, server risponde sulla 67
- LDAPS 636 è la versione sicura di LDAP 389
