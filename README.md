![title](data/info/images/readme/title.png)

# Kaggle Contradictory-My-Dear-Watson

## Overview of this Competition(DeepL)
<hr>

### Description
<br>
<b>...不可能を排除したとき、残ったものは何であれ、たとえありえないことであっても、真実でなければならない。</b><br>
<div style="text-align: right;">
ーSir Arthur Conan Doyleー
</div>

私たちの脳はこのような文章の意味を 瞬時に処理することが可能である.

推測することができます。

- 消去法によって正解を導き出す
- 真実かもしれないもの： "ありえないアイデアは不可能ではない！"
- そして、いくつかの主張は明らかに矛盾しています。"不可能だと断定していたものにこそ真実がある"


自然言語処理（NLP）は、ここ数年でますます精巧になってきています。機械学習モデルは、質問の回答、テキストの抽出、文章の生成、その他多くの複雑なタスクに取り組んでいます。しかし、文章間の関係性を機械が判断できるのか、それとも人間に任せるのか。もしNLPが文章間に適用できるならば、事実確認、フェイクニュースの特定、テキストの分析などに大きな意味を持つ可能性があります。

<b>今回の課題</b><br>

2つの文章があるとしたら、それらが関連している可能性は3つあります：一方はもう一方を含む可能性があり、もう一方はもう一方を矛盾させる可能性があり、またはそれらは無関係である可能性があります。自然言語推論 (Natural Language Inferencing: NLI) は人気のある NLP 問題で、文のペア (前提と仮説からなる) がどのように関連しているかを決定することを含みます。

あなたの課題は、前提文と仮説のペアに0、1、2のラベル（包含、中立、矛盾に対応）を割り当てるNLIモデルを作成することです。さらに面白くするために、訓練セットとテストセットには15の異なる言語のテキストが含まれています。データセットの詳細については、データのページを参照してください。

今日、NLI問題に対する最も一般的なアプローチには、BERTのような埋め込みや変換器の使用があります。このコンテストでは、テンソルプロセッシングユニット（TPU）のパワーを使ってこの問題に挑戦するためのスターターノートブックを提供しています。TPUは、自然言語処理を含む深層学習タスクに特化した強力なハードウェアアクセラレータです。Kaggle では、すべてのユーザーに TPU Quota を無償で提供しています。TPUのドキュメントやKaggleのYouTubeプレイリストをチェックして、詳細な情報やリソースを確認してください。

<a href="https://www.kaggle.com/anasofiauzsoy/tutorial-notebook">推奨チュートリアル<br>
Ana Sofia Uzsoyのチュートリアルでは、TPUとBERTを使って、あなたの最初の提出物をステップバイステップで作成する方法を紹介しています。
これはあなたのNLPの筋肉を鍛え、エキサイティングな問題を解決する絶好の機会です。</a>

Disclaimer: The dataset for this competition contains text that may be considered profane, vulgar, or offensive.
<hr>

### Evaluation

<b>Goal</b>

あなたの目標は、与えられた仮説がその仮説の前提に矛盾しているか、包含しているか、またはそれらのどちらも真ではないか（中立）を予測することです。
検定集合の各標本について、変数の0、1、または2の値を予測しなければなりません。

これらの値は次のように論理的条件に対応します。

0 == entailment(包含)
1 == Neutral
2 == contradiction(矛盾)

<b>Metric</b>
スコアは、正しく予測した関係性の割合によって算出される.

提出ファイルの形式
5195個のエントリーとヘッダー行を含むcsvファイルを提出する必要があります。提出物に余分な列(idと予測値以外の列)や行がある場合、エラーが表示されます。

ファイルには正確に2つの列が必要です。

1. id (任意の順序でソート)
2. prediction


Ex).
|id|prediction|
|---|---|
|c6d58c3f69|1|
|CEFCC82292|1|
|E98005252C|1|
|58518c10ba|1|
|c32b0d16df|1|

<hr>

### Data Description

|Name|Description|
|---|---|
|id|---|
|premise|前提になる文章|
|hypothesis|仮説|
|lang_adv|言語略称(ar/en/hi/)|
|language|言語|
|label|0,1,2|
<hr>

# Log
<hr>



