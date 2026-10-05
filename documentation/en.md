<!-- ELUCENIA technical documentation · qtc · en · no clinical/professional/rights approval -->

# Corrected QT (QTc)

[conditions, sources and permissions](https://elucenia.org/en/tools/qtc)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Measured QT interval

`qt`

ms · range: 200–800

### Heart rate

`fc`

bpm · range: 30–250

### Sex

`sexo`

- `F` — Female
- `M` — Male

## Method edition

QTc/Bazett 1920, Fridericia 1920, Framingham 1992, Hodges 1983; QT ms/RR seconds; AHA 2009 and Vandenberk 2016 references

## Documented formula

RR (s) = 60 ÷ HR.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1.75 × (HR − 60)

## Limits and population

The Vandenberk 2016 study compared QT corrections in adults with sinus rhythm, narrow QRS and heart rate below 90 bpm, in a retrospective single-center analysis. These results do not establish equivalent performance in atrial fibrillation, conduction disorders or all heart rates accepted by the form. Bazett can overestimate QTc at high heart rates and underestimate it at low heart rates. Selection of the correction and interpretation require electrocardiographic context; a value alone does not determine treatment.

## References

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
