﻿## Liblouisで日本語を六点漢字と漢点字に変換するためのテーブルファイル

### 著作権について

日本語の漢字を表す点字は2種類の方式が考案されています。

長谷川貞夫氏による「六点漢字」と、川上泰一氏による「漢点字」です。

「六点漢字」はコンピュータで漢字を入力するために考えられたもので、「漢点字」は点字で漢字を読むために考えられたものです。

これらの漢字の点字に関する著作権はそれぞれの方に帰属します。

私がここに作成しているデータは個人的学習のためのものです。

利用する場合、それぞれの責任でお願いします。

### 各ファイルの説明

* ja-rokutenkanji.utb - 六点漢字に変換するためのファイル
* ja-kantenji.utb - 漢点字に変換するためのファイル

上記の２つがメインのファイルで、下記のファイルはこのメインのファイルから読み込むファイルになっています。

- ja-kanji-braille-shared.uti - 六点漢字、漢点字の両方で共通で読み込むファイル(全角のアルファベットと数字、句読点と記号、ひらがな、カタカナ)

カタカナを囲む符号は六点漢字と漢点字で異なるのですが、ファイルの修正をシンプルにするために、今は漢点字の符号に合わせています。

これら以外に、Liblouis付属の下記のファイルも読み込んでいます。

* unicode.dis - 変換結果をユニコード点字形式で出力するために必要
* en-us-brf.dis - unicode.disの代わりにこちらを読み込むとNABCCで出力できます
* en-ueb-g1.ctb - このファイルから以下のファイルが読み込まれています
* braille-patterns.cti
* en-ueb-chardefs.uti
* en-ueb-math.ctb
* latinLetterDef8Dots.uti

### Liblouis付属のlou_translateでの使い方

Liblouisに含まれるlou_translateを使う場合、コマンドプロンプトで:

> lou_translate -f ja-rokutenkanji.utb <input.txt >output.txt

のようにします。

ja-rokutenkanji.utbは六点漢字に変換するためのファイルです。

input.txtは変換したいテキストファイルで、文字コードがutf8のものです。

output.txtは出力ファイル名です。

ja-rokutenkanji.utbの代わりに、ja-kantenji.utbを指定すると漢点字に変換できます。





