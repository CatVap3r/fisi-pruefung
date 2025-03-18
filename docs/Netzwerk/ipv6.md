> [!INFO] Neue Version
# IPv6-Adresse

IPv6 wurde eingeführt, um die Adressknappheit von IPv4 zu beheben. Es nutzt **128-Bit-Adressen**, geschrieben in hexadezimaler Form, z. B. `2001:0db8:85a3::8a2e:0370:7334`. Dies ermöglicht **2^128 mögliche Adressen**. IPv6-Adressen sind der [OSI-Sicht 3 (Vermittlungsschicht)](osi-schichtmodell.md#osi-schichtmodell#osi-schichten#3%20vermittlungsschicht%20(network%20layer)) untergeordnet.

***

## Notation

1. IPv6 Adressen werden in **Hexadezimal** notiert, wobei die Zahl in **8 Blöcken** zu jeweils **16Bit** unterteilt wird.

2. **Führende Nullen** innerhalb eines Blockes dürfen ausgelassen werden:
	>```
	>2001:0db8:0000:08d3:0000:8a2e:0070:7344
	>```
	>ist gleichbedeutend mit
	>```
	>2001:db8:0:8d3:0:8a2e:70:7344
	>```

3. Ein oder mehrere aufeinander folgende Blöcke, deren Wert ``:0:`` sprich ``:0000:``  beträgt, dürfen ausgelassen werden. Dies wird durch zwei aufeinander folgende ``::`` angezeigt. Dieser Prozess darf nur **einmal pro Adresse** ausgeführt werden:
	>```
	>2001:db8:0:0:0:0:1428:57ab
	>```
	>ist gleichbedeutend mit
	>```
	>2001:db8::1428:57ab
	>```
***

## Aufbau

Eine IPv6 Adresse besteht aus **zwei** Komponenten:

- Erste 64bit: **Netzwerkteil** bestehend aus dem Präfix, das vom ISP oder Netzwerkadministrator zugewiesen wird.

- Letze 64bit: **Schnittstellen-ID**, die entweder aus der MAC-Adresse abgeleitet, zufällig generiert (durch Privacy Extensions) oder manuell eingetragen wird.

***

## Subnetting und Präfixe
 
 IPv6 nutzt CIDR (Classless Inter-Domain Routing) zur Adressierung. Ein Präfix gibt die Netzwerkgröße an. Das Subnetting erfolgt durch die Erweiterung des Präfixes:
 
|Präfix |Beispiel                               |Anzahl möglicher Adressen |
|:-----:|:--------------------------------------|-------------------------:|
|/8     |XX::                                   |2<sup>120</sup>           |
|/16    |XXXX::                                 |2<sup>112</sup>           |
|/24    |XXXX:XX::                              |2<sup>104</sup>           |
|/32    |XXXX:XXXX::                            |2<sup>96</sup>            |
|/40    |XXXX:XXXX:XX::                         |2<sup>88</sup>            |
|/48    |XXXX:XXXX:XXXX::                       |2<sup>80</sup>            |
|/56    |XXXX:XXXX:XXXX:XX::                    |2<sup>72</sup>            |
|/64    |XXXX:XXXX:XXXX:XXXX::                  |2<sup>64</sup>            |
|/72    |XXXX:XXXX:XXXX:XXXX:XX::               |2<sup>56</sup>            |
|/80    |XXXX:XXXX:XXXX:XXXX:XXXX::             |2<sup>48</sup>            |
|/88    |XXXX:XXXX:XXXX:XXXX:XXXX:XX::          |2<sup>40</sup>            |
|/96    |XXXX:XXXX:XXXX:XXXX:XXXX:XXXX::        |2<sup>32</sup>            |
|/104   |XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XX::     |2<sup>24</sup>            |
|/112   |XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX::   |2<sup>16</sup>            |
|/120   |XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XX::|2<sup>8</sup>             |
|/128   |XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX|2<sup>0</sup> (1)         |

***

## Adressierungstypen

- **Unicast**: Eine eindeutige Adresse für eine einzelne Netzwerkverbindung.
- **Multicast**: Pakete werden an eine Gruppe von Geräten gesendet (`FF00::/8` für IPv6).
- **Anycast**: Mehrere Geräte teilen sich eine Adresse, wobei das nächstgelegene Gerät antwortet.

***

## Fazit

- IPv6-Adressen bestehen aus **128bit** in jeweils **16bit Blöcken** getrennt durch `:` welche in der **Hexadezimalform** geschrieben werden.
- **2<sup>128</sup>** mögliche Adressen.
- **Unicast**, **Multicast** und **Anycast** verfügbar.
- **Führende Nullen**, wie ``:0000:``, dürfen zu ``:0:`` gekürzt werden.
- **Blöcke aus Nullen**, wie ``:0000:0000:0000:``, dürfen mit ``::`` **einmal pro Adresse** gekürzt werden.
- Erste 64bit **Netzwerkteil**, letzte 64bit **Schnittstellen-ID**

***

## Quellen

- [Wikipedia - IPv6 | Aufgerufen: 18.03.2025](https://de.wikipedia.org/wiki/IPv6)