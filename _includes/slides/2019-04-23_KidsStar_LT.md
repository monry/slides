class: center, middle

# キッズスター学習帳を<br />支えた技術

## 2019/04/23 KidsStar LT 大会

### 森　哲哉

---

# .center[Agenda]

* はじめに
* 技術書典について
* キッズスター学習帳について
* Re:VIEW について

---

# .center[Agenda]

* .bold[はじめに]
* .disable[技術書典について]
* .disable[キッズスター学習帳について]
* .disable[Re:VIEW について]

---

# .center[はじめに]

本 LT では「**キッズスター学習帳**」を<br />「**技術書典6**」にて頒布した際に<br />用いた技術について、プログラマーの観点からご紹介します。

---

# .center[Agenda]

* .disable[はじめに]
* .bold[技術書典について]
* .disable[キッズスター学習帳について]
* .disable[Re:VIEW について]

---

# .center[技術書典について]

![技術書典6](assets/image/2019-04-23-00-36-03.png)

---

# .center[技術書典について]

<blockquote class="center" style="margin-top: 5em;">.content[新しい技術に出会えるお祭りです。<br /><span style="letter-spacing: -0.1em;">技術書典は、いろんな技術の普及を手伝いたいとの想いではじまりました。</span><br />技術書を中心として出展者はノウハウを詰め込み、<br />来場者はこの場にしかないおもしろい技術書をさがし求める、<br />技術に関わる人のための場として『技術書典』を開催します。]</blockquote>

---

# .center[技術書典について]

## 概要

* 年2回開催される**技術同人誌即売会**
* 参加サークル数: **300サークル**以上
* 来場者数: **10,000人**以上

---

# .center[Agenda]

* .disable[はじめに]
* .disable[技術書典について]
* .bold[キッズスター学習帳について]
* .disable[Re:VIEW について]

---

# .center[<span style="margin: 0 -2em; letter-spacing: -0.05em;">キッズスター学習帳について</span>]

<span class="center" style="margin-top: -0.5em;"><img src="assets/image/2019-04-23-01-29-19.png" alt="キッズスター学習帳" width="45%" /></span>

---

# .center[<span style="margin: 0 -2em; letter-spacing: -0.05em;">キッズスター学習帳について</span>]

## 概要

* キッズスター関係者**6名による共著**
* **技術書典6**にて頒布
* [BOOTH](https://kidsstar-tbf.booth.pm/) でも取り扱い
    * 電子・冊子ともに**¥1,000-**
* 本日時点で**約150冊**販売

---

count: false

# .center[<span style="margin: 0 -2em; letter-spacing: -0.05em;">キッズスター学習帳について</span>]

## 概要

* キッズスター関係者.highlight[**6名による共著**]
* **技術書典6**にて頒布
* [BOOTH](https://kidsstar-tbf.booth.pm/) でも取り扱い
    * 電子・冊子ともに**¥1,000-**
* 本日時点で**約150冊**販売

---

# .center[<span style="margin: 0 -2em; letter-spacing: -0.05em;">キッズスター学習帳について</span>]

## 要件

* 印刷会社に発注するために**組版**必須
* 執筆中に仕上がりを**確認**したい
* 極力手間を掛けたくない

---

class: middle, center

# どうする？

---

class: middle, center

# Re:VIEW

---

# .center[Agenda]

* .disable[はじめに]
* .disable[技術書典について]
* .disable[キッズスター学習帳について]
* .bold[Re:VIEW について]

---

# .center[Re:VIEW について]

![Re:VIEW](assets/image/2019-04-23-00-16-06.png)

---

# .center[Re:VIEW について]

<blockquote style="margin-top: 5em;">.content[Re:VIEW（リビュー）は、軽量マークアップ言語のひとつである。<br />Re:VIEW形式のマークアップを付けたコンテンツを、HTML、LATEX、XML、EPUB、プレーンテキスト等に変換できる。]</blockquote>
<span class="right">出展: [Wikipedia](https://ja.wikipedia.org/wiki/Re:VIEW)</span>

---

# .center[Re:VIEW について]

## 概要

* オープンソース（LGPL）
* **Markdown** っぽい文法
* LaTeX による組版
* 独自拡張可能

---

# .center[Re:VIEW について]

## インストール

* RubyGems 経由
* ソースコードからビルド
* Docker 経由

---

count: false

# .center[Re:VIEW について]

## インストール（KidsStar の場合）

* .disable[RubyGems 経由]
* .disable[ソースコードからビルド]
* .highlight.bold[Docker 経由]

---

count: false

# .center[Re:VIEW について]

## インストール（KidsStar の場合）

* .disable[RubyGems 経由]
* .disable[ソースコードからビルド]
* .highlight.bold[Docker 経由]
    * DockerHub: [`vvakame/review`](https://hub.docker.com/r/vvakame/review)

---

# .center[Re:VIEW について]

## 使い方（KidsStar の場合）

1. 原稿を書く<small> (拡張子: `.re`)</small>
--
count: false
1. 設定ファイル <small>`config.yml`</small> を用意
--
count: false
1. カタログファイル <small>`catalog.yml`</small> を用意
--
count: false
1. `review-pdfmaker` コマンドを実行

```bash
$ review-pdfmaker ./config.yml
```

---

class: middle, center

# ね？簡単でしょう？

---

# .center[Re:VIEW について]

## 確認（KidsStar の場合）

1. `docker-compose` コマンドを実行
    * Docker 関連の設定済

```bash
$ docker-compose run --em ebook # 電子書籍用カラー原稿
$ docker-compose run --em binding # 印刷用モノクロ原稿
```

---

class: middle, center

# ね？簡単でしょう？

---

# .center[Re:VIEW について]

## その他

* TextLint で「てにをは」チェック
* CircleCI で自動ビルド
    * <span class="disable">間に合わず</span>
* 非 Re:VIEW 原稿のマージ
    * <span class="disable">間に合わず</span>

---

# .center[Re:VIEW について]

## ぶっちゃけた話

* UNIBOOK 執筆時の仕組みを<br />丸パクリしてます
    * Special Thanks: Keigo Ando (UTJ)
* Re:VIEW よりも GitHub / CircleCI / Docker あたりの知識が重要

---

class: middle, center

# Let's write a Book !

---

class: middle, center

# One more thing...

---

# One more thing...

このスライドは [**GitHub Pages**](https://pages.github.com/) 上で<br />[**Jekyll**](https://jekyllrb.com/) を用いて Markdown より<br />生成されており、スライドとしての<br />機能は [**Remark.js**](https://github.com/gnab/remark) を用いて<br />実現しています。<br />
<small class="disable"><small>環境作るのが楽しくてスライドそのものの<br />進捗がヤバかったのは内緒です。</small></small>

---

class: center, middle

# Thank you for <br />your attention !!