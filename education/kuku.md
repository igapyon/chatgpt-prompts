# 九九の音読

A x B = C (Pronunciation)
A: 1-9, B: 1-9, C: A x B

## 期待される生成例

1 x 1 = 1 (いんいち が いち)
1 x 2 = 1 (いんに が に)
1 x 3 = 1 (いんさん が さん)
...
2 x 3 = 6 (にさん が ろく)
2 x 4 = 8 (にし が はち)
2 x 5 = 10 (にご じゅう)
...
4 x 2 = 8 (しに が はち)
...
5 x 8 = 40 (ごは しじゅう)
...
6 x 7 = 42 (ろくしち しじゅうに)
...
9 x 8 = 72 (くは しちじゅうに)
9 x 9 = 81 (くく はちじゅういち)

ここで、Aは 1から9までの数字、Bも 1から9までの数字、Cは A x B の結果を表します。
Pronunciationは、対応する語呂合わせ音読を `ひらがな` で示します。気をつけるべき発音の変化については以下に示しいます。

## 気をつけるべき発音の変化

- C が 1桁の数字の場合にのみ、Cの前に `が` を入れます。例: 2 x 3 の場合 `にさん が ろく` となり、2 x 5 の場合 `にご じゅう` になります。
- A が 1 の場合は、`いん` と発音します。例: 1 x 1 の場合 `いんいち が いち`、1 x 4 の場合 `いんし が し` となります。
- A と B が同じ数字の場合、A と B の間に `ん` を挿入します。例: 2 x 2 の場合、`ににんに が し` となります。
- A が 9 の場合は `く` となります。
- B が 9 の場合は `く` と発音しますが、A が 5,6,8 の場合は `っく` となります。例: 3 x 3 は `さざん が く` となり、6 x 9 は `ろっく ごじゅうし` となります。
- 1 x 1 は `いんいち`、1 x 9 は `いんく`、2 x 1 は `にいち`、2 x 2 は `ににん`、2 x 6 は `にろく`、2 x 9 は `にく`、3 x 3 は `さざん`、3 x 6 は `さぶろく`、3 x 8 は `さんぱ`、4 x 4 は `しし`、4 x 8 は `しわ`、4 x 9 は `しく`、5 x 5 は `ごご`、5 x 8 は `ごは`、5 x 9 は `ごっく`、7 x 7 は `しちしち`、7 x 8 は `しちは`、8 x 4 は `はっし`、8 x 8 は `はっぱ`、8 x 9 は `はっく`、9 x 5 は `くご`、9 x 8 は `くは` となります。 
- 4は `し` となり、`よん` は使いません。
- 7は `しち` となり、`なな` は使いません。
- 45 は `しじゅうご` となります。

## 作業

この法則を元に、九九の掛け算の語呂合わせ音読の生成結果を示してください。