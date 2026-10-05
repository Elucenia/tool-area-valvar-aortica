<!-- ELUCENIA technical documentation · area-valvar-aortica · ja · no clinical/professional/rights approval -->

# 大動脈弁口面積（連続の式）

[条件・出典・許諾](https://elucenia.org/ja/tools/area-valvar-aortica)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 左室流出路径

`dvsve`

cm · 範囲: 1.2–3.5

### 左室流出路VTI

`vtivsve`

cm · 範囲: 5–50

### 大動脈弁VTI

`vtiao`

cm · 範囲: 10–250

### 大動脈最大血流速度（任意）

`vmax`

m/s · 任意 · 範囲: 0.5–8

### 体表面積（任意）

`sc`

m² · 任意 · 範囲: 0.8–3

## 方法の版

EACVI/ASE 2017：VTIによる連続の式；DVI；簡易Bernoulli 4 v²

## 記載された計算式

左室流出路面積 = π × (直径 ÷ 2)²

大動脈弁口面積 = 左室流出路面積 × 左室流出路VTI ÷ 大動脈VTI

無次元指数（DVI） = 左室流出路VTI ÷ 大動脈VTI

最大圧較差（簡易Bernoulli式） = 4 × V²

## 限界・対象集団

EACVI/ASE 2017の推奨における大動脈弁狭窄症の評価は総合的なものです。圧較差、血流、駆出率、心室流出路評価の質を併せて考慮する必要があります。低流量や低圧較差の場合は、文書に規定された個別の評価が必要です。計算値だけでは、その完全なアルゴリズムを再現できません。

## 参考文献

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
