# 使用Decision Tree演算法所面臨的問題

## Conflict Resolution
當Decison Tree進行剪枝後，常會面臨一個instance，可以滿足多項規則，導致無法順利分類。以下偍供幾種方法。

- majority voting：選擇被歸類最多的那個類別。
- 根據不同的規則，給矛不同的優先權（像是規則較少的weight較大，或是比罕見的類別weight較大）
- 根據每條規規的預測準確率進行排序，由高到低，當Test Data有結果則直接分類。


## Redundant Terms with Decision Tree

在使用Decision Tree時，常會產生多餘的規則

以下較簡單的規則：

Rule1: IF a = 1 and b = 1, THEN Class = 1
Rule2: IF c = 1 and d = 1, THEN Class = 1


如果換成Decision Tree

IF a = 1 and b = 1 then Class = 1;
IF a = 1 and b = 2  and c= 1 and d = 1, then class = 1;
IF a = 1 and b = 3  and c= 1 and d = 1, then class = 1;
IF a = 2 and c= 1 and d = 1, then class = 1;
IF a = 3 and c= 1 and d = 1, then class = 1;
IF a = 3 and c= 1 and d = 1, then class = 1;

會產生過多太詳細的規則，至於要解決這個問題可以使用Prism Alogrithm



## Prism Alogrithm

它的使用方法為

1. 計算每個類別的邊機率
2. 選擇機率最大的一個，並將這項從原資料取出並做成子集。
3. 重覆1、2步驟，直到所有的子集都為同一類，或是遇到所有的attritube都選擇過了，都還沒分出結果，則選擇子集中類別最多的那個。
4. 將第三步找到的集合從原資料集刪除。
