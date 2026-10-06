<!-- ELUCENIA technical documentation · qtc · fr · no clinical/professional/rights approval -->

# QT corrigé (QTc)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/qtc)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Intervalle QT mesuré

`qt`

ms · intervalle: 200–800

### Fréquence cardiaque

`fc`

bpm · intervalle: 30–250

### Sexe

`sexo`

- `F` — Féminin
- `M` — Masculin

## Édition de la méthode

QTc/Bazett 1920, Fridericia 1920, Framingham 1992, Hodges 1983 ; QT ms/RR secondes ; AHA 2009 et Vandenberk 2016

## Formule documentée

RR (s) = 60 ÷ FC.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1,75 × (FC − 60)

## Limites et population

L’étude Vandenberk 2016 a comparé les corrections du QT chez des adultes en rythme sinusal, avec un QRS étroit et une fréquence cardiaque inférieure à 90 bpm, dans une analyse rétrospective monocentrique. Ces résultats ne démontrent pas une performance équivalente en fibrillation atriale, dans les troubles de conduction ou pour toutes les fréquences acceptées par le formulaire. Bazett peut surestimer le QTc aux fréquences élevées et le sous-estimer aux fréquences basses. Le choix de la correction et l’interprétation exigent le contexte électrocardiographique ; une valeur seule ne détermine pas le traitement.

## Références

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

QTc normal

| Détails du résultat | |
| --- | --- |
| Bazett | 400 ms |
| Fridericia | 400 ms |
| Framingham | 400 ms |
| Hodges | 400 ms |
| Intervalle RR | 1000 ms |


### 2

QTc normal

| Détails du résultat | |
| --- | --- |
| Bazett | 465 ms |
| Fridericia | 427 ms |
| Framingham | 422 ms |
| Hodges | 430 ms |
| Intervalle RR | 600 ms |


### 3

QTc très prolongé (> 500 ms) : risque élevé d’arythmie

| Détails du résultat | |
| --- | --- |
| Bazett | 520 ms |
| Fridericia | 520 ms |
| Framingham | 520 ms |
| Hodges | 520 ms |
| Intervalle RR | 1000 ms |

