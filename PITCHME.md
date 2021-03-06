# Azure Machine Learningで<br>レコメンド
#### 第11回 Cogbot勉強会！(2018/01/23)
#### nikkie

---

### nikkie （にっきー）

- ソフトウェアエンジニア2年目
- 2018/01〜 業務でAzure Machine Learning利用中
- 趣味: アニメ、Python
- [Pythonでアニメ画像のモザイクアート作ってみた](https://speakerdeck.com/ftnext/pillow-mosaic-art-nyumon)

+++

### nikkie (@ftnext)

- [Twitter @ftnext](https://twitter.com/ftnext)
- [Azure Machine Learningの初歩の初歩](http://nikkie-ftnext.hatenablog.com/entry/2017/12/31/230251)
- [Azure Machine Learningの初歩](https://qiita.com/ftnext/items/5852d142050b960b2777)
- [Azure Machine Learningで「最適なアルゴリズムを選択する」には](https://qiita.com/ftnext/items/94d220a5e6c50b43e478)

+++

### 質問・指摘お待ちしています

- 以下、お品書きです。
- Azure Machine Learningの流れ
- レコメンダー
- 購買履歴から評価値を得る
- サンプルを元にした実装例
- まとめ

---

### Azure Machine Learningでレコメンド

- このLTではレコメンドシステムを<br><span class="red-char">レコメンダー</span>と呼びます
- Azure Machine Learning Studioでレコメンダーを作る方法を話します |
- Azure Machine Learningを触ったことがある方<br>向けです |

+++

### Azure Machine Learningの流れ
<span style="font-size:medium">[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次</span>
![AML_Basic-1](/image/AML_Basic-1.png)

+++

### Azure Machine Learningの流れ
<span style="font-size:medium">[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次</span>
![AML_Basic-2](/image/AML_Basic-2.png)

+++

### Azure Machine Learningの流れ
<span style="font-size:medium">[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次</span>
![AML_Basic-3](/image/AML_Basic-3.png)

+++

### Azure Machine Learningの流れ
<span style="font-size:medium">[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次</span>
![AML_Basic-4](/image/AML_Basic-4.png)

+++

### Azure Machine Learningの流れ
<span style="font-size:medium">[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次</span>
![AML_Basic-5](/image/AML_Basic-5.png)

+++

### Azure Machine Learningの流れ
<span style="font-size:medium">[TechSummit 2017 Japan : Hands on Learning 資料](https://github.com/ayako/TS17-AzureMLHoL/blob/master/TS17_AzureMLHoL_UWP.pdf) 目次</span>
![AML_Basic-6](/image/AML_Basic-6.png)

+++

### Azure Machine Learning Studioでは
<span style="font-size:small">https://raw.githubusercontent.com/ayako/TS17-AzureMLHoL/master/media/4-07.PNG をもとに作成</span>
![AML_Studio](/image/AML_Studio.png)

---

### レコメンダー

- レコメンダーでできること
- レコメンダー用モジュール
- レコメンダーの学習に使うデータ
- レコメンダーの例

+++

### レコメンダーでできること

- <span class="red-char">あるユーザに対してアイテムをレコメンドする</span>
- あるユーザのあるアイテムへの評価値を予測する
- あるユーザに関係のあるユーザを見つける
- あるアイテムに関係のあるアイテムを見つける

+++

### レコメンダー用モジュール

- データの前処理: Split Data
  - <span>PropertiesのSplitting modeに**Recommender Split**を指定する</span> |
- 学習: Train Matchbox Recommender |
- 予測: Score Matchbox Recommender |
- 評価: Evaluate Matchbox Recommender |

+++

### レコメンダーの学習に使うデータ

- 評価データ(学習に必須)
  - <span><span class="red-char">ユーザID - アイテムID - 評価値</span> の形式</span> |
  - 例：ユーザU001がアイテムA01を星2と評価した |
- ユーザの属性データ
  - U001の性別、年齢など |
- アイテムの属性データ
  - A01のカテゴリ情報など |

+++

### レコメンダーの例

- レストランのレコメンド |
  - [Microsoft Azure Machine Learning レコメンドを試してみた(データ編)](https://azure-recipe.kc-cloud.jp/2016/03/ml_recommend_data/) |
  - [Microsoft Azure Machine Learning レコメンドを試してみた(モデル作成編)](https://azure-recipe.kc-cloud.jp/2016/04/ml_recommend_model/) |
- 映画のレコメンド |
  - [Azure Machine Learning による推薦システムを構築する手順書](https://www.slideshare.net/masayuki1986/azure-machine-learning-49034325) |

---

### 購買履歴から評価値を得る

- 購買履歴:<br>「誰がどの商品を買った」というデータ
- <span>学習に必要なのは「誰がどの商品を<br><span class="red-char">星いくつと評価</span>した」というデータ</span> |

+++

### 購買履歴から評価値を得る

- 評価値を固定してみる:<br>「購入者は買った商品を星1と評価した」
- レストランのサンプルのデータを加工し、実験

![same_rating_data](image/same_rating_data.png)

+++

### 購買履歴から評価値を得る

- 結果: 無効なデータというエラー
- 評価値がすべて同じために出るらしい

![same_rating_error](image/same_rating_error.png)

+++

### 購買履歴から評価値を得る

Azure AI Galleryに<br>購買履歴を使った事例がないか検索

+++

### 購買履歴から評価値を得る

購買履歴を使った事例<br>
<span style="font-size:medium">https://gallery.cortanaintelligence.com/Experiment/ProductRecfromMDLBranch-3</span>

![gallery_sample](image/gallery_sample.png)

+++

### 購買履歴から評価値を得る

- <span><span class="red-char">購入回数を評価値とみなして</span>評価データを用意</span> |
  - あるユーザが同じ商品を3回買っていたら、<br>その商品への評価は3となる |
  - 同じ人に複数回買われる商品があるため、<br>評価値がすべて同じことによるエラーは出ない |
- ユーザの属性データ、アイテムの属性データは購買履歴から抽出できる |

---

### サンプルを元にした実装例

+++?image=image/recommend_sample-1.png&size=auto 90%

+++?image=image/recommend_sample-2.png&size=auto 90%

+++?image=image/recommend_sample-3.png&size=auto 90%

+++?image=image/recommend_sample-4.png&size=auto 90%

+++?image=image/recommend_sample-5.png&size=auto 90%

+++?image=image/recommend_sample-6.png&size=auto 90%

+++?image=image/recommend_sample-7.png&size=auto 90%

+++

### サンプルを元にした実装例<br>Scoreモジュールの出力

![scored_dataset](image/scored_dataset.png)

---

### まとめ

- <span>Azure Machine Learningでレコメンダーを<br>作るには、<span class="red-char">専用モジュール</span>を使う</span> |
- <span>レコメンダーの学習には <span class="red-char">ユーザID - アイテムID <br>- 評価値</span> の形式のデータが必須</span> |
- <span><span class="red-char">評価値として購入回数を用いる</span>ことで、<br>購買履歴からレコメンダーを作成できる</span> |

+++

### ご清聴ありがとうございました

質問・指摘がありましたら、<br>@ftnextまでお願いします

LTスライド: https://gitpitch.com/ftnext/CogBot11-LT-201801
