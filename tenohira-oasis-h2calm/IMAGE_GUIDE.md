# 画像配置ガイド

このガイドでは、ホームページで使用する画像の配置方法と推奨サイズについて説明します。

---

## フォルダ構成

まず、以下のフォルダ構造を作成してください：

```
images/
├── hero/           # ヒーローセクション用
├── services/       # サービス画像
├── effects/        # 効果セクション用
├── products/       # 製品画像
└── profile/        # プロフィール画像
```

---

## 必要な画像一覧

### 1. ヒーローセクション

**ファイル名**: `hero-bg.jpg` または `hero-bg.webp`
**配置先**: `images/hero/`
**推奨サイズ**: 1920×1080px（16:9）
**ファイル形式**: JPG、WebP
**容量**: 500KB以下（最適化推奨）

**画像内容**:
- 癒しの雰囲気を感じさせる画像
- 水素や水をイメージさせる透明感のある画像
- リラックスしている女性の画像
- 藍色や青系の色調が映える画像

**HTMLでの変更箇所**（index.html 66行目付近）:
```html
<!-- 現在（プレースホルダー） -->
<section id="home" class="hero">

<!-- 変更後（背景画像を追加） -->
<section id="home" class="hero" style="background-image: url('images/hero/hero-bg.jpg');">
```

または、CSSで変更（style.css 338行目付近）:
```css
.hero {
    background: linear-gradient(rgba(46, 80, 144, 0.7), rgba(30, 58, 110, 0.7)),
                url('../images/hero/hero-bg.jpg');
    background-size: cover;
    background-position: center;
}
```

---

### 2. サービス概要セクション

**ファイル名**: `service-overview.jpg`
**配置先**: `images/services/`
**推奨サイズ**: 600×400px（3:2）
**ファイル形式**: JPG、WebP

**画像内容**:
- 水素吸入器を使用している様子
- ヘッドリンパケアの施術風景
- リラックスしている様子

**HTMLでの変更箇所**（index.html 137行目付近）:
```html
<!-- 変更前 -->
<img src="https://placehold.co/600x400/2E5090/FFFFFF?text=Service+Image" alt="サービスイメージ">

<!-- 変更後 -->
<img src="images/services/service-overview.jpg" alt="サービスイメージ" loading="lazy">
```

---

### 3. 特徴セクション（3枚必要）

#### 3-1. 水素美容の効果

**ファイル名**: `feature-hydrogen.jpg`
**配置先**: `images/services/`
**推奨サイズ**: 400×300px（4:3）
**画像内容**: 水素吸入器、水素のイメージ、美容効果

**HTMLでの変更箇所**（index.html 172行目付近）:
```html
<img src="images/services/feature-hydrogen.jpg" alt="水素美容" loading="lazy">
```

#### 3-2. ヘッドリンパケアの効果

**ファイル名**: `feature-head-lymph.jpg`
**配置先**: `images/services/`
**推奨サイズ**: 400×300px（4:3）
**画像内容**: ヘッドマッサージの様子、リラックスしている女性

**HTMLでの変更箇所**（index.html 187行目付近）:
```html
<img src="images/services/feature-head-lymph.jpg" alt="ヘッドリンパケア" loading="lazy">
```

#### 3-3. 出張サービスの便利さ

**ファイル名**: `feature-mobile-service.jpg`
**配置先**: `images/services/`
**推奨サイズ**: 400×300px（4:3）
**画像内容**: 自宅でリラックスしている様子、出張のイメージ

**HTMLでの変更箇所**（index.html 202行目付近）:
```html
<img src="images/services/feature-mobile-service.jpg" alt="出張サービス" loading="lazy">
```

---

### 4. 製品画像（アクアリエッタ）

#### 4-1. メイン画像

**ファイル名**: `aquarietta-main.jpg`
**配置先**: `images/products/`
**推奨サイズ**: 500×500px（1:1）
**画像内容**: アクアリエッタ AQY-300EX 正面画像

**HTMLでの変更箇所**（index.html 443行目付近）:
```html
<img src="images/products/aquarietta-main.jpg" alt="アクアリエッタ AQY-300EX" loading="lazy">
```

#### 4-2. サブ画像（3枚）

**ファイル名**:
- `aquarietta-sub1.jpg`（側面）
- `aquarietta-sub2.jpg`（使用イメージ）
- `aquarietta-sub3.jpg`（パーツ・付属品）

**配置先**: `images/products/`
**推奨サイズ**: 150×150px（1:1）

**HTMLでの変更箇所**（index.html 448行目付近）:
```html
<div class="product-sub-images">
    <img src="images/products/aquarietta-sub1.jpg" alt="製品画像2" loading="lazy">
    <img src="images/products/aquarietta-sub2.jpg" alt="製品画像3" loading="lazy">
    <img src="images/products/aquarietta-sub3.jpg" alt="製品画像4" loading="lazy">
</div>
```

---

### 5. プロフィール画像

