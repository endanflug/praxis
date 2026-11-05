# Enteisung und Winter Ops

[← Zurück zur Artikelübersicht](README.md)

*Stand: 10/2026 · Rubrik: Nice to know*

---

## Fluid-Typen

In der Anwendung haben alle Typen ungefähr gleich viel Glykol, um die Hälfte. Den
Unterschied macht der Verdicker, also wie lange der Film liegen bleibt und bei
welcher Geschwindigkeit er abfliesst. Werte sind Richtwerte, das
Produktdatenblatt gilt.

| Typ | Glykol | Verdicker | Abfliessen / Einsatz | Holdover |
|-----|--------|-----------|----------------------|----------|
| I | Konzentrat 80–90 %, verdünnt nach OAT (typisch 25–45 %) | keiner | läuft sofort ab, Enteisen und Reinigen | Minuten |
| II | um 50 % | ja | Rotation über ca. 100 kt | mittel |
| III | ähnlich (nicht sicher belegt) | ja, dünnflüssiger | Rotation ab ca. 60 kt, Turboprops | zwischen I und II |
| IV | um 50 % unverdünnt, Rest Wasser und Zusätze | ja, optimiert | Rotation über ca. 100 kt | am längsten |

- Type I wird nach der Regel «Gefrierpunkt mindestens 10 °C unter OAT» gemischt,
  nicht in festen Stufen. Unverdünnt ist es nicht vorgesehen.
- «100/0» bei Type IV heisst Produkt wie geliefert, nicht reines Glykol.

---

## Mischung und Holdover

Bei Type IV 50/50 bleiben etwa 25 % Glykol, gut 70 % Wasser und die Hälfte der
Zusätze. Die Holdover Time fällt dadurch stärker als nur auf die Hälfte, und
50/50 ist nur bis etwa −3 °C OAT zugelassen.

Zwei Effekte multiplizieren sich:

1. **Gefrierpunkt:** Der Zusammenhang zwischen Glykolanteil und Gefrierpunkt ist
   nicht linear. Bei 25 % liegt der Gefrierpunkt nur wenige Grad unter null, der
   Puffer schrumpft überproportional.
2. **Verdicker:** Mit verdünnten Polymeren wird der Film dünner und flüssiger und
   nimmt weniger Niederschlag auf.

Bei Type I spielt das Mischverhältnis für die Holdover Time keine Rolle, weil der
Gefrierpunkt-Puffer immer gleich gehalten wird. Die Tabellen unterscheiden dort
nach OAT, Niederschlag und Oberfläche (Aluminium oder Komposit).

---

## Gefrierpunkt-Physik

Wasser gefriert bei 0 °C, reines Ethylenglykol bei etwa −13 °C, die Mischung um
60 % Glykol erst um −50 °C. In der Mischung stören sich die Moleküle gegenseitig
beim Aufbau ihres Kristallgitters.

- **Mehr Glykol ist nicht besser:** Ab einer gewissen Konzentration steigt der
  Gefrierpunkt wieder, und das Fluid wird zäher.
- **Propylenglykol** kristallisiert kaum, es wird bei Kälte glasartig zäh. Darum
  hat es oft keinen echten Gefrierpunkt.
- Dasselbe Prinzip nutzen Streusalz und Auto-Kühlmittel.

---

## Rückstände und Two-Step

Verdicktes Fluid läuft beim Start nicht restlos ab. Ein dünner Restfilm bleibt,
deshalb muss jedes Fluid einen aerodynamischen Abnahmetest bestehen.

> [!CAUTION]
> **Das eigentliche Problem:** Rückstände in Ruderspalten und hinter Klappen
> trocknen ein, quellen bei Regen oder Feuchte wieder zu Gel auf und können in der
> Höhe gefrieren und Ruder blockieren.

- **Two-Step:** Schritt 1 heisses Type I entfernt Eis und reinigt, Schritt 2
  Type IV schützt unverdünnt auf sauberer Fläche. Das Abwaschen alter Reste ist
  ein Nebeneffekt.
- **One-Step mit II/IV** wiederholt fördert Rückstände. Die Spalten werden trotzdem
  nicht restlos sauber, die Technik kontrolliert und reinigt im Winter zusätzlich.

---

*Dieser Artikel dient der Information und ersetzt keine offiziellen Unterlagen.
Verbindlich sind die Holdover-Tabellen und Vorgaben des Luftfahrtunternehmens.
Es gilt der [Haftungsausschluss](../README.md#️-haftungsausschluss).*
