# Pilzboks – Corporate Design

Stand: 30.09.2026 (V2: Salbei-Hintergrund) · Quelle der Farben: `20260809_Logo-Varianten-PilzFarbe.pdf` (Adobe Illustrator, CMYK)
Die gleiche Beschreibung liegt im Pilzboks-Gehirn (`15_Corporate_Design.md`). Bei Widerspruch gilt das Gehirn.

## Farben

| Name | Einsatz | CMYK (Druck) | RGB | HEX (Bildschirm) |
|---|---|---|---|---|
| **Pilzboks-Grün** | Hauptfarbe: Schriftzug, Buttons, Links, Akzente | 92 / 37 / 100 / 36 | 10 / 91 / 44 | `#0A5B2C` |
| **Pilzboks-Braun** | Pilzkappe im Logo, sparsamer Zweitakzent | 39 / 73 / 91 / 57 | 97 / 53 / 26 | `#61351A` |
| **Kontur** | Stiel und Kappenrand im Logo | 0 / 0 / 0 / 100 | 35 / 31 / 32 | `#231F20` |
| **Weiß** | Karten, Buttons, Labels auf dem Salbei-Hintergrund | 0 / 0 / 0 / 0 | 255 / 255 / 255 | `#FFFFFF` |

Die CMYK-Werte sind das Original. Die HEX-Werte sind daraus umgerechnet (Coated FOGRA39 → sRGB,
relativ farbmetrisch mit Tiefenkompensierung – die Standardeinstellung von Adobe in Europa).
Für Druck immer CMYK verwenden, für Bildschirm, Web, Canva, Figma und PowerPoint den HEX-Wert.

### Abgeleitete Töne (nur digital)

| Name | HEX | Wofür |
|---|---|---|
| **Salbei-Hauch** | `#EEF3EA` | Seitenhintergrund der Website (zartes Grün statt reinem Weiß) |
| Salbei dunkler | `#E5ECE0` | Footer, abgesetzte Bereiche |
| Text | `#17231B` | Fließtext und Überschriften (fast Schwarz, leicht grün) |
| Grün dunkel | `#07431F` | Hover-Zustand von Buttons |
| Grün hell | `#3D8A5C` | nur Deko (Verläufe, Linien) – nicht für Text |
| Salbei Hover | `#DCE6D6` | Hover-Flächen |

Kontrast auf Salbei-Hauch (WCAG): Grün 7,3 : 1 · Braun 9,2 : 1 · Text 14,4 : 1 – alle für kleine Schrift geeignet (auf Weiß noch etwas höher).
Weiße Schrift auf Pilzboks-Grün ist ebenfalls gut lesbar (8,2 : 1).

## Logo

- Gültige Variante: **V10 · Pilz 1** aus dem Logo-PDF – gefüllte braune Kappe, dunkle Kontur, grüner Schriftzug.
- Dateien: `pilzboks-logo.svg` (Farbe, für helle Hintergründe) · `pilzboks-logo-weiss.svg` (weiß, für Grün oder dunkle Fotos).
  Beide sind Vektoren direkt aus dem Illustrator-PDF – beliebig skalierbar.
- Logo nie umfärben, verzerren, mit Filtern oder Schatten versehen. Auf Fotos nur dort, wo der Hintergrund ruhig ist.
- Mindestgröße: 24 px Höhe am Bildschirm, 10 mm Höhe im Druck (Empfehlung).
- Freiraum rund ums Logo: mindestens die Höhe des „P“.

## Schrift

- **Logo:** Segoe UI Black – steckt als Pfade in der Logodatei, wird nicht nachgesetzt.
- **Website:** Space Grotesk (liegt in `fonts/`), Überschriften 700, Fließtext 300–400.

## Website-Regeln

- Hintergrund Salbei-Hauch `#EEF3EA`, Karten/Labels/Buttons weiß, Text `#17231B`.
- Akzente in Pilzboks-Grün; Braun sparsam für kleine Details (Punkte, Trennstriche).
- Globus: Ozean in gedämpftem Seegrün-Blau, heller Rand – keine Neon-Effekte.
- Kein Neon-Grün mehr (früher `#4ADE80`), kein Dark Mode.
- Die Farbwerte stehen als CSS-Variablen im `:root` jeder Seite (`--brand-green`, `--brand-brown` …).
  Neue Farben immer dort ergänzen, nie direkt im CSS hartkodieren.

```css
:root{
  --brand-green:#0A5B2C;  /* CMYK 92/37/100/36 */
  --brand-brown:#61351A;  /* CMYK 39/73/91/57 */
  --brand-ink:#231F20;    /* CMYK 0/0/0/100 */
  --bg:#EEF3EA;   /* Salbei-Hauch */
  --card:#FFFFFF;
  --text:#17231B;
}
```
