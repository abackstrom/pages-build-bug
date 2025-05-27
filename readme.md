# pages-build-bug

| status | path | expected | actual |
| --- | --- | --- | --- |
| Working | a/readme.md | a/index.html | a/index.html |
| Broken | b/c/readme.md | b/c/index.html | b/index.html |
| Working | d/readme.md<br>d/e/readme.md | d/index.html<br>d/e/index.html | d/index.html<br>d/e/index.html |
