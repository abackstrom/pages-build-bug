# pages-build-bug

Sample site showing that [benbalter/jekyll-readme-index](https://github.com/benbalter/jekyll-readme-index) `with_frontmatter` unexpectedly moves a nested readme into its parent directory.

| status | path | expected | actual |
| --- | --- | --- | --- |
| Working | `a/readme.md` | [a/index.html](a/index.html) | [a/index.html](a/index.html) |
| Broken | `b/c/readme.md` | [b/c/index.html](b/c/index.html) | [b/index.html](b/index.html) |
| Working | `d/readme.md`<br>`d/e/readme.md` | [d/index.html](d/index.html)<br>[d/e/index.html](d/e/index.html) | [d/index.html](d/index.html)<br>[d/e/index.html](d/e/index.html) |
| Working | `f/g/readme.md`<br>`f/h/readme.md` | [f/g/index.html](f/g/index.html)<br>[f/h/index.html](f/h/index.html) | [f/g/index.html](f/g/index.html)<br>[f/h/index.html](f/h/index.html) |
