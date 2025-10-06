# Perl Mojolicious Application on GitHub Codespaces

このリポジトリはGitHub CodespacesでPerlのMojoliciousアプリケーションを動かすサンプルです。

## 構成

- **Carton + cpanfile**: 依存関係管理
- **Mojolicious**: WebフレームワークでHello Worldアプリケーション

## 使い方

### 1. Codespacesで開く

GitHub上でこのリポジトリを開き、"Code" > "Codespaces" > "Create codespace on main" をクリック

### 2. アプリケーションを起動

```bash
carton exec -- morbo app.pl
```

### 3. アクセス

ポート3000が自動的にフォワードされるので、ブラウザで開くか、以下のコマンドで確認：

```bash
curl http://localhost:3000
```

"Hello World" が返されます。

## ファイル構成

- `.devcontainer/devcontainer.json`: Codespaces設定
- `cpanfile`: Perl依存パッケージ定義
- `app.pl`: Mojolicious Hello Worldアプリケーション
