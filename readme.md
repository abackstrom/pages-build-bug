# pages-build-bug

Sample site showing that [benbalter/jekyll-readme-index](https://github.com/benbalter/jekyll-readme-index) `with_frontmatter` unexpectedly moves a nested readme into its parent directory.

<table>
<thead>
<tr>
<th>status</th>
<th>description</th>
<th>path</th>
<th>expected</th>
<th>actual</th>
</tr>
</thead>
<tbody>
<tr>
<td>Working</td>
<td>readme in subdir stays in subdir</td>
<td nowrap><code>a/readme.md</code></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/a/index.html">a/index.html</a></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/a/index.html">a/index.html</a></td>
</tr>
<tr>
<td>Broken</td>
<td>readme in nested subdir <code>c</code>, with no parent readme, moves into grandparent <code>b</code></td>
<td nowrap><code>b/c/readme.md</code></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/b/c/index.html">b/c/index.html</a></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/b/index.html">b/index.html</a></td>
</tr>
<tr>
<td>Working</td>
<td></td>
<td nowrap><code>d/readme.md</code><br><code>d/e/readme.md</code></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/d/index.html">d/index.html</a><br><a href="/abackstrom/pages-build-bug/blob/main/d/e/index.html">d/e/index.html</a></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/d/index.html">d/index.html</a><br><a href="/abackstrom/pages-build-bug/blob/main/d/e/index.html">d/e/index.html</a></td>
</tr>
<tr>
<td>Working</td>
<td></td>
<td nowrap><code>f/g/readme.md</code><br><code>f/h/readme.md</code></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/f/g/index.html">f/g/index.html</a><br><a href="/abackstrom/pages-build-bug/blob/main/f/h/index.html">f/h/index.html</a></td>
<td nowrap><a href="/abackstrom/pages-build-bug/blob/main/f/g/index.html">f/g/index.html</a><br><a href="/abackstrom/pages-build-bug/blob/main/f/h/index.html">f/h/index.html</a></td>
</tr>
</tbody>
</table>
