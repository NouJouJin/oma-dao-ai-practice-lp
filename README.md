# OMA DAO×AI実践講座 第2回 - ランディングページ

大妻マネジメントアカデミー（OMA）第2回講義「AI×web3で地域活性化企画を創る」の受講者専用ランディングページです。

## 🎯 概要

- **日時**: 2025年11月15日（土）5限※6限の一部
- **テーマ**: AI×web3で地域活性化企画を創る
- **講師**: 農情人（Metagri研究所）

## 🔒 セキュリティ

このLPはパスワード保護されています。
- クライアントサイドでSHA-256ハッシュ検証
- セッションストレージで認証状態を保持
- 受講者のみがアクセス可能

## 🚀 使い方

### ローカルで確認する場合

```bash
# シンプルなHTTPサーバーを起動
python3 -m http.server 8000

# ブラウザで開く
open http://localhost:8000
```

または、`index.html`を直接ブラウザで開くこともできます。

### GitHub Pagesでデプロイ

1. GitHubリポジトリの Settings > Pages へ移動
2. Source を "Deploy from a branch" に設定
3. Branch を `main` (または該当ブランチ) に設定
4. 保存後、数分で公開されます

公開URL: `https://[username].github.io/oma-dao-ai-practice-lp/`

## 📝 パスワード設定

現在のパスワードハッシュは `index.html` 内の以下の部分で設定されています：

```javascript
const PASSWORD_HASH = 'あなたのSHA-256ハッシュ';
```

### パスワードの変更方法

1. 新しいパスワードを決める
2. 以下のサイトでSHA-256ハッシュを生成
   - https://emn178.github.io/online-tools/sha256.html
3. `index.html` の `PASSWORD_HASH` を更新

## 📂 ファイル構成

```
oma-dao-ai-practice-lp/
├── index.html          # メインページ（パスワード保護機能含む）
├── package.json        # プロジェクト情報
└── README.md          # このファイル
```

## 🎨 技術スタック

- HTML5
- CSS3 (Flexbox, Grid, アニメーション)
- Vanilla JavaScript (ES6+)
- SHA-256 暗号化（Web Crypto API）

## 📚 コンテンツ構成

1. **ヘッダー** - タイトル、日時、講義の目的
2. **第1回の振り返り** - web3の基礎、成功事例・失敗事例
3. **今日のゴール** - DAO設計書の作成と発表
4. **参考事例** - Biwako DAO、川上牧場
5. **実践ワークショップ** - フォーマット、AIプロンプト例
6. **発表・投票** - 発表の流れと投票方法
7. **フッター** - Metagri研究所情報、SNSリンク

## 📞 サポート

問題や質問がある場合は、Metagri研究所Discordコミュニティへ：
https://discord.gg/hyw3AkKa8e

---

Presented by 農情人 / Metagri研究所
