# A320 Wetterradar und Windshear

[← Zurück zur Artikelübersicht](README.md)

*Stand: 10/2026 · Rubrik: Nice to know*

---

## Puls-Doppler

Das Wetterradar ist ein Pulsradar im X-Band (um 9,3 GHz). Die Entfernung kommt aus
der echten Laufzeit, die Geschwindigkeit aus dem Doppler-Effekt.

- **Laufzeit:** pro Seemeile rund 12,4 µs hin und zurück, bei 100 NM gut 1 ms.
- **Doppler:** $f_D = 2v / \lambda$. Bei 3,2 cm Wellenlänge verschiebt ein Tropfen
  mit 10 m/s die Frequenz um etwa 620 Hz.
- **Phasenvergleich:** Ein Puls dauert nur rund 1 µs, zu kurz für 620 Hz. Deshalb
  sendet das Radar kohärent und vergleicht die Phase des Echos von Puls zu Puls.
- **Range Gates:** Jede Entfernungszelle bekommt über viele Pulse eine eigene
  Zeitreihe, eine FFT liefert ihr Doppler-Spektrum.
- **Bodenechos:** Ihre Doppler-Verschiebung ist aus den ADIRU-Daten bekannt und
  wird herausgefiltert.

### Das Doppler-Dilemma

Die Pulswiederholfrequenz (PRF) bestimmt zwei Grenzen, die sich ausschliessen.

| PRF | Max. eindeutige Reichweite | Max. eindeutige Geschwindigkeit |
|-----|----------------------------|---------------------------------|
| 1'000 Hz | 150 km (≈ 81 NM) | ≈ 8 m/s |
| 6'000 Hz | 25 km (≈ 13 NM) | ≈ 48 m/s |

Niedrige PRF für Wetter auf Distanz, hohe PRF für Windshear im Nahbereich.

---

## Turbulenz und PWS

Das PWS schaut voraus, braucht dafür aber reflektierende Teilchen.

- **Turbulenz:** gemessen über die Spektrumsbreite. Ruhiger Regen bewegt sich
  einheitlich, in Turbulenz streuen die Tropfengeschwindigkeiten stark. Über einem
  Schwellwert wird die Zelle magenta markiert.
- **Predictive Windshear:** Das Radar misst entlang des Flugwegs die horizontale
  Windgeschwindigkeit in aufeinanderfolgenden Zellen. Starke Änderung auf kurzer
  Distanz, etwa Gegenwind vorne und Rückenwind dahinter, ergibt einen hohen
  F-Factor und eine Warnung, bevor man einfährt.
- **Empfindlicher als das Wetterbild:** Schwache Echos wie Virga bei trockenen
  Microbursts liegen oft unter der Darstellungsschwelle, reichen dem PWS aber.
- **Grenze:** In völlig partikelfreier Luft sieht das PWS nichts. Bei echtem CAVOK
  fehlt es aber meist auch an Konvektion, der Hauptursache für Microbursts.
- **Unsichtbar bleiben:** Gelände- und Lee-Scherung, Low-Level-Jet über
  Inversionen, Seewindfronten, Böenfronten ferner Gewitter bei blauem Himmel.

---

## Reaktive Windshear (FAC)

Die FACs berechnen laufend den Energiezustand aus Luft- und Trägheitsdaten der
ADIRUs. Sinkt er wegen der Luftmasse unter einen Schwellwert, kommt die Warnung.

- **Gemessen:** horizontale Windänderung (Fahrtänderung, die die Trägheitsdaten
  nicht erklären) und Vertikalwind (Flugweg, Pitch, Anstellwinkel).
- **Aktiv:** beim Start ab etwa 3 s nach dem Abheben bis 1300 ft RA, im Anflug von
  1300 ft bis 50 ft RA, mindestens CONF 1 (Werte laut FCOM prüfen).
- **Nur Energieverlust:** Leistungssteigernde Scherung löst nichts aus. Bei einem
  Microburst kommt aber zuerst Gegenwind, ein unerklärlicher Fahrtzuwachs im
  Anflug ist also selbst ein Warnsignal.
- **Reaktiv:** Das Flugzeug ist bereits in der Scherung. Antwort: TOGA, SRS im
  Windshear-Modus.
- **Hilfen:** Speed-Trend-Pfeil, GS Mini in Managed Speed.

> [!NOTE]
> Die Systeme ergänzen sich: PWS schaut voraus, braucht aber Teilchen. Die FACs
> brauchen keine Teilchen, sehen aber nur, was das Flugzeug schon erlebt.

---

## Callouts

**Faustregel:** «Ahead» und «Monitor Radar Display» kommen vom PWS, das dreifache
«WINDSHEAR» von den FACs.

| System | Stufe | Aural | PFD |
|--------|-------|-------|-----|
| PWS | Warning (Start) | WINDSHEAR AHEAD, WINDSHEAR AHEAD | W/S AHEAD rot |
| PWS | Warning (Anflug) | GO AROUND, WINDSHEAR AHEAD | W/S AHEAD rot |
| PWS | Caution | MONITOR RADAR DISPLAY | W/S AHEAD amber |
| FAC (reaktiv) | Warning | WINDSHEAR, WINDSHEAR, WINDSHEAR | WINDSHEAR rot |

---

*Dieser Artikel dient der Information und ersetzt keine offiziellen Unterlagen.
Es gilt der [Haftungsausschluss](../README.md#️-haftungsausschluss).*
