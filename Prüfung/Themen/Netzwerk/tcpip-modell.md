> [!WARNING] Wird überarbeitet!

# TCP/IP-Modell  

Das **TCP/IP-Modell** (Transmission Control Protocol/Internet Protocol) ist ein **praxisnahes Netzwerkmodell**, das die **Kommunikation in Computernetzwerken beschreibt**. Es dient als **Grundlage des Internets** und definiert, wie **Daten über Netzwerke übertragen und empfangen werden**.  

Im Gegensatz zum [**OSI-Schichtmodell**](osi-schichtmodell.md), das aus **sieben Schichten** besteht, verwendet das TCP/IP-Modell **nur vier Schichten**. Diese enthalten alle wichtigen Protokolle, die für die Internetkommunikation notwendig sind.  

***

## Die vier Schichten des TCP/IP-Modells  

### 1. **Netzzugangsschicht (Link Layer)**  
Diese Schicht regelt die **physikalische Verbindung** zwischen Geräten und die **Datenübertragung im lokalen Netzwerk**. Sie umfasst **Hardware-Komponenten** wie **Netzwerkkarten, Switches und Kabel**.  

### 2. **Internetschicht (Internet Layer)**  
Die Internetschicht ist für die **Adressierung und das Routing der Datenpakete** zuständig. Sie verwendet **IP-Adressen** zur eindeutigen Identifikation von Geräten im Netzwerk und sorgt für eine **korrekte Weiterleitung der Pakete**.  

### 3. **Transportschicht (Transport Layer)**  
Diese Schicht stellt eine **zuverlässige oder unzuverlässige Datenübertragung** zwischen Sender und Empfänger sicher. **TCP (Transmission Control Protocol)** bietet eine **verbindungsorientierte, zuverlässige Übertragung**, während **UDP (User Datagram Protocol)** eine **schnellere, aber unzuverlässige Verbindung** ermöglicht.  

### 4. **Anwendungsschicht (Application Layer)**  
Die Anwendungsschicht enthält alle **Protokolle, die direkt von Anwendungen genutzt werden**, z. B. **HTTP (Webseiten), SMTP (E-Mails) oder FTP (Dateiübertragung)**.  

***

## Vergleich von OSI- und TCP/IP-Modell  

| **Schicht TCP/IP-Modell**  | **Schicht OSI-Modell**              | **Funktion**                                               |
|:-------------------------:|:---------------------------------:|:--------------------------------------------------------:|
| Anwendungsschicht         | Anwendung, Darstellung, Sitzung  | Stellt Dienste für Anwendungen bereit                   |
| Transportschicht          | Transportschicht                 | Verantwortlich für die Kommunikation zwischen Prozessen |
| Internetschicht           | Vermittlungsschicht              | Bestimmt den optimalen Weg für Datenpakete             |
| Netzzugangsschicht        | Sicherungsschicht, Bitübertragung | Regelt den Zugriff auf das Übertragungsmedium          |

***

## Übersichtstabelle der TCP/IP-Schichten  

| **Nr.** | **Schicht (Deutsch)**    | **Schicht (Englisch)**  | **Adressierung**  | **Beschreibung**                                       | **Protokolle / Geräte**        |
|:------:|:----------------------:|:----------------:|:---------------:|:--------------------------------------------------:|:-------------------------:|
| 4      | Anwendungsschicht      | Application Layer | URLs, Domänen   | Stellt Netzwerkdienste für Anwendungen bereit     | HTTP, FTP, SMTP, DNS     |
| 3      | Transportschicht       | Transport Layer   | Portnummern     | Regelt Zuverlässigkeit und Flusskontrolle        | TCP, UDP                 |
| 2      | Internetschicht        | Internet Layer    | IP-Adressen     | Bestimmt die Route der Datenpakete               | IP, ICMP, Router         |
| 1      | Netzzugangsschicht     | Link Layer       | MAC-Adressen    | Steuert den Datenzugriff auf das Übertragungsmedium | Ethernet, WLAN, Switch   |

***

## Bedeutung des TCP/IP-Modells  

Das TCP/IP-Modell bildet die **Grundlage für das heutige Internet**. Es ist **weniger theoretisch als das OSI-Modell**, da es **auf real existierenden Protokollen basiert**. Durch seine **geringere Anzahl an Schichten** ist es **praktischer** und hat sich als **de facto Standard** etabliert.  

***

## Vorteile & Nachteile des TCP/IP-Modells  

| **Aspekt**       | **Vorteile**                                      | **Nachteile**                                        |
|:---------------:|:----------------------------------------------:|:------------------------------------------------:|
| **Praxisnähe**  | Wird im Internet und realen Netzwerken verwendet | Weniger genau definierte Trennung der Schichten |
| **Flexibilität**| Unterstützt verschiedene Hardware & Netzwerke   | Komplexer als nötig für kleine Netzwerke        |
| **Robustheit**  | Funktioniert auch bei fehlerhaften Verbindungen  | Keine klare Trennung von Präsentation & Sitzung |
| **Skalierbarkeit** | Ermöglicht große Netzwerke wie das Internet    | Keine einheitliche Sicherheitsmechanismen       |

***

## Quelle

- [Wikipedia - TCP/IP-Modell, 11.03.2025](https://de.wikipedia.org/wiki/TCP/IP)  
