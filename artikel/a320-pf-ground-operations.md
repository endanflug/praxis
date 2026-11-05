# A320 PF Ground Operations

[← Zurück zur Artikelübersicht](README.md)

*Stand: 10/2026 · Rubrik: Praxis – wie man es macht*

> **Kurz gesagt:** Technik und Arbeitsweise des PF am Boden – von der
> Startvorbereitung bis zum Startlauf und von der Landung bis zur Parkposition.
> Tempo entsteht durch Vorbereitung, nicht durch Hetzen.

---

# Teil 1: Departure

## General

Dieses Kapitel beschreibt Technik und Arbeitsweise des PF am Boden, von der
Startvorbereitung bis zum Startlauf, für den A320 mit CFM-Triebwerken. Es ergänzt
die SOPs um das *Warum* und um Erfahrungen aus der Praxis.

Verbindlich sind FCOM und OM-B. Alle Zahlenwerte hier sind Richtwerte zur
Orientierung, nicht Engineering-Daten.

Grundhaltung: vorausschauend arbeiten, jeden Schritt bewusst ausführen und
tatsächlich prüfen, statt aus Gewohnheit zu bestätigen. Tempo entsteht durch
Vorbereitung, nicht durch Hetzen.

---

## Before Start

### Taxi Route Briefing

Der PF erarbeitet die zu erwartende Taxi Route vorher in Ruhe und erzählt sie dem
PM in eigenen Worten.

- Nicht von der Karte vorlesen: Wer abliest, schaut zur Karte statt zum Kollegen.
- Der PM hat idealerweise bereits einen eigenen Überblick und gleicht ab, statt
  zum ersten Mal zuzuhören.
- Im Briefing festlegen, wann der Flight Control Check geplant ist (vor dem
  Rollen oder während des Rollens). Prüfen, ob die Route dafür einen geeigneten
  Geradeausabschnitt bietet.
