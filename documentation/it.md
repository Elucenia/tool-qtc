<!-- ELUCENIA technical documentation · qtc · it · no clinical/professional/rights approval -->

# QT corretto (QTc)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/qtc)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Intervallo QT misurato

`qt`

ms · intervallo: 200–800

### Frequenza cardiaca

`fc`

bpm · intervallo: 30–250

### Sesso

`sexo`

- `F` — Femminile
- `M` — Maschile

## Edizione del metodo

QTc/Bazett 1920, Fridericia 1920, Framingham 1992, Hodges 1983; QT ms/RR secondi; AHA 2009 e Vandenberk 2016

## Formula documentata

RR (s) = 60 ÷ FC.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1,75 × (FC − 60)

## Limiti e popolazione

Lo studio Vandenberk 2016 ha confrontato le correzioni del QT in adulti con ritmo sinusale, QRS stretto e frequenza cardiaca inferiore a 90 bpm, in un’analisi retrospettiva monocentrica. Questi risultati non dimostrano prestazioni equivalenti nella fibrillazione atriale, nei disturbi della conduzione o a tutte le frequenze accettate dal modulo. Bazett può sovrastimare il QTc alle frequenze alte e sottostimarlo alle frequenze basse. La scelta della correzione e l’interpretazione richiedono un contesto elettrocardiografico; un valore da solo non determina il trattamento.

## Riferimenti

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
