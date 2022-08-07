# signate_stu22

### 検討事項

* cv
* stemming or lemmatisation
* Focal loss([Use Focal Loss To Train Model Using Imbalanced Dataset](https://leimao.github.io/blog/Focal-Loss-Explained/))
* preprocessing
* postprocessing
* ensamble
* stacking


### 参考
[2020:Kaggle のデータ分析コンペ Tweet Sentiment Extraction で『5位 / 2,227チーム』を獲得しました :)](https://lab.mo-t.com/blog/kaggle-tweet-sentiment-extraction-2020)
* Kaggle ではよく magic と表現をされますが、『何かに気付く』ことで飛躍的にスコアを伸ばせることがしばしばあります
* アンサンブル学習の代表的な手法には以下のようなものがあります。
  * averaging：各モデルの出力の重み付き（または単純）平均をとり、その値を予測値とする。
  * stacking：各モデルの出力を入力とするモデルを作成し、そのモデルの出力値を予測値とする。

[Toxic Comment Classification Challenge: 1st place solution overview](https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge/discussion/52557)
* Diverse pre-trained embeddings
* Translations as train/test-time augmentation (val-dataのleakに注意)
* Rough-bore pseudo-labelling (テストデータに擬似ラベルを付与して学習)
* Others:　事前学習された埋め込みがモデルの複雑さのほとんどを占めるため些細なアーキテクチャの変更はほとんど効果なし

[2021年のKaggle NLPコンペソリューションの共通戦略から学ぶ](https://qiita.com/cfiken/items/0890269721fb78bd9683)
>* 事前学習モデルの上にアーキテクチャ的な変更を加えてもスコアが改善されづらいことが経験的に知られている[要出典]。
>* 画像コンペとは違い入力が離散値なので、data augmentation での工夫が難しい。
>* 事前学習モデルを使うため、前処理でテキストのクレンジング・クリーニングなどの効果があまり期待できない。
>* データ数が少ない場合は学習が不安定になりがちで、本質的な改善を確認しづらい。


