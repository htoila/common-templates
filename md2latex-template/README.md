# Markdown to Latex
> https://blog.davidz.cn/write-latex-report-with-markdown/
Using pandoc
[template](https://github.com/Wandmalfarbe/pandoc-latex-template)

### examples
```bash
pandoc.exe .\README.md -o 1.pdf --from markdown --template eisvogel --listings
```
markdown 开头存有YAML Front Matter，用于进行配置
```bash
pandoc Report.md `
-o Report.pdf `
--standalone `
--listings `
--number-sections `
--filter pandoc-crossref `
--filter=pandoc-citeproc `
--pdf-engine=xelatex `
--template eisvogel
```

- -o 指定输出文件
- --standalone 独立完整文件
- --listings 使用listings高亮代码
- --number-sections 启用段落编号
- --filter pandoc-crossref 使用过滤器 pandoc-crossref
- --filter pandoc-citeproc 使用过滤器 pandoc-citeproc
- --pdf-engine=xelatex 指定 PDF 的 engine 为 xelatex
- --template eisvogel 指定模板为 eisvogel
