# Rule-based

## 1.清楚記載這個專案的目的和結果，最後的推薦分數是多少，是否有成功
- 目的：建立推薦系統，以提升轉換率。達到 20% 的推薦分數。
- 結果：沒有成功，本次最高的推薦分數為 13%。
## 2.簡明清楚的使用說明：用了哪些工具和方法？為什麼？ 
本次製作兩個推薦模式來達成專案目標：
- 推薦模式一：直接推薦三個月內期間 review最多的前十產品(13%)
- 推薦模式二：利用長尾理論找到前20%的商品來推薦(18%)

工具使用：
- pandas
- numpy
- matplotlib

# Content-based
## 1.清楚記載這個專案的目的和結果，最後的推薦分數是多少，是否有成功
- 目的：利用content-based filtering，建立推薦系統
- 結果：沒有成功，本次推薦比直接使用rule-based還低。
## 2.簡明清楚的使用說明：用了哪些工具和方法？為什麼？ 

本次透過綜合內容推薦及模式來達成專案目標：
- 推薦模式：利用訓練資料三個月內 review最多的前十產品及內容推薦綜合推薦

工具使用：
pandas
numpy
matplotlib
TfidfVectorizer
cosine_similarity

# Collaborative filtering
## 1.清楚記載這個專案的目的和結果，最後的推薦分數是多少，是否有成功
- 專案目的：利用課堂上所學的協同過濾 (collaborative filter) 的方法來產生推薦,包含user-based、item-based以及套件surprise 建立商品推薦
- 結果：沒有成功，僅單純使用協同過濾來推薦比直接使用rule-based還低。
1. 手刻User-based collaborative filtering ：3位user被推薦，推薦分數為0
2. Item-based collaborative filtering： 32位user被推薦，推薦分數為0.0169 
3. 套件 surprise 實作 collaborative filtering：考量爆Ram狀況，故採用近一年的訓練資料來建立，13位user被推薦，推薦分數為0.0169 
## 2.簡明清楚的使用說明：用了哪些工具和方法？
- 結果與討論：透過CF實作推薦算法，模型仍表現不佳，可能原因如下：
1. 資料極大比例為新用戶， 故要從舊用戶中找到相似的用戶極為困難。
2. 藉由cosine similarity 找到相似用戶/物品近似度皆為1，導致無法有效推薦正確商品。

工具使用： pandas、numpy、matplotlib、TfidfVectorizer、cosine_similarity、suurprise
