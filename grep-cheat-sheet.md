# Grep Cheat Sheet
Grep stand for
**G**lobal
**R**egular **E**xpression
**P**rint

## Search with grep
```grep -rnw '.' -e "your_search_string"```

## Search but exclude files
```grep --exclude="fileName.fileExtension" -rnw -e "search for this string in files"```


