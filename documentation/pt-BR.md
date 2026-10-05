<!-- ELUCENIA technical documentation · qtc · pt-BR · no clinical/professional/rights approval -->

# QT corrigido (QTc)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/qtc)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Intervalo QT medido

`qt`

ms · intervalo: 200–800

### Frequência cardíaca

`fc`

bpm · intervalo: 30–250

### Sexo

`sexo`

- `F` — Feminino
- `M` — Masculino

## Edição do método

QTc/Bazett 1920, Fridericia 1920, Framingham 1992, Hodges 1983; QTms/RRseg; referências AHA 2009 e Vandenberk 2016

## Fórmula documentada

RR (s) = 60 ÷ FC.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1,75 × (FC − 60)

## Limites e população

O estudo Vandenberk 2016 comparou correções do QT em adultos com ritmo sinusal, QRS estreito e frequência cardíaca menor que 90 bpm, em análise retrospectiva de um centro. Esses resultados não comprovam desempenho equivalente em fibrilação atrial, distúrbios da condução ou todas as frequências aceitas pelo formulário. Bazett pode superestimar o QTc em frequências altas e subestimá-lo em frequências baixas. A escolha da correção e a interpretação exigem contexto eletrocardiográfico; um valor isolado não determina tratamento.

## Referências

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
