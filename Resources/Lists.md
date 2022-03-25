# Lists

- [ ] Point to other [[Lists]] that needs to be addressed.  Calendar, Someday-Maybe,  Agendas, checklists

[[Lists]] that needs to be addressed:
In
Next actions
Waiting for
Projects
Someday-Maybe  
Calendar 
Agendas 
checklists
[[Scratchpad]]
Checklist Template - Packing for vacation

## In
capture ideas and tasks as they occur to you.  A [[Scratchpad]].  The barrier for adding something to this list shold be minimal.  Capture your open loops.  Dump the contents of your brain in here.

```dataview
TABLE file.tags,
dateformat(file.mtime,"yyyy-MM-dd HH:mm") as Edited, 
dateformat(file.ctime,"yyyy-MM-dd HH:mm") as Created, 
file.size as Size
FROM [[Lists]]
SORT file.mtime desc
```