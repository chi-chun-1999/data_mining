# Estimating

## Training and Test Dataset

通常在模型訓練中，會將資料集分爲Training Dataset與 Test Dataset ，將 Training Dataset拿去訓練出一個模型，接著在利用Test Dataset 進行驗證，通常資料集的切分方式有8:2, 7:3 or 6:4

## k-fold validation

這種方式是將資料集分成k等分，接著將其中1等分當作測試資料集，其餘k-1當作訓練資料集，接著進行模型訓練與測試，結束後再換另一組，重複k次，最後尋找出結果最好的哪一個。

## N-fold validation

這是k-fold validation 的一種特例，是將N筆資料的其中一個當作測試資料集，其餘N-1當作訓練資料集，進行模型訓練與驗證，重複N次，找出最佳。但是這種方式有個非常明顯的bug就算會耗費大量的訓練時間。
