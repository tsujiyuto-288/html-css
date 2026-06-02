# フォームについて

## ⭐️label

入力欄の説明を書くタグ。
`p`タグではなく、基本的には`label`を使う。

```html
<label for="name">名前</label> <input id="name" type="text" />
```

`label`の`for`には、対象のフォーム部品の`id`を書く。
`class`や`name`ではなく、`id`と紐づく。

```html
<label for="email">メールアドレス</label> <input id="email" type="email" />
```

ラベルをクリックすると、紐づいた入力欄にフォーカスできる。
スクリーンリーダーにも「この入力欄が何の入力欄なのか」が伝わりやすい。

### labelの書き方

よく使うのは、`for`と`id`で紐づける書き方。

```html
<label for="password">パスワード</label> <input id="password" type="password" />
```

`label`の中に`input`を入れる書き方もある。
特に`checkbox`や`radio`で見かける。

```html
<label>
  <input type="checkbox" />
  利用規約に同意する
</label>
```

基本は`label for` + `id`。
`checkbox`や`radio`では、`label`の中に入れる書き方もよく使われる。

## ⭐️input

1行入力、チェックボックス、ラジオボタンなどを作るタグ。
`type`属性で入力の種類を変える。

```html
<input type="text" />
<input type="email" />
<input type="password" />
```

`type`を書かない場合は、基本的に`type="text"`として扱われる。
ただし、実務では分かりやすいので`type="text"`と明記することが多い。

```html
<input /> <input type="text" />
```

### よく見るinput type

```html
<input type="text" />
<input type="email" />
<input type="password" />
<input type="number" />
<input type="tel" />
<input type="checkbox" />
<input type="radio" />
<input type="file" />
<input type="hidden" />
<input type="submit" />
```

| type       | 用途                   |
| ---------- | ---------------------- |
| `text`     | 普通の1行テキスト      |
| `email`    | メールアドレス         |
| `password` | パスワード             |
| `number`   | 数値                   |
| `tel`      | 電話番号               |
| `checkbox` | 複数選択・同意チェック |
| `radio`    | 1つだけ選択            |
| `file`     | ファイルアップロード   |
| `hidden`   | 画面に出さない値       |
| `submit`   | フォーム送信ボタン     |

電話番号は`number`ではなく、`tel`を使うことが多い。
先頭の`0`やハイフンを扱いやすいため。

```html
<input type="tel" />
```

`submit`はフォーム送信用のボタン。
最近は`button`タグで書くことも多い。

```html
<!--buttonタグでの書き方↓-->
<button type="submit">送信</button>
```

### inputでよく使う属性

`input`で実務的に理解しておきたい属性。

```html
<input type="text" placeholder="山田太郎" required />
<input type="text" value="初期値" />
<input type="text" required />
<input type="checkbox" checked />
<input type="text" disabled />
<input type="text" readonly />
<input type="text" maxlength="20" />
<input type="number" min="1" max="99" />
<input type="file" accept="image/*" />
```

| 属性          | type                 | 意味                                 |
| ------------- | -------------------- | ------------------------------------ |
| `placeholder` | 入力欄がある系       | 入力前に薄く表示される入力例・ヒント |
| `value`       | ほぼ全て             | 初期値、または送信される値           |
| `required`    | ほぼ全て             | 必須入力にする                       |
| `checked`     | `checkbox` / `radio` | 最初から選択済みにする               |
| `disabled`    | ほぼ全て             | 操作できない状態にする               |
| `readonly`    | 入力欄がある系       | 表示はするが編集できない状態にする   |
| `maxlength`   | 文字や数字入力系     | 入力できる最大文字数                 |
| `min` / `max` | `number`             | 数値の最小値・最大値                 |
| `accept`      | `file`               | 受け取るファイルの種類を指定する     |

**※ typeはあくまで例。正確な仕様は都度確認**
