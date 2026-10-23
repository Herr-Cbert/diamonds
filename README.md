# Dajmonds

Ein kleines Geschicklichkeitsspiel in purem JavaScript auf einem HTML5-Canvas,
inspiriert von den Steine-und-Diamanten-Spielen der 80er. Zwei Dateien, keine
Abhängigkeiten, kein Build.

**Spielen:** [online im Browser](https://herr-cbert.github.io/diamonds/diamonds.html)
oder beide Dateien herunterladen und `diamonds.html` lokal öffnen.

## Spielprinzip

Alle Diamanten einsammeln, dann den Ausgang erreichen. Steine und Diamanten
fallen der Schwerkraft folgend nach unten und rollen von Kanten ab. Ein
**fallender** Stein erschlägt die Spielfigur, ein ruhender Stein direkt über
dem Kopf ist ungefährlich – man kann also unter Steinen hindurchgraben, muss
aber rechtzeitig zur Seite. Steine lassen sich waagerecht schieben, wenn
dahinter Platz ist.

| Taste | Funktion |
|---|---|
| Pfeiltasten | bewegen / graben |
| F1 | Level neu starten |
| F2 | nächstes Level (nach dem Sieg) |
| Bild auf / Bild ab | Level wählen |
| Esc | Pause |

## Eigene Level

Die Level stehen in `levels.js` als Zeichenkette. Jedes Level beginnt mit
`DIMX<Breite>DIMY<Höhe>` (jeweils drei Ziffern), danach folgen die Zeilen:

| Zeichen | Bedeutung |
|---|---|
| `#` | Mauer |
| `-` | Erde (kann weggegraben werden) |
| ` ` | Luft |
| `S` | Stein |
| `X` | Diamant |
| `I` | Eingang (Startposition) |
| `O` | Ausgang |

Die Liste endet mit `END`. Das Spielfeld ist auf 21 × 12 Felder begrenzt.

## Dateien

- `diamonds.html` – Spiel (Logik und Darstellung)
- `levels.js` – Leveldaten
