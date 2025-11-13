# mdからhtmlへの変換
pandoc -f markdown -t html "README.md" > "index.html" --include-before-body=head.html
<!-- pandoc news.md -f markdown -t html5 -o news.html -->
pandoc news.md \
  -f markdown -t html5 \
  -s \
  --include-in-header=news_head.html \
  -o news.html