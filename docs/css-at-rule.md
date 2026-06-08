# cssのアットルール

アットルールは、`@` から始まるCSSの特別な書き方。

CSS全体に関わる命令を書く時に使う。

```css
@media @import @font-face @keyframes;
```

## ✒️@media

画面幅などの条件に合わせて、CSSを切り替える。

```css
@media (max-width: 600px) {
  body {
    background-color: #333333;
  }
}
```

この場合、画面幅が `600px` 以下の時だけ、`body` の背景色が変わる。

`@media` の中にも、普通のCSSと同じようにセレクタを書く必要がある。

```css
@media (max-width: 600px) {
  .container {
    display: block;
  }
}
```

`@media` は、端末がスマホかPCかを直接判定するものではない。
基本的には、画面幅などの条件に当てはまるかをブラウザが判定する。

```text
画面幅が600px以下
→ 中のCSSを適用する

画面幅が600pxより大きい
→ 中のCSSを適用しない
```

PCでもブラウザの横幅を小さくすれば、条件に当てはまる。

## @mediaの使い所

`@media` は、画面幅に合わせて見た目やレイアウトを調整する時に使う。

```css
.container {
  display: flex;
}

@media (max-width: 600px) {
  .container {
    display: block;
  }
}
```

この場合、通常は横並びで、画面幅が狭い時は縦並びになる。

大規模なWebサービスで、端末ごとにHTMLやUI構造自体を変える場合、`@media` が担当する範囲とは別の話になる。
その場合は、サーバー側、JavaScript、コンポーネントの切り替えなどで制御することが多い。

`@media` は、CSS側で画面幅などの条件に応じて、見た目やレイアウトを調整するために使う。

## ✒️@import

別のCSSファイルを読み込む。

```css
@import url("./reset.css");

body {
  margin: 0;
}
```

この場合、今のCSSファイルから `reset.css` を読み込む。

`@import` は、基本的にCSSファイルの先頭の方に書く。

```css
@import url("./reset.css");
@import url("./base.css");

.box {
  background-color: aqua;
}
```

ただし、CSSファイルの読み込みはHTMLの `link` で書くことも多い。

```html
<link rel="stylesheet" href="../css/reset.css" />
<link rel="stylesheet" href="../css/main.css" />
```
