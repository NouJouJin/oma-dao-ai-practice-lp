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
├── README.md           # このファイル
├── PASSWORD_SETUP.md   # パスワード変更の詳細ガイド
├── DEPLOY.md           # GitHub Pagesデプロイガイド
├── SURVEY_GUIDE.md     # Google Formsアンケート作成ガイド
├── .gitignore          # Git除外設定
└── .nojekyll           # GitHub Pages設定
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
5. **実践ワークショップ**
   - 10人分の個別Google Docsテンプレートリンク
   - アクセス権申請の案内
   - AIツール推奨リスト
   - AIプロンプト例（基本版・段階的版）
6. **発表・投票** - 発表の流れと投票方法
7. **アンケート** - 講義の感想、成果物公開許可の確認
8. **フッター** - Metagri研究所情報、SNSリンク

## ✨ 主な機能

### 1. DAO設計書テンプレート（10人分）

受講者ごとに専用のGoogle Docsテンプレートを用意できます。

- 受講者名とリンクを表形式で表示
- アクセス権申請の手順を明記
- `index.html` 内のテーブルで管理

**設定方法:**
1. Google Docsでテンプレートを10個作成
2. 各テンプレートの共有設定で「リンクを知っている全員」または「特定のユーザー」を設定
3. `index.html` のテーブル内のリンクを各テンプレートのURLに更新

### 2. アンケート機能

講義終了後のフィードバック収集用アンケートセクション。

- 第1回・第2回の満足度評価
- 理解度の変化（定量評価）
- 成果物の公開許可確認
- 公開時のニックネーム/名称の記入欄

**設定方法:**
1. `SURVEY_GUIDE.md` を参照してGoogle Formsを作成
2. 作成したフォームのURLを `index.html` のアンケートボタンに設定

### 3. パスワード保護

受講者のみがアクセスできるセキュリティ機能。

- デフォルトパスワード: `oma2024`
- 変更方法は `PASSWORD_SETUP.md` を参照

## 🔧 セットアップ手順

### ステップ1: 受講者名の設定

`index.html` のテーブル（734-783行）の受講者名を実際の名前に変更：

```html
<td>〇〇さん</td>
```

↓

```html
<td>田中さん</td>
```

### ステップ2: Google Docsテンプレートリンクの設定

1. Google Docsでテンプレートを10個作成（コピー機能を活用）
2. 各テンプレートの共有設定を行う
3. 各リンクを `index.html` のテーブルに設定

```html
<a href="#" onclick="alert('Google Docsのリンク1を設定してください'); return false;">
```

↓

```html
<a href="https://docs.google.com/document/d/あなたのドキュメントID/edit" target="_blank">
```

### ステップ3: アンケートフォームの作成と設定

1. `SURVEY_GUIDE.md` を参照してGoogle Formsを作成
2. フォームのURLを `index.html` の989行目に設定

```html
<a href="#" class="button button-large" onclick="alert('Google FormsのアンケートURLをここに設定してください'); return false;">
```

↓

```html
<a href="https://forms.gle/あなたのフォームID" class="button button-large" target="_blank">
```

### ステップ4: パスワードの変更（推奨）

1. `PASSWORD_SETUP.md` を参照
2. 新しいパスワードのSHA-256ハッシュを生成
3. `index.html` の `PASSWORD_HASH` を更新

### ステップ5: デプロイ

1. `DEPLOY.md` を参照してGitHub Pagesに公開
2. URLとパスワードを受講者に配布

## 📞 サポート

問題や質問がある場合は、Metagri研究所Discordコミュニティへ：
https://discord.gg/hyw3AkKa8e

---

Presented by 農情人 / Metagri研究所
