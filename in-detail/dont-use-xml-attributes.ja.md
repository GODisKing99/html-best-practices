# XML属性は使わない

我々はHTML文書を書いています。

悪い例:

    <span lang="ja" xml:lang="ja">...</span>

良い例:

    <span lang="ja">...</span>


## 解説

XHTML 1.1仕様から参照されているXHTML 1.0仕様では必要に応じてXML属性も併記する必要がありました。悪い例で挙げたように、例えば`lang`属性を使用する場合には同じ値の`xml:lang`属性も併記する、と指示されています。

HTML5仕様ではこの`lang`属性と`xml:lang`属性についてわざわざ項が割かれています。おおまかに言うとHTML文書では書いてはならないとされており、XML文書でも書いても良い（MAY）程度に変更されています。

HTML文書を書き、[名前空間を使わないと][1]、事実上`xml:lang`属性以外にXML属性が使われそうな状況はありません。良い例で挙げたように書くべきです。


[1]: omit-namespaces.ja.md
