# Zen Server - Minecraft クロスプレイサーバー

Zenサーバーの公式Webサイトです。黒をテーマにしたかっこいいデザインで、Minecraftクロスプレイサーバーの魅力を紹介します。

## 🎮 特徴

- **クロスプレイ対応**: Java版、Bedrock版、モバイル版など、あらゆるプラットフォームから参加可能
- **24/7稼働**: 高性能サーバーで安定した24時間稼働
- **安全な環境**: 厳格なルールと優秀なモデレーターチームで、安全で楽しい環境を提供

## 🎨 デザイン

- 黒をベースにしたダークテーマ
- 緑のアクセントカラー（Minecraftらしさ）
- モダンで洗練されたUI/UX
- レスポンシブデザイン（デスクトップ・モバイル対応）

## 🛠️ 技術スタック

- **フレームワーク**: React + Vite
- **スタイリング**: Tailwind CSS
- **UIコンポーネント**: shadcn/ui
- **アイコン**: Lucide React
- **アニメーション**: Framer Motion

## 📦 インストール

```bash
# 依存関係をインストール
npm install

# 開発サーバーを起動
npm run dev

# プロダクションビルド
npm run build
```

## 🚀 デプロイ

### GitHub Pages

1. GitHubリポジトリを作成
2. コードをプッシュ
3. Settings > Pages で Source を "GitHub Actions" に設定
4. 以下のワークフローファイルを `.github/workflows/deploy.yml` に作成:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    
    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18'
        
    - name: Install dependencies
      run: npm install
      
    - name: Build
      run: npm run build
      
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./dist
```

### その他のプラットフォーム

- **Vercel**: `vercel --prod`
- **Netlify**: `dist` フォルダをドラッグ&ドロップ
- **Firebase Hosting**: `firebase deploy`

## 📁 プロジェクト構造

```
zen-server-website/
├── src/
│   ├── assets/          # 画像・アセット
│   ├── components/      # UIコンポーネント
│   ├── hooks/          # カスタムフック
│   ├── lib/            # ユーティリティ
│   ├── App.jsx         # メインアプリケーション
│   ├── App.css         # カスタムスタイル
│   └── main.jsx        # エントリーポイント
├── public/             # 静的ファイル
├── dist/              # ビルド済みファイル
└── package.json       # 依存関係
```

## 🎯 含まれるセクション

1. **ヒーローセクション** - インパクトのあるメインビジュアル
2. **サーバー紹介** - 特徴と魅力の説明
3. **参加方法** - Java版・Bedrock版の接続手順
4. **ギャラリー** - サーバー内の建築物とコミュニティ
5. **利用規約** - サーバールールとペナルティ
6. **フッター** - リンクとコミュニティ情報

## 🖼️ 画像アセット

- Zenサーバー専用ロゴ
- 未来的な都市のヒーロー画像
- コミュニティの温かい雰囲気を表現した画像
- Minecraftマルチプレイヤーの様子
- ダークテーマの建築物
- クロスプレイの説明画像

## 📝 ライセンス

このプロジェクトはMITライセンスの下で公開されています。

## 🤝 貢献

プルリクエストやイシューの報告を歓迎します！

---

© 2024 Zen Server. All rights reserved.

