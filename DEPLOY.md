# デプロイガイド

## 🚀 GitHub Pagesへのデプロイ

### 前提条件

- GitHubアカウント
- リポジトリへのプッシュ権限

### デプロイ手順

#### 1. コードをプッシュ

```bash
# 現在のブランチを確認
git branch

# すべての変更をステージング
git add .

# コミット
git commit -m "Initial commit: OMA DAO AI Practice LP"

# プッシュ（初回）
git push -u origin claude/first-session-setup-011CUvBQa25FEyMkXa3P57i6
```

#### 2. GitHub Pagesを有効化

1. GitHubリポジトリページにアクセス
2. **Settings** タブをクリック
3. 左サイドバーから **Pages** をクリック
4. **Source** セクションで以下を設定：
   - Source: `Deploy from a branch`
   - Branch: `claude/first-session-setup-011CUvBQa25FEyMkXa3P57i6`
   - Folder: `/ (root)`
5. **Save** をクリック

#### 3. デプロイ完了を確認

- 数分後、以下のようなURLでアクセス可能になります：
  ```
  https://[GitHubユーザー名].github.io/oma-dao-ai-practice-lp/
  ```

- デプロイ状況は **Actions** タブで確認できます

### 更新のプッシュ

```bash
# ファイルを編集後
git add .
git commit -m "Update content"
git push
```

GitHub Pagesは自動的に更新されます（数分かかる場合があります）。

## 🧪 ローカルでのテスト

### 方法1: Pythonの簡易サーバー（推奨）

```bash
# プロジェクトディレクトリで実行
python3 -m http.server 8000

# ブラウザで開く
# http://localhost:8000
```

### 方法2: 直接ブラウザで開く

```bash
# Macの場合
open index.html

# Windowsの場合
start index.html

# Linuxの場合
xdg-open index.html
```

## 🔒 パスワードのテスト

### デフォルトパスワード

```
oma2024
```

### テスト手順

1. ページにアクセス
2. パスワード入力画面が表示される
3. `oma2024` を入力してログイン
4. メインコンテンツが表示される
5. ログアウトボタンをクリック
6. 再度ログイン画面に戻る

## 📱 レスポンシブデザインのテスト

### ブラウザの開発者ツールを使用

1. ブラウザで開発者ツールを開く（F12 または Cmd+Option+I）
2. デバイスツールバーを開く（Cmd+Shift+M または Ctrl+Shift+M）
3. 以下のデバイスサイズでテスト：
   - iPhone 12/13/14 (390x844)
   - iPad (768x1024)
   - Desktop (1920x1080)

### 確認項目

- ✅ テキストが読みやすい
- ✅ ボタンがタップしやすい
- ✅ 横スクロールが発生しない
- ✅ 画像が適切に表示される

## 🐛 トラブルシューティング

### GitHub Pagesで404エラー

**原因**: ブランチやフォルダの設定が間違っている

**解決方法**:
1. Settings > Pages で設定を確認
2. 正しいブランチが選択されているか確認
3. `index.html` がルートディレクトリにあることを確認

### スタイルが反映されない

**原因**: ブラウザキャッシュ

**解決方法**:
1. Shift + F5 でハードリロード
2. ブラウザのキャッシュをクリア
3. シークレットモードで確認

### パスワードが合わない

**原因**: ハッシュ生成時のミス

**解決方法**:
1. `PASSWORD_SETUP.md` を参照
2. ハッシュを再生成
3. `index.html` の `PASSWORD_HASH` を更新

### GitHub Pagesの更新が反映されない

**原因**: GitHub Actionsのビルド遅延

**解決方法**:
1. GitHubリポジトリの **Actions** タブを確認
2. ビルドが完了するまで数分待つ
3. ブラウザのキャッシュをクリア

## 🔧 カスタマイズ

### Google Docsテンプレートリンクの追加

`index.html` の以下の部分を更新：

```html
<a href="#" class="button button-large" onclick="alert('Google Docsのリンクをここに設定してください'); return false;">
```

↓

```html
<a href="https://docs.google.com/document/d/あなたのドキュメントID/edit" class="button button-large" target="_blank">
```

### カラーテーマの変更

`index.html` の `:root` セクションで色を調整：

```css
:root {
    --primary-green: #2d5016;  /* メインカラー */
    --light-green: #4a7c2c;    /* サブカラー */
    --accent-green: #6ba83e;   /* アクセントカラー */
    --tech-blue: #0066cc;      /* テクノロジーカラー */
}
```

## 📊 アクセス解析（オプション）

### Google Analyticsの追加

`index.html` の `</head>` の直前に追加：

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔐 セキュリティチェックリスト

- [ ] パスワードハッシュを変更した
- [ ] デフォルトパスワードを使用していない
- [ ] パスワードを安全な方法で配布した
- [ ] 公開SNSにパスワードを投稿していない
- [ ] Google Docsのリンクを設定した
- [ ] テンプレートの閲覧権限を確認した

## 📞 サポート

問題が解決しない場合：

1. GitHubのIssuesで報告
2. Metagri研究所Discordで質問
3. README.mdを再確認

---

Happy Deploying! 🚀
