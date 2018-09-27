# 納品時のコードチェック

[フロントエンドチェックリスト](https://github.com/miya0001/Front-End-Checklist)を参考に各項目をチェックしていく。


## チェックリスト (2018/09/18 現時点)
**前提として、simple-pageテンプレートを利用しているものとします。**
* テンプレートに用意されている内容についてのチェック項目は割愛します。
* それ以外に必要がないと判断した項目も載せていません。

### Head
* [ ] Canonical: Medium 重複したコンテンツを避けるために rel="canonical" を使用している。

* [ ] エラーページ: 404 及び 5xx 用のエラーページが存在している。5xx エラーページは CSS が内蔵されている必要があることを覚えておくこと。（サーバーに対する追加のリクエストを行わないこと。）


### HTML
* [ ] Noopener: target="_blank" で外部リンクを使用する際には、rel="noopener" 属性をつけて Tabnabbing 脆弱性を防ぐこと。

* [ ] 不必要なコード: 不必要なコードは、本番環境にアップロードされる前に削除されていること。

* [ ] W3C 準拠: すべてのページを HTML バリデーターでテストして、問題点を抽出する。
🛠 [W3C validator](https://validator.w3.org/)

* [ ] HTML Lint: ツールを使って HTML に問題があるかどうかを分析する。
🛠 [Dirty markup](https://www.10bestdesign.com/dirtymarkup/)
🛠 [Sonar a linting tool for the web](https://webhint.io/scanner/)

* [ ] リンクチェッカー: リンク切れがなく、404 エラーが発生しないことを確認する。
🛠 [W3C Link Checker](https://validator.w3.org/checklink)


### Webフォント
* [ ] ウェブフォントのフォーマット: WOFF, WOFF2 及び TTF はすべてのモダンブラウザでサポートされている。

* [ ] ウェブフォントのサイズ: ウェブフォントのサイズは、すべての綴りが含まれた状態で 2MB を超えないこと。

* [ ] ウェブフォントローダー: 必要があれば、ウェブフォントローダーで、ロード時の挙動を制御する。
🛠 [Typekit Web Font Loader](https://github.com/typekit/webfontloader)


### CSS
* [ ] Responsive Web Design: そのウェブサイトはレスポンシブデザインを採用している。

* [ ] Unique ID: もし ID が使用されているなら、そのページの中でユニークであること。

* [ ] Reset CSS: CSS のリセット (reset, normalize または reboot) が使用されており最新である。

* [ ] JS prefix: すべての class (または JavaScript で使用されいる ID) は、js- で始まっており、それらは CSS で使用されていない。

* [ ] 内部 CSS 及びインラインスタイル: <style> による内部 CSS やインラインスタイルを使用することを避け、正当な理由でのみ使用する。

* [ ] ベンダープレフィックス: CSS ベンダープレフィックスが、ブラウザの互換性に基づいて生成され、使用されている。

* [ ] 圧縮（Minify）: すべての CSS ファイルは圧縮されている。

* [ ] Unused CSS: 使用していない CSS は削除されていること。
🛠 [UnCSS Online](https://uncss-online.com/)
🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)

* [ ] 文法: High すべての CSS 及び SCSS にはエラーがないこと。CSSLintで開発中に常にチェックしておく。

* [ ] レスポンシブデザイン: すべてのページは、320px, 768px, 1024px のブレイクポイントでテストされていること。（可能であれば、アナリティクスの結果に基づいて他のブレイクポイントでもテストする。）

* [ ] CSS バリデーター: CSS がテストされ、関連するエラーが修正されていること。
🛠 [CSS Validator](https://jigsaw.w3.org/css-validator/)

* [ ] デスクトップブラウザ: すべてのページは現在あるすべてのデスクトップブラウザでテストされている。 (Safari, Firefox, Chrome, Internet Explorer(10,11), EDGE)

* [ ] モバイルブラウザ: すべてのページは現在あるすべてのモバイルブラウザでテストされている。 (Chrome, Safari...)

* [ ] OS: すべてのページは各 OS でテストされている。 (Windows, Android, iOS, Mac...)

* [ ] ピクセルパーフェクト: すべてのページはピクセルパーフェクトに近い状態であること。クリエイティブの品質によっては 100% 正確ではない場合があるが、テンプレートにほぼ近い状態である必要がある。


### 画像
* [ ] Optimization: すべての画像はブラウザでの表示に対して最適化されていること。WebP フォーマットは、ホームページのような重要なページでも使用することができます。

* [ ] Width and Height: 最終的に表示される際のサイズがわかっている場合、すべての <img> は、height と width が指定されている。（px または % を指定しない。）

* [ ] Alt テキスト: すべての <img> は Alt テキストが代替テキストとして指定されていること。なおアイコンのimgタグであったりは`alt=""`でよいものとする。


（[WIP]: 今後追加予定のチェックリスト）
### JavaScript


### セキュリティ


### パフォーマンス


### アクセシビリティ


### SEO


