---
sidebar_position: 1
---

# Netzpläne  

Ein **Netzplan** ist ein grafisches Planungsinstrument im **Projektmanagement**, das **Abläufe und Abhängigkeiten** zwischen Aktivitäten darstellt.  
Er wird vor allem in komplexen Projekten genutzt, um **Prozesse zu visualisieren**, **Dauer zu berechnen** und **kritische Wege zu identifizieren**.  

**Beispiel:**\
\
![Beispiel für einen Netzplan](https://t2informatik.de/wp-content/uploads/2018/02/netzplan-wissen-kompakt-t2informatik.jpg)

***

## Merkmale eines Netzplans  

- **Darstellung von Aktivitäten und Abhängigkeiten**  
- **Ermittlung der Projektlaufzeit**  
- **Identifikation des kritischen Pfads**  
- **Optimierung von Abläufen und Ressourcen**  

***

## Anwendung von Netzplänen  

- **Projektmanagement** (z. B. Bauprojekte, Softwareentwicklung)  
- **Produktion und Logistik**  
- **Eventplanung** (z. B. Messen, Produktlaunches)  

***

## Berechnung im Netzplan  

Ein Netzplan ermöglicht die **Berechnung wichtiger Zeitwerte**:  

| Wert              | Bedeutung |
|------------------|------------|
| **Frühester Anfang (FAZ)** | Frühestmöglicher Start eines Vorgangs |
| **Frühestes Ende (FEZ)** | FAZ + Dauer |
| **Spätester Anfang (SAZ)** | Späteste Startzeit, ohne Projektverzögerung |
| **Spätestes Ende (SEZ)** | SAZ + Dauer |
| **Pufferzeit** | Differenz zwischen spätestem und frühestem Start (SAZ - FAZ) |

### Beispiel für eine Berechnung  

Ein Projekt besteht aus **drei Vorgängen**:  

| **Vorgang** | **Dauer (Tage)** | **Vorgänger** |
|------------|----------------|--------------|
| A          | 5              | -            |
| B          | 3              | A            |
| C          | 4              | B            |

#### Schritt 1: Berechnung der frühesten Zeiten  

- **FAZ(A) = 0**, **FEZ(A) = 5**  
- **FAZ(B) = FEZ(A) = 5**, **FEZ(B) = 8**  
- **FAZ(C) = FEZ(B) = 8**, **FEZ(C) = 12**  

#### Schritt 2: Berechnung der spätesten Zeiten  

- **SEZ(C) = 12**, **SAZ(C) = SEZ(C) - Dauer = 12 - 4 = 8**  
- **SEZ(B) = SAZ(C) = 8**, **SAZ(B) = SEZ(B) - Dauer = 8 - 3 = 5**  
- **SEZ(A) = SAZ(B) = 5**, **SAZ(A) = SEZ(A) - Dauer = 5 - 5 = 0**  

#### Kritischer Pfad  

Da **kein Puffer** vorhanden ist (FAZ = SAZ bei allen Vorgängen), ist der **kritische Pfad**:  

**A → B → C** mit einer Gesamtprojektdauer von **12 Tagen**.  

---

## Vorteile & Nachteile von Netzplänen  

| **Aspekt** | **Vorteile** | **Nachteile** |
|------------|-------------|--------------|
| **Transparenz** | Klare Darstellung von Abhängigkeiten | Erstellen kann komplex sein |
| **Optimierung** | Identifikation von Engpässen | Änderungen erfordern Anpassungen |
| **Zeitmanagement** | Berechnung von Pufferzeiten möglich | Nicht alle Projekte sind geeignet |
| **Effizienz** | Hilft, Ressourcen gezielt einzusetzen | Aufwendiger als Gantt-Diagramme |

***

## Quellen  

- [Wikipedia - Netzplantechnik, 12.03.2025](https://de.wikipedia.org/wiki/Netzplantechnik)  
- [T2Informatik - Netzplan, 12.03.2025](https://t2informatik.de/wissen-kompakt/netzplan/)