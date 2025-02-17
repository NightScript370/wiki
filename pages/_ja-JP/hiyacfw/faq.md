---
lang: ja-JP
layout: faq
section: hiyacfw
title: よくある質問とトラブルシューティング
long_title: hiyaCFWのよくある質問とトラブルシューティング
category: other
description: hiyaCFWためのよくある質問とトラブルシューティング
---

#### hiyaCFWのSDNANDにアプリまたはDSiウェアをインストールするにはどうすればいいですか？
SDNANDにアプリをインストールするには、 [TMFH](https://github.com/JeffRuLz/TMFH/releases/latest)を使用する必要がありますが、古いDS自作ソフトには互換性がないかもしれません。
- ゲームカードのダンプをインストールしたい場合は、[フォワーダー](../ds-index/forwarders)を使用する必要があります

#### #-2435-8325エラーコードを取得するのはなぜですか？
ニンテンドーDSiが起動時にこのフォーマット（#が数字である）でエラーが表示された場合は、つまりブートステージ2はSDNANDに何か問題があると考えているということです。 これは通常に、[hiyaCFWを再インストールする](installing)ことによって修正されます。

#### hiyaCFWの起動時に「エラーが発生しました」というメッセージが表示されるのはなぜですか？
ニンテンドーDSiメニューが問題を検出すると、通常にこの一般的なエラーメッセージが表示されます、原因のいくつかは：

##### 空き容量のバグ
大容量ストレージデバイスの空き容量を確認する時に、ニンテンドーDSiメニューにバグがあります。 これは実物のNANDでは発生しませんが（チップはわずか256 MiBなので）、SDカードを使用している時に発生する可能性があります。

何が動作する・しないは、一つ置きの2つのギガバイトの範囲に依存します。 例えば、0〜2GiBの空き容量は動作しますが、2〜4GiBは動作しません。 同じことは、SDカードの容量になるまで、4〜6GiB対6〜8GiBなどに当てはまります。

最新のhiyaCFWバージョンでは、これを回避するにはダミーファイルを作成できるため、必ず最新のバージョンの[hiyaCFW](https://github.com/RocketRobz/hiyaCFW/releases/latest/download/hiyaCFW.7z)をダウンロードし、`hiya.dsi`を「for SDNANDSD card」からSDカードのルートにコピーしてください。

##### 40タイトル以上
ニンテンドーDSiメニューには39タイトルの制限があります。 それ以上のものがある場合は、 `sd:/title`のフォルダからいくつかを削除しますか、[TMFH](https://github.com/JeffRuLz/TMFH/releases/latest)を使ってアンインストールしてください。

##### DSiWareの使用する容量が多すぎます
`00030004`フォルダには、DSiWare用の200ブロック（25MB）の制限もあります。 これは、[TMFH](https://github.com/JeffRuLz/TMFH/releases/latest)を使用してDSiウェアをシステムアプリとしてインストールすることで回避できます。

##### 無効なタイトル
hiyaCFWにタイトルを追加する時に考慮する必要があることがいくつかあります：
- [フォワーダー](../ds-index/forwarders)を使用せずにゲームカードのダンプを実行することができません
- 自作ソフトは、ニンテンドーDSiメニューから動作するには最新のツールを使用して正しく構築する必要があります
