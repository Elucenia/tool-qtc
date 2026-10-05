<!-- ELUCENIA technical documentation · qtc · zh · no clinical/professional/rights approval -->

# 校正 QT 间期（QTc）

[条件、来源与许可](https://elucenia.org/zh/tools/qtc)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 实测 QT 间期

`qt`

ms · 范围: 200–800

### 心率

`fc`

次心搏/分钟 · 范围: 30–250

### 性别

`sexo`

- `F` — 女性
- `M` — 男性

## 方法版本

QTc/Bazett 1920、Fridericia 1920、Framingham 1992、Hodges 1983；QT ms/RR秒；AHA 2009及Vandenberk 2016

## 已记录的公式

RR (s) = 60 ÷ 心率.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1.75 × (心率 − 60)

## 限制与适用人群

Vandenberk 2016在单中心回顾性分析中比较了窦性心律、窄QRS且心率低于90 bpm成人的QT校正。这些结果不能证明在心房颤动、传导障碍或表单接受的全部心率下具有同等表现。Bazett可能在高心率时高估QTc、低心率时低估QTc。校正的选择及解释需要心电图情境；单个值不能决定治疗。

## 参考文献

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
