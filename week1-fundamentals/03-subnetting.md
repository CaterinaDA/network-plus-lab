# Subnetting IPv4

## Obiettivo
Calcolare subnet, broadcast, range host e numero di host utilizzabili.

## Classi IPv4

| Classe | Range primo ottetto | Mask default | CIDR | Host |
|--------|-------------------|--------------|------|------|
| A | 1-126 | 255.0.0.0 | /8 | 16.777.214 |
| B | 128-191 | 255.255.0.0 | /16 | 65.534 |
| C | 192-223 | 255.255.255.0 | /24 | 254 |

- 127.x.x.x riservato al loopback (127.0.0.1)
- Indirizzi privati RFC1918: 10.x.x.x, 172.16-31.x.x, 192.168.x.x

## Tabella CIDR

| CIDR | Mask ultimo ottetto | Blocco | Host | Subnet /24 |
|------|-------------------|--------|------|------------|
| /24 | 0 | 256 | 254 | 1 |
| /25 | 128 | 128 | 126 | 2 |
| /26 | 192 | 64 | 62 | 4 |
| /27 | 224 | 32 | 30 | 8 |
| /28 | 240 | 16 | 14 | 16 |
| /29 | 248 | 8 | 6 | 32 |
| /30 | 252 | 4 | 2 | 64 |

## Formule
- Blocco = 256 - valore ultimo ottetto mask
- Host utilizzabili = blocco - 2
- Broadcast = indirizzo rete + blocco - 1

## Esempio
192.168.1.200/26
- Blocco: 256-192 = 64
- Multipli di 64: 0, 64, 128, 192 → rete: 192.168.1.192
- Broadcast: 192.168.1.192 + 64 - 1 = 192.168.1.255
- Host: da 192.168.1.193 a 192.168.1.254
