> [!INFO] Neue Version
# IPv4-Adresse

IPv4 ist die am weitesten verbreitete Version von IP und verwendet **32-Bit-Adressen**,
die in vier Dezimalzahlen (0-255) geschrieben werden, z. B. `192.168.1.1`. Es gibt ca.
**4,3 Milliarden** mögliche IPv4-Adressen. IPv4-Adressen sind der [OSI-Sicht 3 (Vermittlungsschicht)](osi-schichtmodell.md#osi-schichtmodell#osi-schichten#3%20vermittlungsschicht%20(network%20layer)) untergeordnet.

***

## Aufbau der IPv4-Adresse


***

## Adressierungstypen

- **Unicast**: Eine eindeutige Adresse für eine einzelne Netzwerkverbindung.
- **Broadcast**: Pakete werden an alle Geräte im Netzwerk gesendet(`255.255.255.255`).
- **Multicast**: Pakete werden an eine Gruppe von Geräten gesendet (`224.0.0.0 - 239.255.255.255` ).

***

## Adressklassen

| Klasse | Netz-Teil (y) | Host-Teil (x) |     Aufbau      |   Netzmaske   | Sufix |     Netze | Mögliche Hosts |
| :----: | :-----------: | :-----------: | :-------------: | :-----------: | :---: | --------: | -------------: |
|   A    |     8 Bit     |    24 Bit     | YYY.XXX.XXX.XXX |   255.0.0.0   |  /8   |       128 |     16.777.214 |
|   B    |    16 Bit     |    16 Bit     | YYY.YYY.XXX.XXX |  255.255.0.0  |  /16  |    16.384 |         65.534 |
|   C    |    24 Bit     |     8 Bit     | YYY.YYY.YYY.XXX | 255.255.255.0 |  /24  | 2.097.152 |            254 |

> [!TIP] Info
> Klasse D ist für die Verwendung von Multicast-Anwendungen reserviert.
> Klasse E ist für zukünftige Zwecke reserviert.

***

## IPv4-Subnetting

Subnetting unterteilt Netzwerke in kleinere Subnetze, um die IP-Adressverwaltung zu optimieren.

Beispiel:  
Ein Unternehmen benötigt 16 Subnetze in einem `192.168.1.0/24`-Netz.  
Die Subnetzmaske wird auf `/28` gesetzt:

- **Subnetz 1**: `192.168.1.0/28` (14 Hosts, da 2 für Netz- und Broadcastadresse reserviert sind).
- **Subnetz 2**: `192.168.1.16/28`
- … bis `192.168.1.240/28`.

***

## IPv4-NAT

***

## Quellen
- [Cloudflare - IP adresses, 12.03.2025](https://developers.cloudflare.com/1.1.1.1/ip-addresses/)
- [Cloudflare - Was ist ein Subnetz, 12.03.2025](https://www.cloudflare.com/de-de/learning/network-layer/what-is-a-subnet/)