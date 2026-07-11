# 週末おでかけルーレット (PWA版)

関東の子連れスポットを、天気・年齢・予算でしぼってルーレット提案するアプリ。
iPhoneのホーム画面に追加すると、フルスクリーンのアプリとして動きます。

## ファイル構成

- index.html … アプリ本体(単一ファイル)
- manifest.json … PWAマニフェスト
- sw.js … サービスワーカー(オフライン対応)
- icon-180.png / icon-192.png / icon-512.png … アプリアイコン

## デプロイ手順(GitHub Pages・株帳と同じ流れ)

1. GitHubで新しいリポジトリを作成(例: `odekake-roulette`)
2. この5ファイルをリポジトリ直下にアップロード
3. Settings → Pages → Branch を `main` / `(root)` にして Save
4. 数分後に `https://<ユーザー名>.github.io/odekake-roulette/` で公開されます

## iPhoneへのインストール

1. **Safari**で公開URLを開く(Chromeからは追加できません)
2. 共有ボタン(□↑)→「ホーム画面に追加」
3. ホーム画面の🎡アイコンから起動

## メモ

- おでかけ記録はlocalStorageに保存されます(そのiPhoneの中だけ。サーバには送られません)
- Safariの「履歴とWebサイトデータを消去」を実行すると記録も消えるのでご注意を
- 2回目以降はオフラインでも起動できます
- 更新版を配布したいときは sw.js の `CACHE = "odekake-v1"` の数字を上げてください
