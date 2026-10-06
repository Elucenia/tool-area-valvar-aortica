<!-- ELUCENIA technical documentation · area-valvar-aortica · de · no clinical/professional/rights approval -->

# Aortenklappenöffnungsfläche (Kontinuitätsgleichung)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/area-valvar-aortica)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Durchmesser des linksventrikulären Ausflusstrakts

`dvsve`

cm · Bereich: 1,2–3,5

### Geschwindigkeits-Zeit-Integral (VTI) des linksventrikulären Ausflusstrakts

`vtivsve`

cm · Bereich: 5–50

### Geschwindigkeits-Zeit-Integral der Aortenklappe (VTI)

`vtiao`

cm · Bereich: 10–250

### Maximale Aortengeschwindigkeit (optional)

`vmax`

m/s · optional · Bereich: 0,5–8

### Körperoberfläche (optional)

`sc`

m² · optional · Bereich: 0,8–3

## Fassung der Methode

EACVI/ASE 2017: Kontinuität mittels VTI; DVI; vereinfachte Bernoulli-Gleichung 4 v²

## Dokumentierte Formel

LVOT-Fläche = π × (Durchmesser ÷ 2)²

Aortenklappenfläche = LVOT-Fläche × LVOT-VTI ÷ Aorten-VTI

Dimensionsloser Index (DVI) = LVOT-VTI ÷ Aorten-VTI

Maximaler Gradient (vereinfachte Bernoulli-Gleichung) = 4 × V²

## Grenzen und Population

Die Beurteilung der Aortenstenose nach EACVI/ASE 2017 erfolgt integriert: Gradient, Fluss, Ejektionsfraktion und Qualität der Beurteilung des ventrikulären Ausflusstrakts müssen gemeinsam berücksichtigt werden. Niedrigfluss- oder Niedriggradientensituationen erfordern die im Dokument vorgesehene spezifische Bewertung. Isolierte Rechenwerte bilden diesen vollständigen Algorithmus nicht ab.

## Referenzen

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

Hochgradige Aortenstenose nach Fläche

| Ergebnisdetails | |
| --- | --- |
| LVOT-Fläche | 3,14 cm² |
| Dimensionsloser Index (DVI) | 0,25 |
| Maximaler Gradient (4V²) | 64 mmHg |


### 2

Mäßige Aortenstenose nach Fläche

| Ergebnisdetails | |
| --- | --- |
| LVOT-Fläche | 3,80 cm² |
| Dimensionsloser Index (DVI) | 0,37 |

