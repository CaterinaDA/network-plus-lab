# Routing

## Routing statico vs dinamico

| Tipo | Pro | Contro | Uso |
|------|-----|--------|-----|
| Statico | Semplice, prevedibile | Non si adatta ai guasti | Reti piccole |
| Dinamico | Si adatta automaticamente | Più complesso | Reti grandi |

## Protocolli di routing dinamico

| Protocollo | Metrica | Uso |
|------------|---------|-----|
| RIP | Hop count (max 15) | Obsoleto |
| OSPF | Costo (banda) | Enterprise |
| BGP | Policy | Internet tra provider |

## NAT

| Tipo | Descrizione | Uso |
|------|-------------|-----|
| Static NAT | 1 IP privato = 1 IP pubblico | Server interni |
| Dynamic NAT | Pool di IP pubblici | Reti medie |
| PAT | Molti IP privati = 1 IP pubblico (porta) | Reti domestiche/aziendali |

## Concetti chiave
- Default route: 0.0.0.0/0 — percorso di last resort
- Routing table: tabella con tutti i percorsi conosciuti
- OSPF usa il costo (banda) non gli hop come metrica
- PAT = NAT Overload — usato quasi ovunque
- Comando Linux: ip route — mostra la routing table
- Comando Linux: ip route get X.X.X.X — mostra il percorso verso un IP
