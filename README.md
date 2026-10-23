# mov-map-data

飲食動画マップ（mov-map）アプリが読み込む動画一覧です。`videos.json` を書き換えて保存（Commit）すると、次にアプリを開いたときに反映されます。アプリを作り直す必要はありません。

## 書き方

`videos.json` は `[` と `]` の間に、1件ずつ `{ ... }` を `,` で区切って並べます。

```json
{
  "id": "shibuya-ramen-001",
  "shopName": "〇〇ラーメン 渋谷店",
  "genre": "ramen",
  "latitude": 35.6595,
  "longitude": 139.7005,
  "url": "https://www.instagram.com/reel/XXXXXXXX/",
  "postedAt": "2026-10-20"
}
```

| 項目 | 書くこと |
| --- | --- |
| `id` | ほかと重ならない好きな文字 |
| `shopName` | 店名 |
| `genre` | `ramen` `sushi` `yakiniku` `cafe` `sweets` `izakaya` `italian` `other` のどれか |
| `latitude` / `longitude` | Google マップで店を長押しすると出る数字（左が緯度、右が経度） |
| `url` | Instagram か TikTok の投稿URL |
| `postedAt` | 投稿日（YYYY-MM-DD） |

形が崩れている行はアプリに表示されません。いま入っている3件は見た目確認用の架空のサンプルなので、本物を足したら消してください。

## GitHub のサイト上で編集するには

1. `videos.json` を開いて、右上の鉛筆マークを押します。
2. 書き換えたら「Commit changes」を押します。
