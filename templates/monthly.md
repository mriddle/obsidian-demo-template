---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
# {{date:YYYY MMMM}}
<% tp.file.cursor(1) %>
## What happened last month?

## What's happening this month?

## Highlights

## Automated Highlights
```ad-note
title: Weekly rollup
icon: laptop-code
collapse: true

```dataview
TASK FROM "zettelkasten" and #weekly
WHERE completed 
	AND meta(section).subpath = "Highlights"
	AND file.cday >= date(<%moment().day('monday').week(moment().startOf('month').format('ww')).format('YYYY-MM-DD')%>)
	AND file.cday <= date(<%moment().endOf('month').format('YYYY-MM-DD')%>)
```
---
Tags: #monthly
- Weeks:
	- [[<%moment().startOf('month').format('YYYY-[W]ww')%>]] 
	- [[<%tp.date.now("YYYY-[W]ww", 7)%>]] 
	- [[<%tp.date.now("YYYY-[W]ww", 14)%>]] 
	- [[<%tp.date.now("YYYY-[W]ww", 21)%>]]
	- [[<%tp.date.now("YYYY-[W]ww", 28)%>]]
- Month: self
- Quarter: [[<%tp.date.now("YYYY-[Q]Q")%>]] 
- Year:  [[<%tp.date.now("YYYY")%>]] 
