## CSSとは

> CSS（Cascading Style Sheets、カスケーディング・スタイル・シート）とは、ウェブページのスタイルを指定するための言語です。
http://www.htmq.com/csskihon/001.shtml

### 基本的な書き方

```css
要素名 {
  プロパティ名: 値;
}
```

### 要素の文字の色を変えてみる。

`style.css`を以下のように編集して、

```css
h1 {
  color: #00A4BB;
}
```

`index.html`の`<head></head>`に以下を差し込む

```html
<link rel="stylesheet" href="./style.css">
```

色が変わる！

### classなどを使ってスタイルする要素を指定する

```html
<p class="wt-blue">先進的なパラグラフ</p>
```
```css
.wt-blue {
  color: #00A4BB;
}
```

class名でスタイルを変更する要素を指定できる。

### 擬似クラスを利用してのスタイルを指定する

要素にホバーしたときのスタイルを指定できる`:hover`や、
訪問済みのリンクのスタイルを指定できる`:viited`などある。

[cf. 疑似クラス (Pseudo-classes)](https://developer.mozilla.org/ja/docs/Web/CSS/Pseudo-classes)

```css
.green:hover {
  color: #9DA0A4;
  transition: all 0.5s ease;
}
```
ふわぁって背景が灰色になる。

### ブラウザによって使えるものが異なる。

例えば、レイアウトをすごく簡単に整えることができる、`Flexbox`などは、
IE8,9では利用することができない。

![image](https://cloud.githubusercontent.com/assets/4524771/13471381/b205cc6a-e0f3-11e5-96e7-c1574fdd6836.png)
http://caniuse.com/#feat=flexbox

新しくて便利なものはすぐ使いたくなるけど、サービスをどんなユーザーが利用するかを考える必要がある。（新卒ポータルはどうだろう）

#### ちなみに

つい先日、WantedlyもIE8から10までの対応をやめた。（IEのサポート切れに乗った）
流れに乗って決断することも大事。ずるずるサポートすることでWebの進化が遅れる。

### CSSの本気

http://codepen.io/juliangarnier/pen/idhuG
