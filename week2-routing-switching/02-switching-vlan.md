# Switching e VLAN

## Switch vs Hub

| Dispositivo | Livello OSI | Comportamento |
|-------------|-------------|---------------|
| Hub | L1 Physical | Ripete segnale su tutte le porte |
| Switch | L2 Data Link | Inoltra frame solo alla porta corretta |

## MAC Address Table
- Lo switch salva MAC address + porta in una tabella
- Frame verso MAC conosciuto: inviato solo sulla porta corretta
- Frame verso MAC sconosciuto: flooding su tutte le porte tranne sorgente
- Frame broadcast: flooding su tutte le porte tranne sorgente

## VLAN

### Tipi di porta
| Tipo | Descrizione | Uso |
|------|-------------|-----|
| Access port | Appartiene a una sola VLAN | Collegata a PC/stampanti |
| Trunk port | Trasporta più VLAN con tag 802.1Q | Tra switch o switch-router |

### Comandi Cisco IOS
enable
configure terminal
vlan 10
name Marketing
exit
interface fastethernet 0/1
switchport mode access
switchport access vlan 10
exit
interface fastethernet 0/24
switchport mode trunk
exit

### Verifica
show vlan brief
show interfaces fastethernet 0/24 switchport

## STP — Spanning Tree Protocol
- Previene loop nella rete bloccando collegamenti ridondanti
- Root Bridge: switch con Bridge ID più basso (priority + MAC)
- BPDU: messaggi che gli switch si scambiano per eleggere il Root Bridge
- BPDU Guard: disabilita la porta se riceve BPDU su una access port

## Attacchi
- STP Root Bridge attack: attaccante invia BPDU con priority 0
- VLAN hopping: sfrutta native VLAN mal configurata
- Contromisura: BPDU Guard + cambiare native VLAN da 1

## Lab completato
- Creato rete con 2 switch, 4 PC, VLAN 10 e VLAN 20
- Verificato: stessa VLAN comunica, VLAN diverse non comunicano
- File: vlan-lab.pkt
