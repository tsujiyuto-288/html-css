# cssの色々なプロパティ

## ✒️background-image

背景画像を指定する。

```css
.footer {
  background-image: url("../images/test背景.png");
}
```

画像のパスは `url()` の中に書く。

### 背景を画像にする際によく使用するプロパティ

| プロパティ            | よく使う値  | 意味                                       |
| --------------------- | ----------- | ------------------------------------------ |
| `background-repeat`   | `no-repeat` | 背景画像を繰り返さない                     |
| `background-size`     | `cover`     | 要素全体を埋める。画像が切れることがある   |
| `background-size`     | `contain`   | 画像全体を表示する。余白ができることがある |
| `background-position` | `center`    | 背景画像を中央に表示する                   |

### 背景画像でよく使う形

```css
.footer {
  background-image: url("../images/test背景.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
```

## ✒️opacity

不透明度を指定する
値は、0.0 ~ 1.0 までで不透明度を指定する。

```css
/* 70%表示されて30%透明になる */
.footer p {
  opacity: 0.7;
}
```

## ✒️letter-spacing

文字の間を指定する

```css
/* 10px分隙間が開く */
.footer p {
  letter-spacing: 10px;
}
```
