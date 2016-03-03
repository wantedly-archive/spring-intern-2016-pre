## HTMLとは

> HTMLとは、Hyper Text Markup Language（ハイパーテキスト・マークアップ・ランゲージ）の略で、Webページを作るための最も基本的なマークアップ言語のひとつです。
http://techacademy.jp/magazine/4843

簡単にいうと、

 - Webサイトの「設計図」

### WantedlyのHTMLをみてみよう

![2016-03-01 18 04 56](https://cloud.githubusercontent.com/assets/4524771/13470500/cd8ebc66-e0ef-11e5-8a72-36730b73cec4.png)

![2016-03-01 18 06 21](https://cloud.githubusercontent.com/assets/4524771/13470563/212d459a-e0f0-11e5-9f9d-4e22e9ad0d86.png)

![2016-03-01 18 07 03](https://cloud.githubusercontent.com/assets/4524771/13470531/f100b58c-e0ef-11e5-8f6a-efa749d2d3a9.png)

ブラウザでどんなサイトのソースも閲覧することができる。

### [ワーク]HTML書いてみよう。

`app/index.html`をエディタを開いて、以下を書いてみよう。

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>すごいタイトル</title>
  </head>
  <body>
    <h1>最高な見出し</h1>
    <h2>最上の見出し</h2>
    <p>先進的なパラグラフ</p>
  </body>
</html>
```

Webページっぽいものが表示される。

### すごいな、どうやったんだ

 - ブラウザがHTMLを解析
 - DOMツリー/レンダーツリーを生成
 - ブラウザ上に描写（レンダー）

[cf. ブラウザの仕組み: 最新ウェブブラウザの内部構造](http://www.html5rocks.com/ja/tutorials/internals/howbrowserswork/#The_render_tree_relation_to_the_DOM_tree)

### DOMって？

DOM (Document Object Model) の略で、HTMLを操作するためのAPI。
HTMLの世界とJavascriptの世界の架け橋。

#### DOMツリー

ブラウザでは、HTMLを階層構造（DOMツリー）として解釈する。

![2016-03-01 21 00 57](https://cloud.githubusercontent.com/assets/4524771/13470395/5b8f40a4-e0ef-11e5-8f72-ec886141ab9a.png)

### タグ（要素）

`<html>`や`<p>`,`<h1>`といった記号は**タグ（要素）**と呼ばれており、
例えば、`<p>`は**パラグラフ**で、`<h1>`は**最上位の見出し**であるといったように、それぞれが意味を持っている。

cf. [MDNのHTML 要素リファレンス](https://developer.mozilla.org/ja/docs/Web/HTML/Element)

htmlは人間だけではなくて、ブラウザやクローラーなどのコンピュータも読む。タグが意味を持ち、その意味に沿ってにコーディングすることで、コンピューターにも、どんなサイトなのかをわかってもらうことを可能にしてる。

### 属性

HTMLタグは、**属性**を持つことができる。
代表的なのは、`id`と`class`属性で、例えば以下のように指定することで、
CSS や Javascript から要素を参照するときの目印になる。

```html
/* id */
<div class="id"></div>

/* class */
<div class="main"></div>
```
