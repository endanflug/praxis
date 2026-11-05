# A320 Radio Altimeter

[← Zurück zur Artikelübersicht](README.md)

*Stand: 10/2026 · Rubrik: Nice to know*

---

## Messprinzip: FMCW

Der RA misst die Höhe nicht mit Pulsen, sondern über eine Frequenzverschiebung
(FMCW, Frequency Modulated Continuous Wave). Er sendet im C-Band zwischen 4,2 und
4,4 GHz.

- **Frequenzrampe:** Die Sendefrequenz steigt linear an. Während das Echo unterwegs
  ist (bei 50 ft rund 100 ns), hat sich der Sender schon weiterbewegt.
- **Beat-Frequenz:** Die Differenz zwischen aktuellem Sendesignal und Echo ist
  proportional zur Höhe. Sie ist die in eine Frequenz übersetzte Laufzeit.
- **Warum nicht Laufzeit direkt:** 100 ns auf Zentimeter genau zu stoppen wäre
  extrem aufwendig. Eine Frequenz im Kilohertzbereich lässt sich einfach und
  präzise auswerten.

| Modulationsart | Prinzip |
|----------------|---------|
| Sägezahn | Rampe hoch, dann Sprung zurück |
| Dreieck | Rampe hoch und wieder runter, trennt Höhe und Doppler |
| Konstante Beat-Frequenz | Rampendauer wird nachgeregelt, Höhe steckt in der Rampendauer (klassische Collins-Bauart) |

Welche Variante im eigenen A320 steckt, steht im CMM des verbauten Geräts. Linear
ist die Rampe immer. Eine universelle Zahl wie «exakt 3 kHz bei 50 ft» gibt es
nicht.

---

## Datenübertragung: ARINC 429

Die Radiohöhe geht als 32-Bit-Wort unter Label 164 (oktal) über den
ARINC-429-Bus.

| Bits | Inhalt |
|------|--------|
| 1–8 | Label 164 (Radio Height) |
| 9–10 | SDI (Quellkennung) |
| 11–28 | Datenfeld (Höhe, binär) |
| 29 | Vorzeichen |
| 30–31 | SSM (Status: gültig, Test, Fehler) |
| 32 | Parität (odd) |

Das Paritätsbit erkennt Übertragungsfehler, es korrigiert sie nicht. Fehlerhafte
Wörter werden verworfen.

---

## Der Dip beim Rotieren

Beim Rotieren fällt die RA-Anzeige kurz um 1–2 ft, bevor sie steigt. Ursache ist
reine Geometrie: Die Antennen sitzen am hinteren Unterrumpf, etwa auf Höhe der
hinteren Cargo Door, also hinter dem Hauptfahrwerk. Das Flugzeug dreht sich um
das Hauptfahrwerk, jeder Punkt dahinter senkt sich ab (dieselbe Geometrie wie
beim Tailstrike).

$$
h(\theta) \approx h \cos\theta - d \sin\theta
$$

Mit d ≈ 5 m Abstand hinter dem Hauptfahrwerk und θ = 7° Pitch ergibt sich ein
Absinken von rund 0,6 m, also etwa 2 ft.

- **Keine Cosinus-Korrektur durch die ADIRUs:** Die breite Abstrahlkeule und die
  Auswertung des frühesten Echos liefern ohnehin den kürzesten Abstand zum Boden.
- **Federbeine spielen kaum eine Rolle:** Lastverschiebung und steigender Auftrieb
  heben sich weitgehend auf, es geht um wenige Zentimeter.
- **Danach steigt die Anzeige:** Sobald das Hauptfahrwerk abhebt, wächst der
  Höhengewinn schneller als der geometrische Verlust.

---

## Merksätze

> - RA = FMCW: Frequenzverschiebung statt Pulslaufzeit.
> - Label 164, Parität erkennt, korrigiert nicht.
> - Dip beim Rotieren = Antenne hinter der Drehachse, nichts anderes.
> - Beim Durchstarten tief über Grund ist der RA oft das einzige Instrument, das
>   die echte Höhe kennt (siehe AirHub CDG 2022).

---

*Dieser Artikel dient der Information und ersetzt keine offiziellen Unterlagen.
Es gilt der [Haftungsausschluss](../README.md#️-haftungsausschluss).*
