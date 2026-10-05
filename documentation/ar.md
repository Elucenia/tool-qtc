<!-- ELUCENIA technical documentation · qtc · ar · no clinical/professional/rights approval -->

# فترة QT المصححة (QTc)

[الشروط والمصادر والأذونات](https://elucenia.org/ar/tools/qtc)

## كيفية الاستخدام

استخدم الأداة في البوابة أو افتح index.html عبر خادم HTTP محلي. اختر اللغة، وأكمل الحقول، ثم أجرِ الحساب.

## المدخلات والوحدات

### فترة QT المقاسة

`qt`

ms · النطاق: ٢٠٠–٨٠٠

### معدل ضربات القلب

`fc`

ضربة/دقيقة · النطاق: ٣٠–٢٥٠

### الجنس

`sexo`

- `F` — أنثى
- `M` — ذكر

## إصدار الطريقة

QTc/بازيت 1920، فريديريشيا 1920، فرامنغهام 1992، هودجز 1983؛ QT ms/RR بالثواني؛ AHA 2009 وVandenberk 2016

## المعادلة الموثقة

RR (s) = 60 ÷ معدّل القلب.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1.75 × (معدّل القلب − 60)

## الحدود والفئة السكانية

قارنت دراسة Vandenberk 2016 تصحيحات QT لدى بالغين بنظم جيبي وQRS ضيق ومعدل قلب أقل من 90 bpm، في تحليل استعادي بمركز واحد. لا تثبت هذه النتائج أداءً مكافئًا في الرجفان الأذيني أو اضطرابات التوصيل أو جميع معدلات القلب التي يقبلها النموذج. قد تبالغ Bazett في تقدير QTc عند المعدلات العالية وتقلّل تقديره عند المعدلات المنخفضة. يتطلب اختيار التصحيح والتفسير سياق تخطيط القلب؛ ولا تحدد قيمة منفردة العلاج.

## المراجع

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## إعادة إجراء الاختبارات التقنية

شغّل node test.cjs في المجلد الجذري لهذا المستودع لتكرار الحالات الاصطناعية المسجلة. تُحفظ المدخلات والنتائج المتوقعة وحدود التفاوت الأصلية. لا تُعدّ الاختبارات التقنية تحققًا سريريًا.

```sh
node test.cjs
```

يحتوي tool.json على المصادر والإصدار ونطاق المراجعة. يحتفظ examples.json بالمدخلات والنتائج المتوقعة للحالات الاصطناعية؛ ويسجل results.json النتائج التي تم الحصول عليها.

[السجل والمراجع](../tool.json) · [شيفرة JavaScript](../calculator.js) · [حالات مرجعية](../examples.json) · [results.json](../results.json)

## المراجعة وشروط الاستخدام

لم تُجرَ مراجعة سريرية مستقلة.

هذه الواجهة ترجمة أعدّها مؤلفوها، وليست إصدارًا رسميًا أو معتمدًا. لم تُجرَ مراجعة سريرية مستقلة أو مراجعة لغوية مهنية، ولم تُستكمل الموافقة على حقوق استخدام الأدوات.

نتيجة المعادلة أو التصنيف. يعتمد التفسير والتصرف ومدى الانطباق على التقييم المهني والمصدر المحدد.

## الترخيص ونسبة العمل إلى أصحابه

ينطبق Apache-2.0 على كود ELUCENIA فقط. تبقى حقوق الأدوات والمنشورات والترجمات والبيانات لأصحابها المعنيين. احتفظ بملفّي LICENSE وNOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
