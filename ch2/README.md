# Data of Data Mining

## 2.2

- Nominal Variables: 除了一般的名稱之外，也可以是數值，但是在這種情況下（1+2不等於3）
- Binary Variables:
- Ordinal Variables: 離散性資料，應該是要有意義的順序，如小、中、大
- Integer Variables:
- Interval-scaled Variables:
- Ratio-scaled Variables:



##  區分Categorical 與 Continus

- Categorical：爲nominal、Bingary or Ordinal 的資料集
- Continus：簡單來說就是numerical的資料集，像是Integer、Interval-scaled或Ratio-scaled的資料集


## 資料的清理

1. 遇到一個屬性爲numerical的資料集，結果只有少數對應的數值分佈於每筆資料中，則可考慮將這個屬性視爲nominal
2. 如果有一個屬性資料的值都是同一個，則將這個屬性刪除


## 資料的遺失

在事務應用問題上，很多時候拿到的Dataset往往都會缺資料集，因此對於這類問題，有兩種比較常見的方案，分別爲：
1. 刪除資料
2. 如果是Categorical的資料，用比較頻繁的值替代，如果是Continus則用平均值取代


針對以上的方式，如果是遇到 __屬性資料遺失__ ，而不是類別資料遺失，不是很建議使用刪除資料的方式，而是利用頻繁值或是平均值取代。但如果是 __遇到類別資料遺失__ 就比較推薦使用刪除資料的方式
