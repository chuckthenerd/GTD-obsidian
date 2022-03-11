# Projects

%% 
   Exclude the files:  Project, Projects
   and any file in the Archive path
   and any file in the Template path

   Include the #project and files with Project in their name
%%


## List of all active projects

``` dataview
TABLE file.tags,
dateformat(file.mtime,"yyyy-MM-dd HH:mm") as Edited, 
dateformat(file.ctime,"yyyy-MM-dd HH:mm") as Created, 
file.size as Size
FROM "" 
WHERE
(  contains(file.name, "Project") or contains(file.tags,"project") )
AND
(
    file.name != "Projects"
AND file.name != "Project"
AND !contains(file.path, "Archive")
AND !contains(file.path, "Templates")
)
SORT file.mtime desc
```

- [ ] List of all active projects and (next action OR next task which is not done)
- [ ] List of all active projects that don't have a next action
