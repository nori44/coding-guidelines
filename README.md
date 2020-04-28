# 全般

### 対応ブラウザ
  - iOS safari
  - Android
  - Edge (windows10)
  - IE11
  - chrome
  - Firefox
  - safari

### インデント

スペース2個

### 文字コード 
 UTF-8

### 画像 
 - SP→デフォルト2倍サイズで書き出し
 - PC→そのままで書き出し

### コメントアウト
 - html : 各閉じタグの終わりに挿入する
 - CSS : 上部などに必要に応じて挿入する

<br>

# 命名規則

### 画像名

[種別]-[名前]\_[連番].[拡張子]

例 : `btn-submit_01.svg`

### CSS class名

BEM(MindBEMding)なども利用可能。以下の方法は一例

[ページ名/モジュール名]-[名前]\_[連番]<br>
[ページ名/モジュール名]-[名前]\_[状態]

例 : `header-gnav_01` <br>
例 : `header-btn_primary` <br>
例外 : 現在位置表示の`.current`などは単一で使って良い

<br>

# ディレクトリ名

画像ディレクトリ : `img`<br>
CSSディレクトリ : `css`<br>
JSディレクトリ : `js`<br>

ページごとのディレクトリは [ページ名] のディレクトリとし、`index.html` を入れる

<br>

# head内の基本形

```
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>ページのタイトル</title>
  <meta name="description" content="ページの内容を説明する文章">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="format-detection" content="telephone=no">
  <link rel="stylesheet" href="CSSファイルのパス">
  <script src="JavaScriptファイルのパス"></script>
</head>
```
<br>

# CSS

モバイルファーストとして記述する。<br>
SP表示のスタイルをまず記述し、PC表示をメディアクエリで記述する

CSSのセレクタ名はclassのみ使用<br>
※idセレクタを使う場合はJS用、ページ内リンク用のみ許可

子孫セレクタ：可能

例 ： `header .header-gnav a`

benderprefixは、ブラウザの主要バージョンで不要になっているのなら入れない

### CSSプロパティ、セレクタの書き方

```
img {
  max-width: 100%;
}
```
「セレクタ名」「半角スペース」「ブレース」<br>
「インデント」「プロパティ」「コロン」「半角スペース」「値」「セミコロン」<br>
「ブレース」<br>
とする<br>
最終行のプロパティの値のうしろにもセミコロンを付与する<br>
SCSSで圧縮する場合はこの限りではない

### リセットCSS

各章ごとに別のリセット系CSSを採用可能

<br>

# media queries

以下のブレークポイントから１〜2つほど利用する

 - 'sm-min': 'screen and (min-width: 576px)',
 - 'sm-max': 'screen and (max-width: 575px)',
 - 'md-min': 'screen and (min-width: 768px)',
 - 'md-max': 'screen and (max-width: 767px)',
 - 'lg-min': 'screen and (min-width: 992px)',
 - 'lg-max': 'screen and (max-width: 991px)',
 - 'xl-min': 'screen and (min-width: 1131px)',
 - 'xl-max': 'screen and (max-width: 1130px)',

Bootstrapのver4を参考にしています。

### media queries記述場所

SCSSを採用する章では、各スタイルの同じネスト内に記述

<br>

# SCSS

SASS構文ではなくSCSSで記述する

<br>

# JS
jQueryを利用可能
