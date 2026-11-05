# A320 Flight Controls – Sidestick-Signale und Rechner

[← Zurück zur Artikelübersicht](README.md)

*Stand: 10/2026 · Rubrik: Nice to know*

---

## Überblick: 7 Flugsteuerungsrechner

Die A320 hat sieben Flugsteuerungsrechner: zwei ELAC, drei SEC und zwei FAC. ELAC
und SEC bewegen alle Steuerflächen für Roll und Pitch, die FACs sind für
Seitenruder und Flight Envelope zuständig.

Im Roll ist ELAC 1 normalerweise aktiv, ELAC 2 Standby. Die drei SECs sind
baugleich; ihre Funktion ergibt sich aus dem Einbauplatz und den dort
angeschlossenen Aktuatoren.

| Rechner | Name | Roll | Pitch | Yaw / Sonstiges |
|---------|------|------|-------|-----------------|
| ELAC 1 + 2 | Elevator Aileron Computer | Querruder; Roll-Befehle für Spoiler an die SECs | Höhenruder und THS (normal: ELAC 2 aktiv, ELAC 1 Standby) | berechnet im Normal Law Yaw Damping und Turn Coordination |
| SEC 1 + 2 | Spoiler Elevator Computer | Spoiler | Backup für Höhenruder und THS | Speedbrakes, Ground Spoiler |
| SEC 3 | Spoiler Elevator Computer | Spoiler | keine Funktion | Speedbrakes, Ground Spoiler |
| FAC 1 + 2 | Flight Augmentation Computer | – | – | Seitenruder-Funktionen, Speeds, Warnungen (normal: FAC 1 aktiv, FAC 2 Standby) |

---

## COM und MON: zwei Kanäle pro Rechner

Jeder ELAC, SEC und FAC hat zwei Kanäle, die sich gegenseitig kontrollieren.

- **COM (Command):** berechnet die Befehle und steuert die Aktuatoren.
- **MON (Monitor):** rechnet parallel dieselbe Aufgabe und vergleicht mit COM.

Weichen die Ergebnisse ab, schaltet sich der Rechner (bzw. die betroffene Achse)
ab und der nächste übernimmt. Wichtig: COM und MON bekommen je ein eigenes
Poti-Signal vom Sidestick, also zwei unabhängig gemessene Werte.

> [!NOTE]
> **Begriff:** Bei Airbus heisst es COM/MON, nicht „Primary/Monitor“. „PRIM“ ist
> bei A330/A340/A350 ein eigener Rechnertyp.

---

## Sidestick-Potis: 10 Roll, 8 Pitch

Pro Sidestick gibt es 10 Roll-Potis und 8 Pitch-Potis. Jedes Poti ist mit genau
einem Kanal eines Rechners verbunden: Roll geht an 5 Rechner × 2 Kanäle, Pitch an
4 Rechner × 2 Kanäle.

Mit zwei Sidesticks sind es im Flugzeug insgesamt 20 Roll- und 16 Pitch-Potis.
Die genaue Poti-Nummerierung und Pin-Belegung steht im AMM (ATA 27-92).

| Rechner | Roll COM | Roll MON | Pitch COM | Pitch MON |
|---------|----------|----------|-----------|-----------|
| ELAC 1 | ja | ja | ja | ja |
| ELAC 2 | ja | ja | ja | ja |
| SEC 1 | ja | ja | ja | ja |
| SEC 2 | ja | ja | ja | ja |
| SEC 3 | ja | ja | – | – |
| FAC 1 + 2 | – | – | – | – |
| **Summe** | **5** | **5** | **4** | **4** |

### Warum Pitch weniger Signale hat

SEC 3 steuert keine Höhenruder-Aktuatoren und braucht deshalb kein Pitch-Signal.
Ein Rechner bekommt nur die Signale der Achse, in der er eine Steuerfläche bewegt.

- **Roll:** 5 Spoiler pro Flügel, verteilt auf alle drei SECs (SEC 1: Spoiler 3 + 4,
  SEC 2: Spoiler 5, SEC 3: Spoiler 1 + 2). Spoiler 2 ist ein Roll-Spoiler, also
  braucht SEC 3 das Roll-Signal.
- **Pitch:** Jedes Höhenruder hat zwei Stellzylinder, insgesamt vier. Diese werden
  von ELAC 1/2 und SEC 1/2 angesteuert.

Für Pitch wird die geforderte Sicherheit mit vier Rechnern plus mechanischer
Trimmung erreicht. Ein fünfter Rechner bräuchte zusätzliche Servos, Verkabelung
und Hydraulik im Leitwerk.

> [!TIP]
> **Merkhilfe zum Vergleich:** Roll = 5 Rechner, kein mechanisches Backup.
> Pitch = 4 Rechner + mechanische Trimmung.

---

## FAC 1 + 2

Die FACs bekommen keine Sidestick-Signale. Die Seitenruderpedale sind mechanisch
mit dem Seitenruder verbunden; die FACs wirken über drei elektrische „Helfer“
zusätzlich darauf ein.

| Funktion | Was sie tut |
|----------|-------------|
| Yaw Damper | Dämpft Dutch Roll, Turn Coordination. Im Normal Law berechnet der ELAC die Befehle, der FAC setzt sie um; im Alternate Law rechnet der FAC selbst. |
| Rudder Trim | Manuell über RUD TRIM oder automatisch durch den Autopiloten (z. B. Triebwerksausfall). |
| Rudder Travel Limiter | Verstellbarer mechanischer Anschlag, je ein Motor pro FAC. Ca. 25° bis 160 kt, ca. 3,5° bei 380 kt. |

Fallen beide FACs aus, bleibt der Anschlag stehen; laut FCOM ist nach dem
Ausfahren der Slats wieder voller Ausschlag verfügbar.

**Flight-Envelope-Funktionen:** Speeds auf dem PFD (VLS, VFE, VMAX, Green Dot, S/F,
VSW), Alpha-Floor-Erkennung, Low Energy Warning („SPEED, SPEED, SPEED“), reaktive
Windshear-Warnung, Gewicht und Schwerpunkt.

---

## Mechanical Backup

Das Mechanical Backup arbeitet ganz ohne Rechner und ist die letzte
Rückfallebene, wenn alle Flugsteuerungsrechner oder die elektrische Versorgung
ausfallen.

- **Pitch:** Trimmrad im Cockpit, über Seilzüge direkt auf die THS.
- **Yaw:** Seitenruderpedale, über Seilzüge auf das Seitenruder.
- **Roll:** keine mechanische Steuerung; Rollen nur indirekt über das Seitenruder.

---

## Merksätze

> 1. Roll = 5 Rechner × 2 Kanäle = 10 Potis. Pitch = 4 Rechner × 2 Kanäle = 8 Potis.
> 2. SEC 3 fehlt bei Pitch, weil er nur Spoiler steuert.
> 3. COM steuert, MON kontrolliert, jeder mit eigenem Poti-Signal.
> 4. FACs: Seitenruder und Flight Envelope, keine Sidestick-Signale.
> 5. Mechanical Backup: Trimmrad (Pitch) und Pedale (Yaw), kein Roll.
> 6. Im Normal Law befiehlt der Sidestick eine Rollrate, keinen Ruderausschlag.
>    Neutraler Stick = „halte, was ich habe“.

---

*Dieser Artikel dient der Information und ersetzt keine offiziellen Unterlagen.
Es gilt der [Haftungsausschluss](../README.md#️-haftungsausschluss).*
