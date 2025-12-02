# cliの使い方

## ダウンロード

GitHubにコードが公開されており、最新のビルドはリリースからダウンロードできます。
- https://github.com/candylfs/candylfs-cli/releases

## コマンド群

### GitHubログイン
```
candylfs login <TenantID>
```

コマンドを実行すると、以下のような表示が出ます

```
Logging in to tenant: my-tenant-id

→ Open this URL in your browser:
  https://github.com/login/device

→ Enter this code:
  XXXX-XXXX
```

1. 表示されたURLをブラウザで開く
2. 表示されたコードを入力
3. GitHubで認証を承認

認証が完了すると、トークンが自動的に保存されます。
自動でcli側でGit Credential Helperに自動でトークン情報が埋め込まれ、特に設定することなくcandylfsの認証を通せます。

### ログアウト(クレデンシャル削除)

#### 全てのテナントのからログアウトする場合
```
candylfs logout
```

#### 特定のテナントのからログアウトする場合
```
candylfs logout  <TenantID>
```
### 設定確認
```
candylfs config show
```
