# Troubleshooting

## Metodologia CompTIA (7 passi)
1. Identify the problem
2. Establish a theory of probable cause
3. Test the theory
4. Establish a plan of action
5. Implement the solution
6. Verify full system functionality
7. Document findings

## Regola fondamentale
Non saltare mai il passo 3 (test theory) prima di implementare la soluzione.

## Comandi CLI

| Funzione | Windows | Linux |
|----------|---------|-------|
| Configurazione IP | ipconfig | ip a |
| Routing table | route print | ip route |
| Connessioni attive | netstat -an | ss -tuln |
| DNS lookup | nslookup | nslookup / dig |
| Tracciare percorso | tracert | traceroute |
| Ping | ping | ping -c 4 |
| ARP cache | arp -a | arp -a |
| Percorso specifico | - | ip route get X.X.X.X |

## Scenari tipo esame

### Ping 8.8.8.8 funziona, siti web non aprono
Problema: DNS non risponde, non il gateway
Tool: nslookup per verificare DNS

### traceroute mostra * * * ma destinazione raggiungibile
Causa: router intermedi filtrano ICMP
Non significa rete rotta

### ARP cache mostra MAC sconosciuto per il gateway
Causa: ARP poisoning in corso
Soluzione: DAI, isolare il dispositivo sospetto

### Switch fa flooding su tutte le porte
Causa: MAC address table piena (MAC flooding attack)
Soluzione: Port Security

## Hardening pratico
- MySQL bind-address = 127.0.0.1 per limitare esposizione
- Regola: Local Address 0.0.0.0 = esposto, 127.0.0.1 = sicuro

## Simulazione esame
Punteggio: 13/15 (87%)
Aree da ripassare: posizionamento ACL, troubleshooting DNS vs gateway
