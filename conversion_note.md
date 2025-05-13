# mdからhtmlへの変換
pandoc -f markdown -t html "README.md" > "index.html" --include-before-body=head.html