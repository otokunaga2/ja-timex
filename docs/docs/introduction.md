# イントロダクション
## 概要
人間が言葉として表現する日付や時刻、期間、頻度といった時間情報は、実に多様な表現を持ちます。テキストにおける時間情報を正確に認識することは、そのテキストが意味する事象やその関係性の理解に必要不可欠です。そうした時間情報を扱う言語処理タスクやアプリケーションにおいては、テキスト中から時間情報に関する表現を抽出し、記述される表現と規格化された構造とを紐付け、プログラムから利用できるように変換しなければなりません。

そこで、時間情報にまつわる表現を網羅的に収集し抽出ルールを作成し、それを元にテキスト中から候補となる表現を取得、そして時間情報のアノテーション規格に対応付けることでプログラミング言語の時間型との変換を行うための、時間情報の解析器を作成しました。

## 機能

- ルールベースによる日本語テキストからの日付や時刻、期間や頻度といった時間情報表現を抽出
- アラビア数字/漢数字、西暦/和暦などの多彩なフォーマットに対応
- 時間表現のdatetime/timedelta形式への変換サポート

## 抽出対象の具体例

- 日付表現
    - `2021年7月18日`, `2021/07`, `令和3年7月18日`, `2021年度`, `21世紀`, etc.
- 時間表現
    - `12時34分56秒`, `9:00 AM`, `午前`, etc.
- 持続時間表現
    - `1年間`, `3時間`, `1時間30分`, etc
- 頻度集合表現
    - `3ヶ月に1回`, `3日に1日`, `3日おき`, `毎月`, etc.

実際のテキストからの抽出事例は[具体例](examples.md)を参照ください。

## 参考文献
本パッケージは、以下の論文で提案されている時間情報アノテーションの枠組みを元に作成しています。本ドキュメントの`[1]`, `[2]`は下記と対応しています。

1.  [小西光, 浅原正幸, & 前川喜久雄. (2013). 『現代日本語書き言葉均衡コーパス』 に対する時間情報アノテーション. 自然言語処理, 20(2), 201-221.](https://www.jstage.jst.go.jp/article/jnlp/20/2/20_201/_article/-char/ja/)
2.   [成澤克麻 (2014)「自然言語処理における数量表現の取り扱い」東北大学大学院 修士論文](http://www.cl.ecei.tohoku.ac.jp/publications/2015/mthesis2013_narisawa_submitted.pdf)
