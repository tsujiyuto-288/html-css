# cssの色々な情報まとめ

## background-image:

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
