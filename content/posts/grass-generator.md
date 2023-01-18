---
title: grass-generator
date: 2023-01-18
description: "草を生やすライブラリgrass-generatorを作ったよ"
image: https://github.com/ta1m1kam/grass-generator/raw/main/docs/images/example.png
---

# 作った経緯
Githubではコントリビュートに応じて草が生える機能があります。
それを応用した自身のアプリケーションが作成したくて作りました。
canvasとsvgのどちらかで生成することができて、label等もカスタマイズ可能でです。

npm packageとしてnpm registryに登録してあるのでどなたでも使用可能です。

[grass-generator](https://www.npmjs.com/package/grass-generator)

# 機能

以下のようなjsonデータを取得 or 作成します。

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

このデータを以下のようにライブラリをimportして、APIを実行するだけです。

## SVG
```js
import { drawGrassSvg } from 'grass-generator';
drawGrassSvg(document.getElementById('svg'), { data });
```

## Canvas
```js
import { drawGrassCanvas } from 'grass-generator';
drawGrassCanvas(document.getElementById('canvas'), { data });
```


# 今後
これを使ってデイリータスクの進捗計測アプリでも作ろうかなと思います。
以上！さようなら！
