# Azure Machine Learningで<br>レコメンド
#### 第11回 Cogbot勉強会！(2018/01/23)
#### nikkie

---

自己紹介

+++

---

### このLTでは

- Azure Machine Learning Studioについて話します |
- 主な対象: Azure Machine Learningを触ったことがある方 |

+++

### Azure Machine Learningの流れ

![AML_Basic-1](/image/AML_Basic-1.png)

[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次

+++

### Azure Machine Learningの流れ

![AML_Basic-2](/image/AML_Basic-2.png)

[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次

+++

### Azure Machine Learningの流れ

![AML_Basic-3](/image/AML_Basic-3.png)

[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次

+++

### Azure Machine Learningの流れ

![AML_Basic-4](/image/AML_Basic-4.png)

[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次

+++

### Azure Machine Learningの流れ

![AML_Basic-5](/image/AML_Basic-5.png)

[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次

+++

### Azure Machine Learningの流れ

![AML_Basic-6](/image/AML_Basic-6.png)

[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次

+++

### Azure Machine Learning Studioでは

![AML_Studio](/image/AML_Studio.png)

https://raw.githubusercontent.com/ayako/TS17-AzureMLHoL/master/media/4-07.PNG をもとに作成

---

### レコメンダーを作る

- レコメンダーでできること
- レコメンダー用モジュール
- レコメンダーに与えるデータ
- レコメンダーの例

+++

### レコメンダーでできること

- あるユーザのあるアイテムへの評価値を予測する |
- あるユーザに対してアイテムをレコメンドする |
- あるユーザに関係のあるユーザを見つける |
- あるアイテムに関係のあるアイテムを見つける |

+++

### レコメンダー用モジュール

- データの前処理: Split Data
  - PropertiesのSplitting modeに**Recommender Split**を指定する |
- 学習: Train Matchbox Recommender |
- 予測: Score Matchbox Recommender |
- 評価: Evaluate Matchbox Recommender |

+++

### レコメンダーに与えるデータ

- 評価データ(学習に必須)
  - ユーザID - アイテムID - 評価値 の形式 |
  - 例：ユーザU001がアイテムA01を星2と評価した |
- ユーザの属性データ
  - U001の性別、年齢など |
- アイテムの属性データ
  - アイテムがレストランの場合、A01の位置情報や料理の種類など |

+++

### レコメンダーの例

- レストランのレコメンド |
  - [Microsoft Azure Machine Learning レコメンドを試してみた(データ編)](https://azure-recipe.kc-cloud.jp/2016/03/ml_recommend_data/) |
  - [Microsoft Azure Machine Learning レコメンドを試してみた(モデル作成編)](https://azure-recipe.kc-cloud.jp/2016/04/ml_recommend_model/) |
- 映画のレコメンド |
  - [Azure Machine Learning による推薦システムを構築する手順書](https://www.slideshare.net/masayuki1986/azure-machine-learning-49034325) |

---

購買データからレコメンダーを作る

+++

---

まとめ

+++

ご清聴ありがとうございました
