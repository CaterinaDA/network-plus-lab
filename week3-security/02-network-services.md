# Servizi di Rete

## DHCP - processo DORA
1. DISCOVER - client manda broadcast
2. OFFER - server offre un IP
3. REQUEST - client accetta l'IP
4. ACK - server conferma assegnazione

## Concetti DHCP
- Lease time: durata assegnazione IP, rinnovo a meta tempo
- DHCP Scope: range di IP assegnabili
- DHCP Reservation: IP fisso basato su MAC address
- DHCP Relay Agent: inoltra richieste broadcast al server DHCP in altra subnet (converte in unicast)

## DNS - tipi di record
| Record | Funzione |
|--------|----------|
| A | Nome -> IPv4 |
| AAAA | Nome -> IPv6 |
| CNAME | Alias -> altro nome |
| MX | Mail server |
| PTR | IPv4 -> Nome (reverse lookup) |
| NS | Name server autoritativo |
| TXT | Testo generico (SPF, DKIM) |
| SOA | Start of Authority |

## DNS - gerarchia query (recursive)
1. Client -> resolver locale
2. Resolver -> Root server
3. Root -> TLD server (.com)
4. TLD -> nameserver del dominio
5. Nameserver -> risposta con IP
6. Resolver salva in cache e risponde al client

## Authoritative vs Non-authoritative
- Non-authoritative: risposta dalla cache del resolver
- Authoritative: risposta diretta dal nameserver del dominio
- TTL: tempo di validita del record in cache

## NTP
- Porta 123 UDP
- Critico per Kerberos/Active Directory (tolleranza max 5 minuti)
- Stratum: gerarchia di sincronizzazione (0 = fonte di riferimento)
