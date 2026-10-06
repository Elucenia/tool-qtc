<!-- ELUCENIA technical documentation · qtc · de · no clinical/professional/rights approval -->

# Korrigiertes QT (QTc)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/qtc)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Gemessenes QT-Intervall

`qt`

ms · Bereich: 200–800

### Herzfrequenz

`fc`

bpm · Bereich: 30–250

### Geschlecht

`sexo`

- `F` — Weiblich
- `M` — Männlich

## Fassung der Methode

QTc/Bazett 1920, Fridericia 1920, Framingham 1992, Hodges 1983; QT ms/RR Sekunden; AHA 2009 und Vandenberk 2016

## Dokumentierte Formel

RR (s) = 60 ÷ HF.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1,75 × (HF − 60)

## Grenzen und Population

Vandenberk 2016 verglich QT-Korrekturen bei Erwachsenen mit Sinusrhythmus, schmalem QRS und Herzfrequenz unter 90 bpm in einer retrospektiven Einzelzentrumsanalyse. Diese Ergebnisse belegen keine gleichwertige Leistung bei Vorhofflimmern, Leitungsstörungen oder allen vom Formular akzeptierten Frequenzen. Bazett kann QTc bei hohen Frequenzen überschätzen und bei niedrigen unterschätzen. Korrekturauswahl und Interpretation benötigen elektrokardiografischen Kontext; ein isolierter Wert bestimmt keine Behandlung.

## Referenzen

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

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

Normales QTc

| Ergebnisdetails | |
| --- | --- |
| Bazett | 400 ms |
| Fridericia | 400 ms |
| Framingham | 400 ms |
| Hodges | 400 ms |
| RR-Intervall | 1000 ms |


### 2

Normales QTc

| Ergebnisdetails | |
| --- | --- |
| Bazett | 465 ms |
| Fridericia | 427 ms |
| Framingham | 422 ms |
| Hodges | 430 ms |
| RR-Intervall | 600 ms |


### 3

Stark verlängertes QTc (> 500 ms): hohes Arrhythmierisiko

| Ergebnisdetails | |
| --- | --- |
| Bazett | 520 ms |
| Fridericia | 520 ms |
| Framingham | 520 ms |
| Hodges | 520 ms |
| RR-Intervall | 1000 ms |

