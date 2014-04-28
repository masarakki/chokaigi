# chokaigi

超会議3の超チューニンガソンでつくったもの

## 何してるの?

元ファイルである `public_html/index.html` を読み込んで

- jsとcssを1つにまとめてs3に置く (毎回新しい名前でファイル生成)
- オプションでimageをs3に置く
- html内のjs/css/imageの外部呼び出しをcloud frontのドメインに変更
  - cloud frontのドメイン(distribution)が複数あればラウンドロビンするようにする
- js/css/html を minify

## 使い方

    bin/assets

画像のアップロードもするなら

    END_IMAGE=true bin/assets
    
    
`gen/index.html` に速くなったバージョンの `index.html` が生成される
