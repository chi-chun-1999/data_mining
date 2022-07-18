# Clash

使用決策樹時，有時候會遇到，dataset發生clash的問題，也就是說，有instances的所有attritube值都相同，唯獨class不同，以至於出現無法分類分類的問題。

目前處理這個問題的方式有三種
- Marjority Voting：將這些Instance中選擇分類結果最多的那一個
- Delete Branch：將這個分支刪除，一個不是那麼建議的方式，因爲這種方式與刪除instance類似
- clash threshold：再clash set中如果有屬於同一類別的子集大過於這個值，則使用Majority Voting的方式，如果都沒有則Delete Branch。通常會使用60% 70% 80% 90%。此外如果這個值是0%，則變成Marjority Voting；如果爲100%，則變成Delete Branch。



