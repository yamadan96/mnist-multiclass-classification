🧠 MNIST Multiclass Classification using Softmax & PyTorch

このリポジトリでは、sklearn.datasets.load_digits() を用いた8x8画像の手書き数字データ（MNIST）を対象に、Softmax回帰による多クラス分類をPyTorchで実装しています。

⸻

📌 内容

セクション	説明
データロード	sklearn.datasets.load_digits() を用いて画像・ラベルを取得
前処理	One-hotエンコーディング、正規化
モデル	手書きのSoftmax回帰モデル（W・bをパラメータとして定義）
学習	1サンプルずつforループで学習（勾配計算・更新あり）
評価	Accuracyを計算し、損失曲線をプロット



⸻

🛠️ 使用技術
	•	Python 3.x
	•	PyTorch
	•	scikit-learn
	•	matplotlib

⸻

🔍 実行結果（概要）
	•	学習精度（Accuracy）: 約97.7%（訓練セット）
	•	損失関数: Cross Entropy Loss
	•	最適化: 明示的なforループ＋勾配降下法
	•	Softmaxの実装: torch.exp() と torch.max() による数値安定化あり

⸻

📈 可視化
	•	画像の表示（matplotlib.pyplot.imshow()）
	•	学習中の損失変化グラフ（エポックごとにログ）

⸻

💡 学習の工夫ポイント
	•	損失の数値安定化 (+1e-10) を導入
	•	softmax のオーバーフロー対策として max を引く
	•	1データずつの更新によりパラメータの変化を直感的に把握可能

⸻

🚀 実行方法

Google Colab または Jupyter Notebook 上で .ipynb を開いて、セルを順番に実行してください。
