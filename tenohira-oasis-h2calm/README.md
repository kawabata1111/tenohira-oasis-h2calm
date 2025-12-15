# てのひらオアシスH₂calm 公式ホームページ

## プロジェクト概要

水素美容とヘッドリンパケアを組み合わせた出張ケアサロン「てのひらオアシスH₂calm（エイチツーカーム）」の公式ホームページです。

**キャッチフレーズ**: がんばる毎日に、ちょっと深呼吸を。

---

## ファイル構成

```
/
├── index.html          # メインHTMLファイル
├── style.css           # スタイルシート
├── script.js           # JavaScriptファイル
├── README.md           # このファイル
├── IMAGE_GUIDE.md      # 画像配置ガイド
└── images/             # 画像フォルダ（後で作成）
    ├── hero/           # ヒーローセクション用画像
    ├── services/       # サービス画像
    ├── products/       # 製品画像
    └── profile/        # プロフィール画像
```

---

## セットアップ手順

### 1. ファイルの配置

すべてのファイルを同じディレクトリに配置してください：
- `index.html`
- `style.css`
- `script.js`

### 2. 画像フォルダの作成

プロジェクトルートに `images` フォルダを作成し、以下のサブフォルダを作成してください：

```bash
mkdir images
mkdir images/hero
mkdir images/services
mkdir images/products
mkdir images/profile
```

### 3. 画像の準備

詳細は `IMAGE_GUIDE.md` を参照してください。

各セクションに必要な画像：
- **ヒーローセクション**: 背景画像（推奨サイズ: 1920×1080px）
- **サービス概要**: サービスイメージ画像（600×400px）
- **特徴セクション**: 各特徴の画像3枚（400×300px）
- **製品画像**: メイン画像1枚（500×500px）、サブ画像3枚（150×150px）
- **プロフィール**: 代表者の写真（300×300px）

### 4. ブラウザで開く

`index.html` をダブルクリックするか、ブラウザにドラッグ&ドロップして開いてください。

---

## 技術仕様

### 使用技術

- **HTML5**: セマンティックHTML、構造化データ対応
- **CSS3**: Flexbox、Grid、レスポンシブデザイン
- **JavaScript**: バニラJS（フレームワーク不使用）
- **フォント**: Google Fonts（Noto Sans JP、Montserrat）
- **アイコン**: Font Awesome 6.4.0

### 対応ブラウザ

- Chrome（最新版）
- Firefox（最新版）
- Safari（最新版）
- Edge（最新版）
- モバイルブラウザ対応

### レスポンシブブレイクポイント

- デスクトップ: 1200px以上
- タブレット: 768px〜1199px
- モバイル: 767px以下

---

## カラーパレット

```css
メインカラー（藍色）: #2E5090
サブカラー1（淡い青）: #A8BFDA
サブカラー2（白）: #FFFFFF
サブカラー3（オフホワイト）: #F5F7FA
アクセント1（淡い水色）: #E8F4F8
アクセント2（水色）: #B8E0F6
テキスト（濃紺）: #1A2332
テキスト（グレー）: #666666
```

---

## カスタマイズ方法

### 1. テキストの変更

`index.html` を開き、変更したいテキスト部分を直接編集してください。

### 2. 色の変更

`style.css` の最上部にあるCSS変数（`:root`セクション）を編集してください：

```css
:root {
    --main-color: #2E5090;  /* メインカラーを変更 */
    --accent-1: #D4AF37;    /* アクセントカラーを変更 */
    /* その他の色も同様に変更可能 */
}
```

### 3. フォントの変更

`style.css` のフォント設定を変更し、必要に応じて `index.html` の `<head>` 内のGoogle Fontsのリンクも変更してください。

### 4. 画像の差し替え

1. 新しい画像を `images/` フォルダの適切なサブフォルダに配置
2. `index.html` で該当する画像のパスを更新

例：
```html
<!-- 変更前（プレースホルダー） -->
<img src="https://placehold.co/600x400/2E5090/FFFFFF?text=Service+Image" alt="サービスイメージ">

<!-- 変更後（実際の画像） -->
<img src="images/services/service-01.jpg" alt="サービスイメージ">
```

---

## Googleマップの設定

`index.html` の地図セクションにある埋め込みコードを、実際の所在地のものに変更してください。

### 手順：

1. [Google Maps](https://www.google.com/maps) にアクセス
2. 住所「三重県津市片田井戸町228-1」を検索
3. 「共有」→「地図を埋め込む」を選択
4. 埋め込みコードをコピー
5. `index.html` の `<iframe>` タグを置き換え

---

## SEO最適化

### メタタグの編集

`index.html` の `<head>` セクションで、以下を編集してください：

```html
<meta name="description" content="ここに説明を記入">
<meta name="keywords" content="キーワード1,キーワード2,キーワード3">
<title>ページタイトル</title>
```

### OGP（Open Graph Protocol）の追加（推奨）

SNSでシェアされた際の表示を最適化するため、以下のタグを追加することをおすすめします：

```html
<meta property="og:title" content="てのひらオアシスH₂calm">
<meta property="og:description" content="水素美容×ヘッドリンパケアの出張サロン">
<meta property="og:image" content="https://yoursite.com/images/og-image.jpg">
<meta property="og:url" content="https://yoursite.com">
<meta property="og:type" content="website">
```

---

## デプロイ（公開）方法

### 方法1: レンタルサーバー

1. FTPソフト（FileZilla等）でサーバーに接続
2. すべてのファイルをアップロード
3. ドメインにアクセスして確認

### 方法2: Netlify（無料・推奨）

1. [Netlify](https://www.netlify.com/) にアカウント作成
2. プロジェクトフォルダをドラッグ&ドロップ
3. 自動的にデプロイされ、URLが発行される

### 方法3: GitHub Pages（無料）

1. GitHubにリポジトリを作成
2. ファイルをプッシュ
3. Settings → Pages でGitHub Pagesを有効化

---

## トラブルシューティング

### 画像が表示されない

- 画像ファイルのパスが正しいか確認
- 画像ファイル名の大文字・小文字を確認
- ブラウザのキャッシュをクリア

### スタイルが適用されない

- `style.css` が正しく読み込まれているか確認
- ブラウザの開発者ツールでエラーを確認
- CSSファイルのパスが正しいか確認

### JavaScriptが動作しない

- ブラウザのコンソールでエラーを確認
- `script.js` が正しく読み込まれているか確認
- JavaScriptが有効になっているか確認

### レスポンシブデザインが機能しない

- ブラウザの開発者ツールでモバイル表示を確認
- viewportメタタグが正しく設定されているか確認

---

## お問い合わせ先

ホームページの技術的な問題や質問がある場合：

**てのひらオアシスH₂calm**
- 電話: 090-1527-2302
- メール: tenohiraoasis@gmail.com
- 公式LINE: https://line.me/R/ti/p/@149ullwk

---

## ライセンス

このホームページは「てのひらオアシスH₂calm」専用に作成されたものです。

© 2025 てのひらオアシスH₂calm. All rights reserved.

---

## 更新履歴

### Version 1.0.0（2025年10月27日）
- 初回リリース
- 全6セクション実装
- レスポンシブデザイン対応
- SEO最適化実装
