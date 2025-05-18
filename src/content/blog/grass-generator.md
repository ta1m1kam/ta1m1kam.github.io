---
title: grass-generator
pubDate: 2023-01-18
description: "草を生やすライブラリgrass-generatorを作ったよ"
heroImage: "https://raw.githubusercontent.com/ta1m1kam/grass-generator/main/docs/images/example.png"
---

# 作った経緯

Github ではコントリビュートに応じて草が生える機能があります。
それを応用した自身のアプリケーションが作成したくて作りました。
canvas と svg のどちらかで生成することができて、label 等もカスタマイズ可能でです。

npm package として npm registry に登録してあるのでどなたでも使用可能です。

[grass-generator](https://www.npmjs.com/package/grass-generator)

# 機能

以下のような json データを取得 or 作成します。

```json
{
  "years": [
    {
      "year": "2023",
      "total": 0,
      "range": {
        "start": "2023-01-01",
        "end": "2023-12-31"
      }
    },
    {
      "year": "2022",
      "total": 360,
      "range": {
        "start": "2022-01-01",
        "end": "2022-12-31"
      }
    }
  ]
}
```

このデータを以下のようにライブラリを import して、API を実行するだけです。

## SVG

```js
import { drawGrassSvg } from "grass-generator";
drawGrassSvg(document.getElementById("svg"), { data });
```

## Canvas

```js
import { drawGrassCanvas } from "grass-generator";
drawGrassCanvas(document.getElementById("canvas"), { data });
```

# 今後

これを使ってデイリータスクの進捗計測アプリでも作ろうかなと思います。
以上！さようなら！
