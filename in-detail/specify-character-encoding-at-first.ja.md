# 最初に文字エンコーディングを指定する

仕様では文書の先頭1024バイトまでに文字エンコーディングを指定することを要求しています。

悪い例:

    <head>
      <meta content="width=device-width" name="viewport">
      <meta charset="UTF-8">
      ...
    </head>

良い例:

    <head>
      <meta charset="UTF-8">
      <meta content="width=device-width" name="viewport">
      ...
    </head>


## 解説

文字コードの指定は`head`要素内で行う必要がありますが、その位置までは明確な規定はありません。しかしなるべく先頭、できれば一番最初に指定しておくべきでしょう。それはブラウザーの文字コード自動判別機能と密接な関係があります。

ブラウザーの文字コード判別はHTMLドキュメント全体を読み込んでから行われるとは限りません。あるブラウザーはファイルの先頭のみから判別を行います。また`title`要素が文字コード指定より前にあるとうまく判別できないという問題もかつてありました。そのためファイルの先頭から1024バイトまでに書くことが推奨されています。

HTML5ではDOCTYPE宣言他、多くの記述がシンプルになってはいます。良い例で挙げたように`head`要素の先頭に書くと決めておけば、ほぼ確実に1024バイトまでに収まるでしょう。
