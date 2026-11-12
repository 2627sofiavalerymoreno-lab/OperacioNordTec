# Operació NordTec - Sofia Moreno Trelles (ASIX 1A)

## INDEX:

- [Operació NordTec - Sofia Moreno Trelles (ASIX 1A)](#operació-nordtec---sofia-moreno-trelles-asix-1a)
  - [INDEX:](#index)
  - [Estat del projecte](#estat-del-projecte)
    - [Que s'ha fet](#que-sha-fet)
    - [Què esta pendent?](#què-esta-pendent)
  - [Arquitectura de xarxa](#arquitectura-de-xarxa)
    - [Màquina Router (`router_lab_0373.yaml`)\[cite: 1\]](#màquina-router-router_lab_0373yamlcite-1)
    - [Màquines Client i Serveis](#màquines-client-i-serveis)
  - [Configuracions](#configuracions)
  - [Incidències i solucions](#incidències-i-solucions)
    - [Incidència 1](#incidència-1)
  - [Decisions tècniques](#decisions-tècniques)
  - [Reflexions tècniques](#reflexions-tècniques)

## Estat del projecte

### Que s'ha fet
### Què esta pendent? 
__________________________

## Arquitectura de xarxa

L'arquitectura de xarxa definida als fitxers Netplan de la infraestructura consta de les següents interfícies i adreçaments[cite: 1, 2, 5, 9]:

### Màquina Router (`router_lab_0373.yaml`)[cite: 1]
| Interfície | Segment / Comentari | Configuració IPv4 | Adreça IP / Màscara |
| :--- | :--- | :--- | :--- |
| `enp1s0` | Sortida a Internet (WAN)[cite: 7] | DHCP (`dhcp4: true`)[cite: 1] | Assignada dinàmicament |
| `enp2s0` | `#kali` | DHCP (`dhcp4: true`)[cite: 1, 2] | Assignada dinàmicament |
| `enp3s0` | `#dmz`[cite: 1, 2] | Estàtica (`dhcp4: false`)[cite: 1, 2] | `10.0.0.1/24`[cite: 1, 2] |
| `enp4s0` | `#lan`[cite: 1, 2] | Estàtica (`dhcp4: false`)[cite: 1, 2] | `192.168.10.1/24`[cite: 1, 2] |
| `enp5s0` | Xarxa interna LAN 2 | Estàtica (`dhcp4: false`)[cite: 1, 2] | `192.168.20.1/24` |

### Màquines Client i Serveis
| Màquina | Rol | Interfície | Adreça IP / Màscara | Passarel·la (*Gateway*) |
| :--- | :--- | :--- | :--- | :--- |
| **Client** | Equip d'usuari | `enp1s0` (`NetworkManager`) | `192.168.20.10/24`[cite: 9] | `192.168.20.1`[cite: 9] |
| **`nortec-lan`** (Codi `0F2A`) | Servidor Web (`rol="web"`) | Xarxa LAN (`192.168.10.0/24`) | `192.168.10.10`[cite: 5, 7] | `192.168.10.1` |

____________________________

## Configuracions

______________________________


## Incidències i solucions

### Incidència 1
- **Missatge d'error exacte:** 
- **Quan:** 
- **Causa:** 
- **Solució:** 
- **Detectada per:**

_____________________________

## Decisions tècniques

__________________________

## Reflexions tècniques