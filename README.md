# satysfi-resume

[SATySFi](https://github.com/gfngfn/SATySFi) の履歴書テンプレートです。

## Usage

`resume.satyh` をインポートします。

```
@import resume
```

```
Resume.document (|
  date = (2024, 4, 8); % 記述日 年/月/日 (int * int * int)
  birthday = (2003, 1, 1); % 誕生日 年/月/日 (int * int * int)
  age = 21; % 満年齢 (int)
  sex = { 男 }; % 性別 (inline-text)
|) '<
  % ここに履歴書の内容を記述します
>
```

以下のコマンドを用いて記述します。

- `+face-img (string)`: 顔写真のファイル名を指定します。4:3の画像を指定してください。
- `+name (inline-text) (inline-text)`: 名前を指定します。それぞれ姓/名です。
- `+name-ruby (inline-text) (inline-text)`: 名前のふりがなを指定します。それぞれ姓/名です。
- `+address1 (inline-text) (inline-text) (inline-text) (inline-text) (string)`:
  住所を記述します。それぞれ 郵便番号 / 住所 / 住所振り仮名 / 電話番号 / メールアドレス です。メールアドレスはリンクが付きます。
- `+address2 (inline-text) (inline-text) (inline-text) (inline-text) (string)`:
  連絡先を記述します。引数は `+address1` と同様です。

- `education-history (inline-text) (inline-text) (inline-text)`:
  学歴を記述します。それぞれ 年 / 月 / 内容 です。
- `career-history (inline-text) (inline-text) (inline-text)`:
  職歴を記述します。それぞれ 年 / 月 / 内容 です。
- `qualification-history (inline-text) (inline-text) (inline-text)`:
  免許/資格を記述します。それぞれ 年 / 月 / 内容 です。
- `+self-motivation ?:(context -> context) (block-text)`:
  志望動機を記述します。 
- `+self-pr ?:(context -> context) (block-text)`:
  趣味・特技・アピールポイントを記述します。
- `+self-desired ?:(context -> context) (block-text)`:
  本人希望を記述します。

詳しい書き方は `resume.saty` を参照してください。
