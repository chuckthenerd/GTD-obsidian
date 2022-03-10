# Projects

- [ ] Generate a list of all Projects here

%% Exclude this file and path (Templates or Archive)
removing column ", file.size as Size "
%%

``` dataview
TABLE file.mtime as Edited, file.ctime as Created
FROM ""
WHERE contains(file.name, "Project")
AND  file.name != "Projects"
AND  file.name != "Project"
AND !contains(file.name, "(ARCHIVE)")
AND !contains(file.path, "Templates")
AND !contains(file.path, "Archive")
SORT file.mtime desc
```