# md2tex
このリポジトリは、markdownで書いた文書をTeXに変換し、物理部の部誌などに使えるようにするためのものです。
This repo is to convert documents written in markdown(.md) to TeX files(.tex) for KPC archives.

## 注意点
TeXファイルへの変換にはpandocという拡張機能をVS Codeからインストールする必要があります。

## How to convert the files
まずはmarkdownで文書を作り、次のスクリプトを実行しましょう。
First of all you need to create a markdown file and then run the following script:
```sh
pandoc (markdownで書いた文書のファイル名).md -f gfm -t latex --filter "pandoc.py" -o (変換後のTeXファイル名).tex
```

何もコンソールに出力されなければおそらく成功です。生成されたTeXファイルを```\input{ファイル名.tex}```などとして挿入すれば、書きにくい部分のみTeXで作っておいて、本文は楽にmarkdownで書くことができます。
If there is no response in the terminal, it is probably successful.