**ファイル名**: `profile-gucchi.jpg`
**配置先**: `images/profile/`
**推奨サイズ**: 300×300px（1:1）または400×400px
**画像内容**: 代表者・坂口智さんの写真（プロフェッショナルな雰囲気）

**HTMLでの変更箇所**（index.html 551行目付近）:
```html
<img src="images/profile/profile-gucchi.jpg" alt="代表 坂口智" loading="lazy">
```

---

## 画像の最適化

### 推奨ツール

1. **TinyPNG** (https://tinypng.com/)
   - JPGとPNGを圧縮
   - 画質を保ちながらファイルサイズを削減

2. **Squoosh** (https://squoosh.app/)
   - Googleが提供する画像最適化ツール
   - WebP形式への変換が可能

3. **ImageOptim**（Mac用）
   - ドラッグ&ドロップで簡単に最適化

### WebP形式の使用（推奨）

WebP形式を使用すると、画質を保ちながらファイルサイズを大幅に削減できます。

**HTMLでの記述例**:
```html
<picture>
    <source srcset="images/hero/hero-bg.webp" type="image/webp">
    <img src="images/hero/hero-bg.jpg" alt="ヒーロー画像">
</picture>
```

---

## ファイル命名規則

- **小文字を使用**: `hero-bg.jpg` ✓、`Hero-BG.jpg` ✗
- **ハイフンで単語を区切る**: `service-overview.jpg` ✓、`service_overview.jpg` ✗
- **日本語を使わない**: `service.jpg` ✓、`サービス.jpg` ✗
- **スペースを使わない**: `hero-bg.jpg` ✓、`hero bg.jpg` ✗

---

## 画像の準備ができていない場合

プレースホルダー画像のままでも、ホームページは正常に動作します。

### プレースホルダーサービス

- **Lorem Picsum**: https://picsum.photos/
- **Unsplash Source**: https://source.unsplash.com/
- **Placehold.co**: https://placehold.co/（現在使用中）

### フリー素材サイト

実際の画像を準備する際に使えるサイト：

1. **写真AC**: https://www.photo-ac.com/
2. **Unsplash**: https://unsplash.com/
3. **Pexels**: https://www.pexels.com/
4. **Pixabay**: https://pixabay.com/

---

## 画像の差し替え手順

### 手順1: 画像を準備

1. 上記の推奨サイズに合わせて画像を準備
2. 必要に応じて画像を圧縮・最適化
3. 適切なファイル名を付ける

### 手順2: 画像を配置

1. `images/` フォルダ内の適切なサブフォルダに画像を配置
2. ファイル名が正しいか確認

### 手順3: HTMLを編集

1. `index.html` を開く
2. 該当する箇所のURLを変更
3. `src="https://placehold.co/..."` → `src="images/xxx/yyy.jpg"`

### 手順4: 確認

1. ブラウザでページを開く（F5でリロード）
2. 画像が正しく表示されているか確認
3. モバイル表示も確認（開発者ツールで）

---

## トラブルシューティング

### 画像が表示されない

**原因1**: パスが間違っている
```html
<!-- 誤り -->
<img src="image/service.jpg">

<!-- 正しい -->
<img src="images/services/service.jpg">
```

**原因2**: ファイル名の大文字・小文字が違う
```html
<!-- ファイル名が Service.jpg の場合 -->
<img src="images/services/service.jpg">  <!-- ✗ 表示されない -->
<img src="images/services/Service.jpg">  <!-- ✓ 表示される -->
```

**原因3**: ファイルが存在しない
- フォルダに画像が正しく配置されているか確認

### 画像の読み込みが遅い

- 画像のファイルサイズを確認（目安: 500KB以下）
- 画像圧縮ツールで最適化
- WebP形式への変換を検討

### 画像の縦横比がおかしい

- CSSで `object-fit: cover;` を使用（すでに設定済み）
- 推奨サイズに合わせて画像を準備

---

## チェックリスト

画像の準備が完了したら、以下をチェックしてください：

- [ ] すべての画像ファイルを準備した
- [ ] 画像を最適化（圧縮）した
- [ ] 適切なファイル名を付けた
- [ ] `images/` フォルダ内に正しく配置した
- [ ] `index.html` のパスを変更した
- [ ] ブラウザで表示を確認した
- [ ] モバイル表示も確認した
- [ ] すべての画像が正しく表示されている

---

## 追加の画像

必要に応じて、以下のセクションにも画像を追加できます：

### 効果セクション
- 水素吸入の効果を説明する画像
- ヘッドリンパケアの効果を説明する画像

### お客様の声（今後追加する場合）
- お客様の写真（許可を得た場合のみ）
- ビフォーアフター画像

### ギャラリー（今後追加する場合）
- サロンの雰囲気
- 施術の様子
- 使用する機器

---

## お問い合わせ

画像の準備や配置に関してご不明な点がございましたら、お気軽にお問い合わせください。

**てのひらオアシスH₂calm**
- 電話: 090-1527-2302
- メール: tenohiraoasis@gmail.com

---

**最終更新**: 2025年10月27日
