---
creation date: 2021-11-29 21:06
modification date: Monday 29th November 2021 21:06:23
---
# TODO

*This list is compiled by retrieving tasks not yet completed from your #daily or #1on1 notes.*

## Daily
```dataviewjs
dv.taskList(dv.pages('"zettelkasten" and #daily')
	.sort(note => note.file.ctime, 'desc')
	.file.tasks.where(t => !t.completed));
```

## My 1 on 1 meetings
```ad-note
title: Confidential
icon: user-lock
collapse: true

```dataviewjs
dv.taskList(dv.pages('"zettelkasten" and (#1on1)')
	.sort(note => note.file.ctime, 'desc')
	.file.tasks.where(t => !t.completed));


```
