# simple-page

npm-scriptsを使った静的ページ(HTML5/CSS3)のミニマム開発環境


## 環境構築
* npm/yarn
  * browser-sync
  * node-sass
  * nodemon
  * rimraf


## 開発手順
```
yarn install
yarn run build:scss:watch
yarn run serve
  open http://localhost:3000
```


## SCSSのフォルダ構成
1. _colors.scssにそれぞれ使う色を設定する
2. _settings.scssにそれぞれ使う変数値を設定する
3. 各sectionごとにcomponentsで分けてCSS設計を行う
4. layoutの中のCSSは全体共通のものに対して責任を持つ
5. section関係なく共通で使う項目は_utilities.scssに入れる
6. 文字のレイアウトに関する共通CSSは_typography.scssに入れる


## 各種言語
* HTML5
* CSS3
  * SCSS
  * BEM
