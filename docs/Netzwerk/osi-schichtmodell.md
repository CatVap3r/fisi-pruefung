> [!TIP] Neue Version in Arbeit
# OSI-Schichtmodell  

Das **OSI-Schichtmodell** (Open Systems Interconnection Model) ist ein **theoretisches Referenzmodell für Netzwerke**, das die Kommunikation in **sieben Schichten** unterteilt. Es dient als **theoretische Grundlage** für Netzwerkprotokolle und beschreibt, **wie Daten von einer Anwendung eines Geräts zu einer Anwendung eines anderen Geräts übertragen werden**. In der Praxis wird häufig das [TCP/IP-Schichtmodell](tcpip-modell.md) verwendet, das in vielen realen Netzwerken zugrunde liegt, während das OSI-Modell hauptsächlich als theoretische Grundlage dient.

Jede Schicht hat eine spezifische Aufgabe und kommuniziert nur mit der darüber- und darunterliegenden Schicht. Das Modell hilft dabei, **Netzwerkprobleme zu analysieren, Protokolle zu standardisieren und die Interoperabilität zwischen verschiedenen Systemen zu gewährleisten**.  

***

## OSI-Schichten 

### 1. Bitübertragungsschicht (Physical Layer)
Die Bitübertragungsschicht sorgt für die **physikalische Übertragung von Daten** über ein Medium wie **Kupferkabel, Glasfaser oder Funk**.  

### 2. Sicherungsschicht (Data Link Layer)
Diese Schicht organisiert die **fehlerfreie Übertragung von Datenframes** zwischen direkt verbundenen Geräten. Sie regelt **Zugriffsverfahren und Fehlerkorrekturen**.  

### 3. Vermittlungsschicht (Network Layer)  
In der Vermittlungsschicht erfolgt das **Routing der Datenpakete** durch das Netzwerk. Sie bestimmt den **optimalen Pfad** von Quelle zu Ziel und nutzt dazu **IP-Adressen**. Geräte, welche auf der Vermittlungsschicht arbeiten sind beispielsweise **Layer-3-Switche** und **Router**.

### 4. Transportschicht (Transport Layer)
Diese Schicht sorgt für eine **zuverlässige oder unzuverlässige Datenübertragung**. Sie steuert die **Flusskontrolle, Fehlerkontrolle und Segmentierung**.  

### 5. Sitzungsschicht (Session Layer)  
Die Sitzungsschicht verwaltet und steuert die **Dauer einer Kommunikationssitzung** zwischen zwei Systemen.  

### 6. Darstellungsschicht (Presentation Layer)  
Hier werden **Datenformate standardisiert**, **Verschlüsselung** und **Komprimierung** durchgeführt.  

### 7. Anwendungsschicht (Application Layer)  
Diese Schicht stellt **Netzwerkdienste für Anwendungen** bereit, z. B. **HTTP, FTP oder E-Mail-Dienste**.  

***

## Übersichtstabelle der OSI-Schichten  

| **Nr.** | **Schicht (Deutsch)**      | **Schicht (Englisch)**  | **Adressierung**    | **Beschreibung**                                         | **Netzwerkgerät**           |
|:------:|:----------------------:|:----------------:|:----------------:|:--------------------------------------------------:|:------------------------:|
| 7      | Anwendungsschicht      | Application Layer  | URLs, Domänen    | Stellt Netzwerkdienste für Anwendungen bereit     | Gateway, Firewall        |
| 6      | Darstellungsschicht    | Presentation Layer | Keine            | Wandelt Daten in ein einheitliches Format um     | Gateway                  |
| 5      | Sitzungsschicht        | Session Layer     | Keine            | Steuert Sitzungsaufbau, -steuerung, -abbau       | Gateway                  |
| 4      | Transportschicht       | Transport Layer   | Portnummern      | Regelt den sicheren und zuverlässigen Transport  | Firewall                 |
| 3      | Vermittlungsschicht    | Network Layer     | IP-Adressen      | Bestimmt die optimale Route für Datenpakete     | Router                   |
| 2      | Sicherungsschicht      | Data Link Layer   | MAC-Adressen     | Organisiert fehlerfreie Datenübertragung        | Switch, Bridge           |
| 1      | Bitübertragungsschicht | Physical Layer    | Keine            | Physische Datenübertragung über das Medium      | Repeater, Hub, Kabel     |

***

## Bedeutung des OSI-Modells  

Das OSI-Modell hilft Entwicklern und Netzwerkadministratoren, **Fehler zu lokalisieren, Netzwerke zu optimieren und Kommunikationsprozesse besser zu verstehen**. In der Praxis werden oft mehrere Schichten von **Protokollen wie TCP/IP kombiniert**, um eine funktionierende Netzwerkkommunikation zu ermöglichen.  

***

## Vorteile & Nachteile des OSI-Modells  

|      **Aspekt**      |                  **Vorteile**                   |                    **Nachteile**                    |
| :------------------: | :---------------------------------------------: | :-------------------------------------------------: |
|     **Struktur**     |          Klare Trennung der Funktionen          |      In der Praxis nicht immer exakt anwendbar      |
| **Standardisierung** | Herstellerunabhängig, fördert Interoperabilität |  Manche Protokolle überschneiden mehrere Schichten  |
|   **Fehlersuche**    |          Erleichtert Netzwerkdiagnose           |               Komplex für Einsteiger                |
|   **Modularität**    |     Austausch einzelner Protokolle möglich      | Nicht alle realen Netzwerke folgen exakt dem Modell |

***

## Quelle

- [Wikipedia - OSI-Modell, 11.03.2025](https://de.wikipedia.org/wiki/OSI-Modell)  
