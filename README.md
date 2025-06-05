# local-LaTeX
```
docker pull texlive/texlive:latest
```

```
docker run --rm \
  -v "$(pwd)":/doc \
  -w /doc \
  texlive/texlive:latest \
  pdflatex -file-line-error -interaction=nonstopmode -synctex=1 \
  -output-format=pdf \
  -output-directory=/doc/out \
  <filename>.tex

```

supress logs
```
docker run --rm \
  -v "$(pwd)":/doc \
  -w /doc \
  texlive/texlive:latest \
  pdflatex -file-line-error -interaction=nonstopmode -synctex=1 \
  -output-format=pdf \
  -output-directory=/doc/out \
  <filename>.tex > /dev/null
```


install skim for mac
