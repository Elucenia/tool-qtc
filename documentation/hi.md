<!-- ELUCENIA technical documentation · qtc · hi · no clinical/professional/rights approval -->

# संशोधित QT अंतराल (QTc)

[शर्तें, स्रोत और अनुमतियाँ](https://elucenia.org/hi/tools/qtc)

## उपयोग कैसे करें

पोर्टल पर उपकरण का उपयोग करें या स्थानीय HTTP सर्वर के माध्यम से index.html खोलें। भाषा चुनें, फ़ील्ड भरें और गणना करें।

## इनपुट और इकाइयाँ

### मापा गया QT अंतराल

`qt`

ms · सीमा: 200–800

### हृदय गति

`fc`

धड़कन/मिनट · सीमा: 30–250

### लिंग

`sexo`

- `F` — महिला
- `M` — पुरुष

## विधि का संस्करण

QTc/Bazett 1920, Fridericia 1920, Framingham 1992, Hodges 1983; QT ms/RR सेकंड; AHA 2009 व Vandenberk 2016

## दस्तावेज़ित सूत्र

RR (s) = 60 ÷ हृदय दर.

Bazett: QTc = QT ÷ √RR

Fridericia: QTc = QT ÷ ∛RR

Framingham: QTc = QT + 154 × (1 − RR)

Hodges: QTc = QT + 1.75 × (हृदय दर − 60)

## सीमाएँ और जनसमूह

Vandenberk 2016 अध्ययन ने एक केंद्र के पूर्वव्यापी विश्लेषण में साइनस रिद्म, संकीर्ण QRS और 90 bpm से कम हृदय दर वाले वयस्कों में QT सुधारों की तुलना की। ये परिणाम एट्रियल फ़िब्रिलेशन, चालन विकारों या फ़ॉर्म में स्वीकार की गई सभी हृदय दरों पर समान प्रदर्शन सिद्ध नहीं करते। Bazett ऊँची दरों पर QTc को अधिक और कम दरों पर कम आँक सकता है। सुधार का चयन और व्याख्या इलेक्ट्रोकार्डियोग्राफ़िक संदर्भ की माँग करते हैं; अकेला मान उपचार निर्धारित नहीं करता।

## संदर्भ

- [Rautaharju PM et al. AHA/ACCF/HRS Recommendations for the Standardization and Interpretation of the Electrocardiogram, Part IV: The ST Segment, T and U Waves, and the QT Interval. Circulation, 2009.](https://doi.org/10.1161/CIRCULATIONAHA.108.191096)

- [Vandenberk B et al. Which QT correction formulae to use for QT monitoring? J Am Heart Assoc, 2016.](https://doi.org/10.1161/JAHA.116.003264)

- [https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4937268/)

## तकनीकी परीक्षण दोहराएँ

दर्ज कृत्रिम मामलों को दोहराने के लिए इस रिपॉज़िटरी की मूल निर्देशिका में node test.cjs चलाएँ। मूल इनपुट, अपेक्षित परिणाम और सहनशीलता सीमाएँ सुरक्षित रखी गई हैं। तकनीकी परीक्षण नैदानिक सत्यापन नहीं हैं।

```sh
node test.cjs
```

tool.json में स्रोत, संस्करण और समीक्षा का दायरा दिया गया है। examples.json में कृत्रिम इनपुट और अपेक्षित परिणाम सुरक्षित हैं; results.json में प्राप्त परिणाम दर्ज हैं।

[रिकॉर्ड और संदर्भ](../tool.json) · [JavaScript कोड](../calculator.js) · [संदर्भ मामले](../examples.json) · [results.json](../results.json)

## समीक्षा और उपयोग की शर्तें

स्वतंत्र नैदानिक समीक्षा नहीं की गई है।

यह इंटरफ़ेस लेखकों द्वारा किया गया अनुवाद है, कोई आधिकारिक या प्रमाणित संस्करण नहीं। स्वतंत्र नैदानिक समीक्षा, पेशेवर भाषाई समीक्षा और उपकरणों के अधिकारों की अनुमति की प्रक्रिया पूरी नहीं हुई है।

सूत्र या वर्गीकरण का परिणाम। व्याख्या, कार्यवाही और उपयुक्तता पेशेवर मूल्यांकन और चुने गए स्रोत पर निर्भर है।

## लाइसेंस और श्रेय

Apache-2.0 केवल ELUCENIA के कोड पर लागू होता है। उपकरणों, प्रकाशनों, अनुवादों और डेटा के अधिकार उनके संबंधित अधिकारधारकों के पास रहते हैं। LICENSE और NOTICE सुरक्षित रखें।

ELUCENIA · Felipe Guedes · Copyright © 2026

## दर्ज किए गए परिणाम

नीचे दी गई जानकारी कृत्रिम उदाहरणों के लिए पद्धति के आउटपुट को सुरक्षित रखती है। यह स्वतंत्र नैदानिक सत्यापन नहीं है।

### 1

QTc सामान्य

| परिणाम का विवरण | |
| --- | --- |
| Bazett | 400 ms |
| Fridericia | 400 ms |
| Framingham | 400 ms |
| Hodges | 400 ms |
| RR अंतराल | 1000 ms |


### 2

QTc सामान्य

| परिणाम का विवरण | |
| --- | --- |
| Bazett | 465 ms |
| Fridericia | 427 ms |
| Framingham | 422 ms |
| Hodges | 430 ms |
| RR अंतराल | 600 ms |


### 3

QTc बहुत अधिक लंबा (> 500 ms): अतालता का उच्च जोखिम

| परिणाम का विवरण | |
| --- | --- |
| Bazett | 520 ms |
| Fridericia | 520 ms |
| Framingham | 520 ms |
| Hodges | 520 ms |
| RR अंतराल | 1000 ms |

