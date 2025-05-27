# pages-build-bug

Sample site showing that [benbalter/jekyll-readme-index](https://github.com/benbalter/jekyll-readme-index) `with_frontmatter` unexpectedly moves a nested readme into its parent directory.

[abackstrom/pages-build-bug/](https://github.com/abackstrom/pages-build-bug/)

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
<td>readme in directory stays there</td>
<td nowrap>a/readme.md</td>
<td nowrap><a href="a/index.html">a/index.html</a></td>
<td nowrap><a href="a/index.html">a/index.html</a></td>
</tr>
<tr>
<td>Broken</td>
<td>readme in subdir moves into empty parent dir</td>
<td nowrap>b/c/readme.md</td>
<td nowrap><a href="b/c/index.html">b/c/index.html</a></td>
<td nowrap><a href="b/index.html">b/index.html</a></td>
</tr>
<tr>
<td>Working</td>
<td>subdir readme will not clobber parent readme</td>
<td nowrap>d/readme.md<br>d/e/readme.md</td>
<td nowrap><a href="d/index.html">d/index.html</a><br><a href="d/e/index.html">d/e/index.html</a></td>
<td nowrap><a href="d/index.html">d/index.html</a><br><a href="d/e/index.html">d/e/index.html</a></td>
</tr>
<tr>
<td>Broken</td>
<td>one subdir readme moves into parent</td>
<td nowrap>f/g/readme.md<br>f/h/readme.md</td>
<td nowrap><a href="f/g/index.html">f/g/index.html</a><br><a href="f/h/index.html">f/h/index.html</a></td>
<td nowrap><a href="f/index.html">f/index.html</a><br><a href="f/h/index.html">f/h/index.html</a></td>
</tr>
</tbody>
</table>


