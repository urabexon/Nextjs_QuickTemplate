# Next.js Frontend Template

モダンなフロントエンド開発のためのテンプレート。Next.js + Supabase + Google認証 + Docker対応でフルスタックアプリケーションを素早く構築できます。

## 機能

- **Next.js 14** (App Router)
- **Supabase** (データベース・認証)
- **Google認証** (One Tap対応)
- **Tailwind CSS** (スタイリング)
- **TypeScript** (型安全性)
- **Docker** (コンテナ化)
- **shadcn/ui** (UIコンポーネント)

## 環境構築

### 1. リポジトリのクローン

```bash
git clone <repository-url>
cd 21.Nextjs_QuickTemplate
```

### 2. 環境変数の設定

`.example`ファイルを`.env`にコピーして必要な値を設定：

```bash
cp .example .env
```

```.env
NEXT_PUBLIC_SUPABASE_URL=your-supabase-url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-supabase-anon-key
NEXT_PUBLIC_GOOGLE_CLIENT_ID=your-google-client-id
```

### 3. 開発環境の起動

#### 通常の開発環境

```bash
npm install
npm run dev
```

#### Docker環境

```bash
docker-compose up
```

## セットアップガイド

### Supabaseの設定

1. [Supabase](https://supabase.com/)でプロジェクトを作成
2. プロジェクトのURLとAnon Keyを環境変数に設定
3. 認証設定でGoogleプロバイダーを有効化

### Google認証の設定

1. [Google Cloud Console](https://console.cloud.google.com/)でプロジェクトを作成
2. OAuth 2.0認証情報を作成
3. Client IDを環境変数に設定
4. 承認済みのJavaScriptオリジンを追加

## プロジェクト構成

```
├── app/                    # Next.js App Router
│   ├── (auth-pages)/      # 認証関連ページ
│   ├── auth/              # 認証API
│   ├── protected/         # 保護されたページ
│   └── layout.tsx         # レイアウト
├── components/            # UIコンポーネント
│   ├── ui/               # shadcn/ui
│   └── tutorial/         # チュートリアル
├── utils/                # ユーティリティ
│   └── supabase/         # Supabase設定
├── lib/                  # 共通ライブラリ
├── Dockerfile            # Dockerイメージ定義
├── docker-compose.yml    # Docker環境構成
└── .dockerignore         # Docker除外ファイル
```

## 使用方法

### 認証機能

- サインアップ: `/sign-up`
- サインイン: `/sign-in`
- パスワードリセット: `/forgot-password`
- 保護されたページ: `/protected`

### 開発コマンド

```bash
# 開発サーバー起動
npm run dev

# プロダクションビルド
npm run build

# プロダクションサーバー起動
npm run start
```

### Docker コマンド

```bash
# 開発環境起動
docker-compose up

# バックグラウンド起動
docker-compose up -d

# 停止
docker-compose down

# 再ビルド
docker-compose up --build
```

## デプロイメント

### Vercel

1. GitHubリポジトリと連携
2. 環境変数を設定
3. デプロイ

### Docker

```bash
# イメージビルド
docker build -t nextjs-template .

# コンテナ起動
docker run -p 3000:3000 nextjs-template
```

## カスタマイズ

このテンプレートは以下の用途に適しています：

- SaaSアプリケーション
- 管理画面
- コーポレートサイト
- ポートフォリオサイト

### 追加可能な機能

- 多言語対応 (i18n)
- ダークモード
- PWA対応
- 決済機能 (Stripe)
- メール送信機能

## ライセンス

MIT License

## 貢献

プルリクエストやイシューは歓迎します。

## サポート

問題が発生した場合は、以下をご確認ください：

1. 環境変数が正しく設定されているか
2. Supabase・Googleの設定が正しいか
3. ポートが使用中でないか

詳細な設定方法は各サービスの公式ドキュメントを参照してください。