- An Flughäfen mit hoher Verkehrsdichte das zügige Anrollen nach der Takeoff
  Clearance ansprechen (siehe [High Density Operations](#high-density-operations)).

---

## Engine Start

Ab MASTER ON gibt es für den PF nur noch diesen Engine Start. Die FADEC steuert
und meldet fast alles, Aufgabe des PF ist die lückenlose Überwachung, nicht das
Verlassen auf die FADEC.

### Vorbereitung

- **Before Start Flow:** Items dann ausführen und prüfen, wenn sie dran sind.
  Nicht auf „habe ich vorhin schon gemacht“ verlassen.
- **ENG MODE Selector auf IGN/START:** Die Packs schliessen, damit die APU Bleed
  Air für den Starter zur Verfügung steht, und die FADECs werden versorgt. Ein
  paar Sekunden geben, hörbar am Leiserwerden im Cockpit. Es funktioniert auch
  ohne Warten, aber man hetzt hier nicht durch.
- Information an Ground Crew und PM (Details gemäss OM-B).

### Ablauf und Überwachung

Nach MASTER ON den Blick auf dem ENG Display halten. Kein Cabin Call, kein
Kartensortieren, keine MCDU-Eingaben. Jedes Ereignis aktiv bestätigen: Passiert
das wirklich?

1. Start Valve offen, N2 beginnt zu steigen.
2. Ca. 16 % N2: Ignition vorhanden?
3. Ca. 22 % N2: Fuel Flow vorhanden? EGT steigt (Light-up)?
4. Ca. 50 % N2: Start Valve und Ignition geschlossen? Ein Start Valve kann auch
   hängen.
5. N2 beschleunigt weiter bis Idle.
6. Generator schaltet zu (hörbares Klacken).
7. Graue Hinterlegung der N2-Anzeige verschwindet: Start complete.

Erst danach das zweite Triebwerk, mit gleichem Ablauf und gleicher Disziplin.

> [!NOTE]
> Der gesamte Startablauf wird über N2 überwacht, da der Starter die
> Hochdruckwelle antreibt. N1 dreht mit, ist aber nicht der Leitparameter.

---

## After Start

Der Engine Start ist abgeschlossen, wenn auf beiden N2-Anzeigen die graue
Hinterlegung verschwunden ist. Eine AVAIL-Anzeige, wo vorhanden, ist eine
zusätzliche Bestätigung, aber nicht der Trigger.

### Ablauf

1. ENG MODE Selector auf NORM.
2. APU BLEED OFF.
3. PF After Start Flow beenden.
4. Ground Crew informieren und entlassen.
5. PM führt seinen Flow durch.
6. Signal vom Boden (Pin gezeigt): After Start Checklist.

### Pitch Trim Check

Referenz für die Pitch Trim ist der TO CG aus dem Loadsheet, gemerkt oder
nachgesehen. Die Trimmanzeige wird gegen diesen Wert geprüft, im Rahmen der
Ablesegenauigkeit.

- Die Fuel Page höchstens danach zur zusätzlichen Bestätigung nutzen, nie vorher.
  Wer den Wert vorher kennt, sieht ihn auch dann, wenn die Trimmung daneben steht
  (Confirmation Bias).
- Der CG auf der Fuel Page beruht auf den von der Crew eingegebenen Daten. Ein
  Eingabefehler steht also auch dort. Das Loadsheet ist die unabhängige Quelle.
- Keine Werte ansagen, die man auf der Anzeige nicht ablesen kann. Zehntelprozente
  sind auf der Trimmanzeige nicht erkennbar.
- Technik: Nicht nur die Linie suchen, sondern abzählen, zwischen welchen
  Hauptmarkierungen der Sollwert liegt.

> [!WARNING]
> **Common Error:** Wert auf der Fuel Page ablesen (z. B. 27,3 %), dann kurz auf
> die Trimmanzeige schauen und den Wert bestätigen. Ein Versatz von genau einer
> Hauptmarkierung (5 %) wird dabei leicht übersehen, weil die Anzeige auf einer
> dicken Linie steht und plausibel wirkt.

---

## Flight Control Check im Stand

Der Flight Control Check ist sicherheitskritisch und wird ohne Eile
durchgeführt. Er prüft nicht, ob sich etwas bewegt, sondern ob volle Ausschläge
erreicht werden.

### Sidestick (PF)

- Sidestick in jede Richtung bis zum Anschlag bewegen und **dort halten**, bis der
  PM die volle Auslenkung ausgerufen hat.

### Rudder (PF)

- PEDALS DISC mit dem Handballen drücken, die Finger bleiben am Tiller.
- Diese Handhaltung **immer** anwenden, auch im Stillstand. So ist die Technik
  identisch, egal ob der Check vor oder während des Rollens erfolgt, und die
  Kontrolle über den Tiller bleibt jederzeit erhalten.
- Rudder gleichmässig bis zum Anschlag, Richtwert zwei bis vier Sekunden. Eine
  Sekunde ist zu schnell, fünf zu langsam.

### Sidestick (PM)

- Der PM beginnt erst, wenn der PF komplett fertig ist.

> [!WARNING]
> **Common Error:** Der PM beginnt mit seinem Sidestick-Check, während der PF noch
> den Rudder prüft. Das teilt die Aufmerksamkeit bei einem Check, der ungeteilte
> Aufmerksamkeit verdient, erzeugt logisch nicht zusammenpassende Bewegungen auf
> der F/CTL Page und bringt praktisch keinen Zeitgewinn.

---

## Taxi

Rollen heisst vorausschauend fahren: wenige, bewusste Schub- und Bremsvorgänge,
klare kurze Ansagen und ein Licht, das nach aussen zuverlässig den Zustand des
Flugzeugs zeigt.

### Losrollen

1. Taxi Clearance erhalten.
2. PM schaut raus: „Clear right side“.
3. **Danach** PF: „Clear left side“. Der Call des PF ist der Startpunkt für die
   Bewegung. Vorher werden keine Bremsen gelöst.
4. Taxi Light ON, **immer zuerst**, als Signal nach aussen.
5. Parking Brake OFF.
6. Kurz abwarten, ob das Flugzeug von selbst anrollt. Schub nur, wenn nötig.

**Schubregel:** Falls Schub zum Anrollen nötig ist, ideal 30–35 % N1,
**niemals über 40 %**. Danach Geduld, das Anrollen kann einen Moment dauern.

> [!WARNING]
> **Common Error:** Der PF macht seinen Call zuerst und beginnt bereits zu rollen,
> bevor der PM seine Seite bestätigt hat.

### Brake Check

- Sobald das Flugzeug rollt, Schub stehen lassen.
- Kurz und gefühlvoll gegenbremsen, nur bis Bremswirkung spürbar ist. Nicht
  anhalten.
- Jede Beschleunigung belastet das Triebwerk. Einzeln ist der Effekt gering, in
  der Summe über die Einsatzzeit nicht. Vermeidbare Schubwechsel werden daher
  grundsätzlich vermieden.

> [!WARNING]
> **Common Error:** Schub auf Idle, Brake Check, dann erneut Schub. Unnötige
> Schubwechsel und ein unruhiges Anrollen ohne jeden Vorteil.

### Navigation und Ansagen

- Der PF kündigt die nächsten Abzweigungen kurz an („hier links“, „die zweite
  rechts“), ohne lange Erklärungen.
- Der PM erkennt, dass der PF einen Plan hat, und kann gezielt abgleichen. Das
  entlastet erheblich und deckt Fehler auf, bevor die Kurve gefahren ist.

### Centerline und Kurven

- Ziel ist die Centerline. Richtwert: Linie ungefähr zwischen den Displays. Die
  exakte Referenz hängt von Sitzposition und Augenhöhe ab.
- Standardkurve mit Bugrad auf der Linie: die Linie etwa über das kurveninnere
  Knie laufen lassen.
- Das Einlenken wirkt optisch zu spät. Grund: Das Bugrad liegt ca. 2,5 m hinter
  dem Piloten. Das ist geometrisch korrekt.
- Am Anfang mit kleinen Korrekturen arbeiten. Das Bugrad ist auf den Centerline
  Lights hörbar, diese Rückmeldung für die eigene Sitzposition einprägen.

### Taxi Speed

- Geschwindigkeit laufen lassen bis ca. 20 bzw. 30 kt, je nach Bereich.
- Dann gefühlvoll auf ca. 10 kt abbremsen und wieder laufen lassen.
- Niemals die Bremse schleifen lassen.

> [!CAUTION]
> Starkes Bremsen nur im Notfall. Die Kabinenbesatzung ist während des Rollens in
> der Regel nicht angeschnallt, Verletzungsgefahr.

### Clear Calls beim Rollen

- „Clear right/left“ gezielt einsetzen: bei 180°-Turns, in unübersichtlichen
  Situationen und wenn die Seite wirklich nicht einsehbar war.
- Nicht routinemässig an jeder Kreuzung, die beide Piloten längst überblickt
  haben.

> [!WARNING]
> **Common Error:** Standardmässiges „Clear right“ an jeder Abzweigung, auch beim
> Linksabbiegen oder bei frei einsehbaren Kreuzungen. Der Call verliert seine
> Bedeutung und wird nicht mehr bewusst wahrgenommen.

### Abstände

- Vorausschauend aufschliessen: Zu viel Abstand reduziert die Kapazität hinter
  einem und kann den Verkehrsfluss stocken lassen, besonders bei hohem
  Verkehrsaufkommen.
- Red Bar / Holding Point: Die Linie darf optisch bis an die Nase heranreichen.
- Zum vorausstehenden Flugzeug: Richtwert etwas weniger als eine Flugzeuglänge.

> [!CAUTION]
> Jet Blast des vorausstehenden Flugzeugs beim Anrollen berücksichtigen,
> besonders hinter grösseren Typen.

> [!WARNING]
> **Common Error:** Zu grosser Abstand zur Red Bar oder zum vorausstehenden
> Flugzeug.

### Anhalten

- Reihenfolge: **erst Parking Brake SET, dann Taxi Light OFF**.
- Gegenstück zum Losrollen (erst Licht an, dann Parking Brake OFF).
- Es darf nie der Zustand „Parking Brake OFF, Licht aus“ entstehen. Das Licht
  signalisiert nach aussen, dass mit Bewegung zu rechnen ist.

---

## Flight Control Check während des Rollens

Während des Rollens gilt eine strikte Arbeitsteilung: Der PF steuert und schaut
raus, der PM überwacht die F/CTL Page. Wer dem PM dabei nicht vertrauen will oder
kann, macht den Check vor dem Rollen.

### Planung

- Bereits im Taxi Briefing prüfen, ob auf der Route ein längerer
  Geradeausabschnitt zu erwarten ist.
- Ist das nicht der Fall: Check vor dem Rollen.
- Bei wenig Erfahrung mit dieser Technik ebenfalls eher vor dem Rollen. Der Ablauf
  ist koordinativ anspruchsvoll.

### Durchführung

- Ablauf identisch zum Check im Stand, inklusive PEDALS DISC mit dem Handballen
  und Fingern am Tiller.
- **Der PF schaut nicht auf das Display**, auch wenn der Impuls stark ist. Die
  Augen bleiben draussen.
- Das Flugzeug bleibt mit dem Tiller voll steuerbar, auch während die Pedale
  getrennt sind.

### Rudder Check

- Hier ist der Blick nach draussen besonders wichtig.
- Anspruchsvolle Koordination: z. B. rechtes Bein voll durchstrecken und
  gleichzeitig mit dem Tiller gegensteuern, um auf der Centerline zu bleiben.

> [!CAUTION]
> Trennt der PEDALS DISC nicht, lenkt der Rudderausschlag das Bugrad mit. Das wird
> nur bemerkt, wenn der PF draussen bleibt.

---

## Taxi Checklist

Die Taxi Checklist wird angefordert, wenn die Voraussetzungen erfüllt sind
**und** die Situation einen ruhigen Moment bietet.

### Voraussetzungen gemäss FCTM

- Cabin Ready
- T.O CONFIG pb pressed

Der PF muss diese Kriterien kennen und fordert die Checklist erst an, wenn beide
erfüllt sind.

### Zeitpunkt

- Zusätzlich die Situation bewerten: Wo bin ich? Wo werde ich gleich sein?
- Nicht unmittelbar vor einem Turn oder einer komplexen Stelle anfordern. Die
  Checklist enthält Head-down-Items.
- Bei vielen Turns ohne ruhigen Abschnitt: Checklist erst am Rollhalt. Lieber
  später als unter Zeitdruck.

### Durchführung

- Jedes Item tatsächlich prüfen. Die Antwort beschreibt den Ist-Zustand, nicht den
  erwarteten.
- Genau dafür wird die Checklist in einem ruhigen Moment gemacht: um die Zeit zum
  Hinschauen zu haben.

> [!NOTE]
> Der Zeitpunkt des T.O CONFIG Tests ist auch ein Instrument zur Tempokontrolle.
> Der PM (meist der Commander) kann damit Hektik bewusst herausnehmen.
> Voraussetzung ist, dass der PF die Kriterien kennt und respektiert.

> [!WARNING]
> **Common Error:** Antwort aus Routine statt aus Kontrolle. Beispiel: Das Weather
> Radar ist gemäss OM-B noch OFF (Einschalten erst am Rollhalt), die Antwort
> lautet trotzdem „On and Auto“. Das tritt bei bestimmten Items nicht vereinzelt,
> sondern systematisch auf.

---

## Before Takeoff / Line-up Checklist

Wie beim Taxi gilt: Erst der Flow, dann die Checklist. Die Checklist kontrolliert
nur, was bereits gemacht ist.

### Voraussetzungen

- Line-up clearance received
- Line-up flow pattern completed

### Hinweise

- Anrollen vom Rollhalt: gleiche Schubregel wie beim ersten Anrollen (siehe
  [Taxi](#losrollen)), auch wenn man sich wegen des Verkehrs zum Beeilen gedrängt
  fühlt.
- Packs OFF (Standard): Zeitpunkt bewusst wählen. Bei voraussichtlicher Wartezeit
  auf der Bahn, besonders bei hohen Temperaturen, den Komfort für Passagiere und
  Crew berücksichtigen.
- Landing Lights von RETRACT auf OFF: Die Lichter fahren aus, bleiben aber dunkel.
  ON erst mit der Takeoff Clearance.
- Auf den Zeitpunkt achten, zu dem die Items tatsächlich erledigt sind.

> [!NOTE]
> Der PM (meist CM1) kann den Flow bewusst etwas verzögern, um sich zuerst einen
> Überblick über die Situation zu verschaffen, bevor der Blick nach innen geht.

> [!WARNING]
> **Common Error:** Flow-Items werden erst beim Abarbeiten der Checklist
> ausgeführt. Aus Flow plus Kontrolle wird ein Read-and-do, die Kontrollfunktion
> geht verloren.

---

## Line-up ohne Meterverlust (90°-Einfahrt)

Bei vollem Tiller-Einschlag (ca. 75°) und 5–7 kt wird eingelenkt, wenn das
Cockpit ca. 9 m über die Mittellinie hinaus ist. Dann steht die Mitte zwischen
den Hauptfahrwerken am Ende auf der Mittellinie, ohne S-Korrektur und ohne
verschenkte Meter.

### Merkbild

- Nicht zur Bahnkante schauen, sondern zur Mittellinie.
- Eingelenkt wird, wenn die Mittellinie ungefähr in der Mitte des zweiten
  Seitenfensters steht, also deutlich hinter querab. Dann voller Anschlag.
- Je weiter man die Bahn hinunterschaut, desto näher rückt die Mittellinie optisch
  an querab: bei ca. 50 m Blickweite rund 10° dahinter, bei ca. 100 m rund 5°.
- Gefühl vs. Wissen: Beim Einlenken sieht man vorne oft nur noch die Bahnkante.
  Wenn es sich zu spät anfühlt, ist es wahrscheinlich richtig.

### Geschwindigkeit und Bremsen

- Vor dem Einlenken auf 5–7 kt verzögern. Das Merkbild gilt nur in diesem Bereich.
  Bei höherer Geschwindigkeit stimmt der Einlenkpunkt nicht mehr, und das Flugzeug
  kommt nicht sauber auf der Mittellinie heraus. Wer deutlich langsamer rollt, für
  den stimmt die Orientierung im Fenster ebenfalls nicht mehr.
- Ab etwa der Hälfte des Turns gefühlvoll bremsen, um den Schwung abzubauen. Keine
  Vollbremsung. Wird zu spät gebremst, dreht das Flugzeug über die Mittellinie
  hinaus.

| Rollgeschwindigkeit | Meter pro Sekunde | Strecke in 0,5 s |
|---------------------|-------------------|------------------|
| 5 kt                | 2,6 m/s           | 1,3 m            |
| 7 kt                | 3,6 m/s           | 1,8 m            |
| 10 kt               | 5,1 m/s           | 2,6 m            |

> [!CAUTION]
> Auf einer 30 m breiten Bahn bleiben vom Einlenkpunkt bis zum Rand nur ca. 6 m.

### Hintergrund: die Geometrie

Der Drehpunkt liegt auf der Verlängerung der Hauptfahrwerksachse, im Abstand R
von der Rumpfmitte:

$$
R = \frac{\text{Radstand}}{\tan(75^\circ)} \approx \frac{12{,}6\ \text{m}}{3{,}73} \approx 3{,}4\ \text{m}
$$

Damit die Hauptfahrwerksmitte nach der 90°-Kurve auf der Mittellinie steht, muss
sie beim Einlenken genau R vor der Mittellinie stehen. Mit ca. 2,5 m zwischen
Auge und Bugrad liegt das Auge ca. 15 m vor dem Hauptfahrwerk. Rechnerisch ist
das Cockpit beim Einlenken also ca. 11,7 m über die Mittellinie hinaus.

Der Praxiswert von ca. 9 m ist ein Erfahrungswert. Er berücksichtigt, dass der
volle Einschlag nicht sofort da ist und das Flugzeug weiterrollt, während der
Tiller einschlägt, sowie den Schlupf der Reifen. Je schneller man rollt, desto
früher muss man einlenken.

---

## High Density Operations

An Flughäfen mit hoher Verkehrsdichte wird nach der Takeoff Clearance ein sehr
zügiges Anrollen erwartet (z. B. Homebase: ca. 12 Sekunden). Das gelingt nur,
wenn die Schritte vorbereitet sind und überlappend statt nacheinander ausgeführt
werden.

### Vorbereitung

- Im Briefing oder spätestens im Stand absprechen.
- Bereitschaftscheck zwischen den Piloten: „Fertig?“ ist eine Abfrage, keine
  Aufforderung zum Starten.

### Nach Erhalt der Takeoff Clearance

1. Landing Lights ON. Der Tower sieht damit bereits die Reaktion.
2. Thrust Levers sofort auf ca. 50 % N1, **Füsse bleiben auf den Bremsen**.
3. Kurze Calls: „Ready“ – „Takeoff“.
4. Bremsen lösen, Takeoff Thrust setzen.

> [!NOTE]
> Werden diese Schritte nacheinander statt überlappend ausgeführt, ist die
> erwartete Zeit kaum einzuhalten. Eine Annullierung der Takeoff Clearance ist
> dann möglich.

---

## Takeoff Thrust und Rotation

Takeoff Thrust wird gefühlvoll gesetzt, und die Hand bleibt an den Thrust Levers,
bis der Schub tatsächlich steht.

### Takeoff Thrust

1. Thrust Levers auf ca. 50 % N1, Stabilisierung abwarten.
2. Bremsen lösen.
3. Hebel gefühlvoll, aber zügig auf FLX/TOGA schieben, nicht in einem Ruck. Die
   FADEC regelt zwar, aber so arbeitet man nicht.
4. Hand erst an den CM1 übergeben, wenn der Takeoff Thrust **tatsächlich steht**,
   nicht wenn die Hebel in der Raste sind.

> [!WARNING]
> **Common Error:** Hebel ruckartig nach vorne und sofort Hand weg. Während des
> Hochspulens hat niemand die Hand an den Thrust Levers.

### Rotation

- Bei V1 = VR oder minimaler Differenz: nicht beim Erreichen der Geschwindigkeit
  rotieren, sondern den Call des PM abwarten. So bleiben Entscheidung und Rotation
  sauber getrennt.

---

# Teil 2: Arrival

## Rollout

Mit dem Öffnen der Reverser ist die Entscheidung gefallen: Decision to Stop, es
gibt keine andere Option mehr. Bei den meisten Landungen reicht Idle Reverse.

1. Nach dem Touchdown das Bugrad langsam, aber ohne Verzögerung absenken.
2. Reverse unmittelbar nach dem Touchdown öffnen.
3. Die Autobrake ihre Arbeit machen lassen.
4. 70-kt-Call: Reverse Idle. Wurde nur Idle Reverse genutzt, ändert sich nichts.
5. Idle Reverse bleibt bis Taxi Speed gesetzt.

> [!NOTE]
> Die Autobrake regelt auf eine Zielverzögerung. Mehr Reverse macht die
> Bremsstrecke deshalb nicht kürzer, sondern verlagert nur Energie von den Bremsen
> auf die Triebwerke.

---

## Verlassen der Bahn

Der PF entscheidet früh, welchen Taxiway er nehmen will, und disarmt die Ground
Spoilers erst, wenn die Bahn verlassen und die Situation geklärt ist.

- Entscheidung für den Taxiway: entweder etwas stärker bremsen oder die Autobrake
  gefühlvoll übernehmen und bis zum Taxiway rollen lassen.
- Der PF disarmt die Ground Spoilers erst, wenn die Holding Line überrollt ist.
  Nicht vorher, auch wenn unklar ist, wohin es geht, oder mit ATC kommuniziert
  wird.
- Erst wenn alles geklärt ist: Spoilers DISARM. Die Spoiler haben keine Eile.

> [!WARNING]
> **Common Error:** Disarm der Ground Spoilers vor oder während des Turns beim
> Verlassen der Bahn. Die Aufmerksamkeit des PF gehört in dieser Phase nach
> draussen.

---

## After Landing und Taxi In

Nach dem Verlassen der Bahn gilt eine klare Arbeitsteilung: Der PF rollt, der PM
arbeitet seinen Flow ab.

### After Landing

- Der Disarm der Ground Spoilers durch den PF ist das Signal für den PM.
- Trotzdem beginnt der PM nicht sofort mit seinem Flow. Zuerst überwacht er:
  richtiger Taxiway, Route klar?
- Dann PM Flow.
- Der PF rollt nur und hilft nicht mit Tasten oder Schaltern.
- Fällt dem PF auf, dass etwas vergessen wurde: kurzer verbaler Hinweis an den PM.
- Flow abgeschlossen: After Landing Checklist.

### Taxi In

- Wenn nicht 100 % klar ist, wo es langgeht: anhalten.
- Ein Stopp auf dem Taxiway wirkt störend, ein Verrollen stört aber mehr und kann
  Zeit, Geld und im schlimmsten Fall Schäden kosten.

---

## Parkposition und Engine Shutdown

Nach dem Setzen der Parking Brake gibt es keine Eile mehr: Die Triebwerke werden
einzeln abgestellt und jeweils überprüft.

### Anfahren der Parkposition

- In der Regel 90°-Einfahrt.
- **Nicht in die Parkposition eindrehen, bevor alles identifiziert ist:**
  Marshaller oder Docking Guidance System (aktiv, Flugzeugtyp, Callsign). Im
  Zweifel vor dem Turn anhalten und mit ATC klären.
- **Leicht übersteuern:** Nicht eindrehen, wenn die Leitlinie querab ist, sondern
  etwas später. Nicht so ausgeprägt wie beim Line-up, aber nach demselben Prinzip.
- Lichter frühestens im Inbound Turn ausschalten, etwas später ist unkritisch.
- Licht blendet höchstens kurz und richtet keinen Schaden an, hat aber eine
  Bedeutung: Es zeigt, dass sich das Flugzeug bewegt.
- Nach Anzeige (Docking System oder Marshaller) gefühlvoll abbremsen.
- Parking Brake SET.

> [!CAUTION]
> Wird zu früh eingedreht, wird die Kurve geschnitten. Mit rund 15 m Tragfläche
> auf jeder Seite des Rumpfes kann die Flügelspitze dabei sehr nah an das Heck
> eines geparkten Flugzeugs geraten.

> [!WARNING]
> **Common Error:** Lichter bereits auf dem Taxiway aus. Anderer Verkehr kann das
> als stehendes Flugzeug interpretieren, und niemand erkennt, dass gleich
> eingebogen wird.

### Engine Shutdown

1. Prüfen: Flugzeug steht, APU läuft **und** APU Bleed ist gesetzt.
2. Engine Cool-down Time gemäss FCOM beachten.
3. Erstes Triebwerk abstellen, prüfen, dass N2 und EGT sinken.
4. Erst dann das zweite Triebwerk abstellen und ebenso prüfen.

> [!NOTE]
> Es gibt keinen Grund, beide Triebwerke fast gleichzeitig abzustellen.

### Task Sharing nach dem Shutdown

- Der PF macht keine PM-Items, auch wenn er gerade Zeit hat und die Schalter näher
  liegen.

> [!WARNING]
> **Common Error:** Der PF übernimmt regelmässig PM-Items. Das wirkt hilfreich,
> führt aber dazu, dass der PM seine eigenen Items verlernt. Es ist keine Hilfe.

---

## Beacon und Parking Checklist

Das Beacon wird erst ausgeschaltet, wenn alle Türen disarmed sind, und die
Parking Checklist erst, wenn der Parking Flow des PM abgeschlossen ist.

### Beacon

- Je nach Airline: Seat Belts OFF bzw. Callout, sobald alle Türen disarmed sind.
- Erst **danach** Beacon OFF.
- Hintergrund: Mit Beacon OFF nähert sich das Ground Equipment. Passiert beim
  Disarmen ein Fehler, löst die Rutsche sonst in das Equipment aus.

### Parking Checklist

- Kriterium: Parking Flow completed.
- Der PM überwacht Beacon und Disarming und macht erst **danach** seinen Flow.

> [!WARNING]
> **Common Error:** Die Checklist wird beim Ausschalten des Beacons angefordert. Zu
> diesem Zeitpunkt ist der Parking Flow des PM in der Regel noch nicht
> abgeschlossen.

---

*Dieser Artikel gibt persönliche Erfahrungen wieder und ersetzt keine offiziellen
Unterlagen. Verbindlich sind FCOM, FCTM, QRH und das OM des jeweiligen
Luftfahrtunternehmens. Es gilt der [Haftungsausschluss](../README.md#️-haftungsausschluss).*
