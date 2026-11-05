# HEMA VOR Y 33 – Raw-Data-Training

[← Zurück zur Artikelübersicht](README.md)

*Stand: 10/2026 · Rubrik: Praxis – wie man es macht*

> **Kurz gesagt:** Der Teardrop wird mit rund 10° Bank geflogen, nicht mit 20–25°.
> Wer die Bank hält, läuft am FAF D8.2 MAK sauber auf 326° ein.

Alle Werte ohne Wind, Basis Lido 7-60 vom 11. Juli 2024 (Aktualität prüfen).

> [!CAUTION]
> Trainingsunterlage, nicht für die Navigation. Verbindlich ist die aktuelle
> Anflugkarte.

---

## 1. Eckdaten VOR Y 33

MAK DVOR/DME 115.5 steht hinter der Bahn: Die Schwelle 33 liegt bei D2.6 MAK. Der
ganze Anflug wird auf die Station zu geflogen, die DME zählt bis 2.6 herunter.

| Segment | Kurs / Radial | Höhe | Ende |
|---------|---------------|------|------|
| Über MAK | – | 3500 | Beginn Outbound |
| Outbound | R116 | Sinkflug 3500 → 2000 | D8.2 MAK |
| Rechtskurve | 210° (116° → 326°) | 2000 | Inbound 326° |
| FAF | 326° (R146 inbound) | at 2000 | D8.2 MAK |
| Final | 326°, 2,87° | bis MDA 580 | MAPt D2.6 MAK = THR |

**Final** 5,6 NM. Bei 150 kt GS rund 2:15 und 760 ft/min. MDA 580 ft (MDH 350),
RVR 900 m, THR 233 ft. PAPI 3,0°.

| D MAK | 8.2 | 8 | 7 | 6 | 5 | 4 |
|-------|-----|---|---|---|---|---|
| Höhe (ft) | 2000 | 1940 | 1640 | 1330 | 1020 | 720 |

**Fehlanflug:** 326° bis mindestens 1300, Rechtskurve direkt MAK, Steigflug 2500.
Holding über MAK, Inbound 146°, Rechtskurven.

---

## 2. Faustregeln Kurvenradius bei 150 kt

Bei 150 kt und 20° Bank ist der Radius rund 0,9 NM. Das muss man für jeden Visual
kennen.

$$
R = \frac{V^2}{g \cdot \tan\varphi}
$$

| Bank | Radius | 90°-Kurve | 180°-Wendung (seitlicher Versatz) |
|------|--------|-----------|-----------------------------------|
| 25° | ca. 0,7 NM | 0,7 NM vorher eindrehen | ca. 1,4 NM |
| 20° | ca. 0,9 NM | 0,9 NM vorher eindrehen | ca. 1,8 NM |
| 10° | ca. 2 NM | – | ca. 4 NM |

Die Werte gelten für die TAS. An einem heissen Tag in Marsa Alam liegt sie schon in
niedriger Höhe ein paar Knoten über der IAS.

---

## 3. Die 210°-Kurve: 10° Bank

Ende Outbound (R116, D8.2) und FAF (R146, D8.2) liegen rund 4,2 NM auseinander. Das
ist der Durchmesser der Kurve, also Radius rund 2 NM. Bei 150 kt ergibt das rund
10° Bank.

$$
\text{Abstand} = 2 \cdot 8{,}2 \cdot \sin 15^\circ \approx 4{,}2\ \text{NM}
\quad\Rightarrow\quad R \approx 2\ \text{NM}
\quad\Rightarrow\quad \varphi \approx 10^\circ
$$

Die Kurve ist rund 8 NM lang und dauert gut 3 Minuten. Wer aus Gewohnheit mit
20–25° eindreht, steht vor dem FAF quer zum Final.

### Kontrollpunkt Kurvenmitte

| Punkt | Heading | Radial | DME |
|-------|---------|--------|-----|
| Beginn Kurve | 116° | R116 | 8,2 |
| Mitte Kurve | ca. 220° | ca. R131 | ca. 10,7 |
| Ende Kurve (FAF) | 326° | R146 | 8,2 |

Wer bei Heading 220 auf etwa R131 und D10.7 ist, liegt richtig: Bank halten,
weiterfliegen.

### Warum die Nadel täuscht

Die Nadel zeigt Winkel, nicht Strecke. Auf 8 NM ist ein Grad Radial rund 0,14 NM,
voller Ausschlag (10°) rund 1,4 NM. Die Nadel wird also mitten in der Kurve
lebendig und läuft dann langsam und gleichmässig herein. **Nicht nervös werden,
nicht nachziehen: 10° halten.**

---

## 4. Eindrehen über MAK auf R116

Bei Anflug mit Heading ca. 090 auf MAK sind es nur 26° Kursänderung. Eingedreht
wird im Cone, wenn die Nadel weg ist, nicht erst wenn TO/FROM umspringt.

| Vorhalt (26°-Kurve) | 180 kt | 250 kt |
|---------------------|--------|--------|
| bei 25° Bank | ca. 0,25 NM (ca. 5 s) | ca. 0,45 NM (ca. 7 s) |
| bei 20° Bank | ca. 0,3 NM (ca. 6 s) | ca. 0,6 NM (ca. 8 s) |

Die DME hilft hier nicht: Auf 3500 ft zeigt sie direkt über der Station noch rund
0,5 NM Schrägentfernung. Die Vorhaltewerte liegen genau in dem Bereich, den sie
nicht auflöst, und genau im Cone über dem VOR.

---

## 5. Displays: beide ROSE VOR

Beide NDs auf ROSE VOR, kein MAP. Der MAP zeigt die FMS-Position, also RNAV. Wer
auf den MAP schaut, fliegt einen RNAV-Anflug mit VOR-Deko. Nur mit ROSE VOR sieht
man, was das VOR wirklich sagt, und muss die Geometrie aus diesem Blatt im Kopf
haben.

---

*Dieser Artikel gibt persönliche Erfahrungen wieder und ersetzt keine offiziellen
Unterlagen. Es gilt der [Haftungsausschluss](../README.md#️-haftungsausschluss).*
