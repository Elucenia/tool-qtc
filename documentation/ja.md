<!-- ELUCENIA technical documentation · qtc · ja · no clinical/professional/rights approval -->

# 補正QT間隔（QTc）

[条件・出典・許諾](https://elucenia.org/ja/tools/qtc)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 実測QT間隔

`qt`

ms · 範囲: 200–800

### 心拍数

`fc`

拍/分 · 範囲: 30–250

### 性別

`sexo`

- `F` — 女性
- `M` — 男性

## 方法の版

QTc/Bazett 1920、Fridericia 1920、Framingham 1992、Hodges 1983、QT ms/RR秒、AHA 2009とVandenberk 2016

## 記載された計算式

RR (s) = 60 ÷ 心拍数.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1.75 × (心拍数 − 60)

## 限界・対象集団

Vandenberk 2016の研究は単施設の後ろ向き解析で、洞調律、狭いQRS、心拍数90 bpm未満の成人でQT補正を比較しました。この結果は、心房細動、伝導障害、フォームが受け付ける全ての心拍数で同等の性能があることを証明しません。Bazettは高い心拍数ではQTcを過大評価し、低い心拍数では過小評価することがあります。補正法の選択と解釈には心電図の状況が必要であり、一つの値だけでは治療は決まりません。

## 参考文献

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 記録された結果

以下の情報は、合成例に対する手法の出力を保持したものです。独立した臨床的検証を示すものではありません。

### 1

QTc正常

| 結果の詳細 | |
| --- | --- |
| Bazett | 400 ms |
| Fridericia | 400 ms |
| Framingham | 400 ms |
| Hodges | 400 ms |
| RR間隔 | 1000 ms |


### 2

QTc正常

| 結果の詳細 | |
| --- | --- |
| Bazett | 465 ms |
| Fridericia | 427 ms |
| Framingham | 422 ms |
| Hodges | 430 ms |
| RR間隔 | 600 ms |


### 3

QTcが著明延長（> 500 ms）：不整脈リスクが高い

| 結果の詳細 | |
| --- | --- |
| Bazett | 520 ms |
| Fridericia | 520 ms |
| Framingham | 520 ms |
| Hodges | 520 ms |
| RR間隔 | 1000 ms |

