## List of all tags in use and where
Credit goes out to user [mnvwvnm](https://forum.obsidian.md/u/mnvwvnm) on 2021-09-12 in [this forum](https://forum.obsidian.md/t/creating-a-tag-index-table-with-dataview/23997/10)

This provides a dynamic view that relates tags to a file.  The file entries (are/are not/can be) duplicated in this table.

```dataview 
TABLE 
WITHOUT ID (tag + "(" + length(rows.file.link) + ")") AS Tags, link(sort(rows.file.name)) AS Files 
FROM "" WHERE file.tags FLATTEN file.tags AS tag 
GROUP BY tag SORT length(rows.file.link) DESC 
```