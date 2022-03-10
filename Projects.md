# Projects

- [ ] Generate a list of all ACTIVE Projects here

%% Exclude this file and path (Templates or Archive)
removing column ", file.size as Size "
%%

## List of all active projects

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

- [ ] List of all active projects and (next action OR next task which is not done)
- [ ] List of all active projects that don't have a next action