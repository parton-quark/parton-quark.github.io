# mdからhtmlへの変換
* pandoc
  * pandoc -f markdown -t html "README.md" > "index.html"
  * pandoc -f markdown -t html -c ./example.css ./README.md > ./README.html
* style.htmlからスタイル持ってくる
* google analyticsをheadの前に挿入
