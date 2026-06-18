# Networking Appliances e Cloud Concepts

## Networking Appliances

### Firewall
- Stateless: filtra ogni pacchetto individualmente con regole ACL
- Stateful: tiene traccia dello stato delle connessioni
- NGFW: Next Generation Firewall - ispezione L7, include IDS/IPS

### IDS vs IPS
| | IDS | IPS |
|--|-----|-----|
| Posizione | Fuori banda (SPAN port) | In linea con il traffico |
| Azione | Solo rileva e avvisa | Rileva e blocca |
| Rischio | Falsi negativi | Falsi positivi |

### Load Balancer
- Distribuisce traffico tra piu server
- Garantisce high availability e ridondanza
- Se un server cade, il traffico viene distribuito sui rimanenti

### Proxy
- Forward proxy: client -> proxy -> internet (filtraggio, caching, anonimato)
- Reverse proxy: internet -> proxy -> server interni (load balancing, SSL termination)

### NAS vs SAN
| | NAS | SAN |
|--|-----|-----|
| Protocollo | NFS, SMB (file-level) | Fibre Channel, iSCSI (block-level) |
| Uso | File sharing | Database enterprise |
| Costo | Economico | Costoso |

## Cloud Concepts

### Service Models
| Modello | Provider gestisce | Cliente gestisce | Esempio |
|---------|-------------------|------------------|---------|
| SaaS | Tutto | Solo utilizzo | Gmail, Office 365 |
| PaaS | Infrastruttura + OS | Applicazioni | AWS Elastic Beanstalk |
| IaaS | Solo hardware | OS, app, sicurezza | AWS EC2, Azure VM |

### Deployment Models
- Public cloud: infrastruttura condivisa - startup, piccole aziende
- Private cloud: infrastruttura dedicata - banche, governo
- Hybrid cloud: mix public + private - dati sensibili on-premise
- Community cloud: condiviso tra organizzazioni simili

### Concetti cloud specifici
- NFV: virtualizza funzioni di rete hardware (firewall, router) su software
- VPC: rete privata isolata dentro un cloud pubblico
- Network Security Groups: firewall virtuali nel cloud
- Cloud Gateway: connessione sicura tra rete on-premise e cloud
- Elasticity: scala automaticamente in base alla domanda
- Scalability: capacita di crescere quando necessario
