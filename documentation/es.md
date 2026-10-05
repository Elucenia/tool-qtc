<!-- ELUCENIA technical documentation · qtc · es · no clinical/professional/rights approval -->

# QT corregido (QTc)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/qtc)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Intervalo QT medido

`qt`

ms · intervalo: 200–800

### Frecuencia cardíaca

`fc`

bpm · intervalo: 30–250

### Sexo

`sexo`

- `F` — Femenino
- `M` — Masculino

## Edición del método

QTc/Bazett 1920, Fridericia 1920, Framingham 1992, Hodges 1983; QT ms/RR segundos; AHA 2009 y Vandenberk 2016

## Fórmula documentada

RR (s) = 60 ÷ FC.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1,75 × (FC − 60)

## Límites y población

El estudio Vandenberk 2016 comparó correcciones del QT en adultos con ritmo sinusal, QRS estrecho y frecuencia cardíaca menor de 90 bpm, en un análisis retrospectivo de un solo centro. Estos resultados no demuestran un rendimiento equivalente en fibrilación auricular, trastornos de conducción ni todas las frecuencias aceptadas por el formulario. Bazett puede sobreestimar el QTc a frecuencias altas y subestimarlo a frecuencias bajas. La elección de la corrección y la interpretación requieren contexto electrocardiográfico; un valor aislado no determina el tratamiento.

## Referencias

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
