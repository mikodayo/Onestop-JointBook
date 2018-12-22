# Re:VIEWテンプレート

## 概要説明
ワンストップ　合同誌を書こう

## この本の目的
合同誌はいいぞ。
会社やコミュニティで合同誌を作りたい、と思ったことありませんか？
考えたこともない？では、書きましょう。作りましょう。

合同誌とすることで、執筆の敷居を思いっきり低くすることができます。
以下に合同誌のメリットを述べます。

1.　みんなの知見を持ち寄って、一冊の本が作れる。
会社やコミュニティでやるということは、自分一人では書けない、広い内容をカバーする本が作れます。テーマを揃えるもよし、各著者が書きたいものを書くのもよし。どちらも素敵な本になります。
コミュニティの実績としても、十分でしょう・


2.　執筆のハードルが低い
一人で20ページなど書かないと本の体裁にならないんじゃないか？と尻込みするということはありませんか？薄い本といいつつ、薄すぎるのは…
懸念はわかります。特に、100P超えがボコボコある技術書界隈ではその懸念は十分わかります。ページ数が多いほうが偉いのではないですよ。出来上がった本はすべて偉大です。ですが、尻込みして出なかった本は、評価不可能ですよね？

では、10Pなら？→10Pならなんとかなるかなー。わかります。
では、10ページ書く人が3人いたら？　30ページの本ができますね。
30ページなら、同人誌としての厚みは十分でしょう。
100人いたら？100Pの本が生まれます。


デメリット
編集長は少し大変ですね。
著者、原稿集め、スケジュール管理、編集作業、印刷費は誰が持つ？など。

でも、合同誌だからできることもあります。もっとカジュアルに本をはやしませんか？
ということで、合同誌に特化した「ワンストップ合同誌を作ろう」の企画をスタートします。
合同誌のメリット、デメリット、原稿募集・告知、執筆ノウハウ、編集ノウハウ、打ち上げやお礼の方法、権利関係の扱い、実際に発行してみての感想など。権利関係は、最初に明確にしておくことをおすすめします。


こういったノウハウを集めた本を作りたいのです。


## 執筆・配布スケジュール

募集開始・環境構築　12月16日

章目次確定：1月末日

本文初稿：2月末

レビュー＆追記：3月15日

入稿:3月20日 発行　技術書典6(日程、募集開始はまだですが) を

大枠なスケジュールとします。(多少前後します)

## 著者紹介兼あとがき
Contributers.re内に、テンプレートに従って記入ください。

## 執筆にあたってのお願い
CIでコンパイルが通ることを確認してください。エラーのまま放置はなるべくやめてください。

Confrictが発生した場合は、解決お願いします。一応、PRで上げてもらえれば、定期的にチェックするようにしますが。

push -f等はやめましょう。（歴史を書き換えてはいけません。

相談事：
Issue立ててください。

雑談、ざっくばらんな相談については、Slackがあります。
参加方法は、親方まで。https://twitter.com/oyakata2438/
## Re:VIEWの書き方

[Re:VIEWチートシート](https://gist.github.com/erukiti/c4e3189dda179a0f0b73299fb5787838) を作ってみたので、参考にしてみてください。

## CI
https://app.wercker.com/oyakata2438/Onestop-meeting/runs
でPDFが書きだされます。（ちょっと後で更新します）
一番上のBuildをクリックすると展開されるので、
Output Artifactをクリックして、Download artifactをクリックすると、
tarで固めたpdfがダウンロードできます。

## インストール

細かい準備(TeX入れたり)は[『技術書をかこう！』](https://github.com/TechBooster/C89-FirstStepReVIEW-v2)に準じます。

### WindowsでReviewを使う方法

https://qiita.com/implicit_none/items/398c6e0bbedc8b160621
暗黙の型宣言さんが詳しく書いてくれてます。あるいは、技術同人誌を書こう‐アウトプットのススメ‐をご覧ください。

### Dockerを使う方法

Dockerを使うのが一番手軽です。

```sh
$ docker run --rm -v `pwd`:/work vvakame/review /bin/sh -c "cd /work/articles ; review-pdfmaker config.yml"
```

### Docker使わずビルド

```sh
cd articles ; review pdfmaker config.yml
```

### 権利

ベースには、[TechBooster/ReVIEW\-Template: TechBoosterで利用しているRe:VIEWのテンプレート（B5/A5/電子書籍）](https://github.com/TechBooster/ReVIEW-Template) を使っています。

  * 設定ファイル、テンプレートなど制作環境（techbooster-doujin.styなど）はMITライセンスです
    * 再配布などMITライセンスで定める範囲で権利者表記をおねがいします
