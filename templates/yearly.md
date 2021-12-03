---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
# {{date:YYYY}}
<% tp.file.cursor(1) %>
## What happened last year?

## What's happening this year?

## Highlights

## Automated Highlights
```ad-note
title: Quarterly rollup
icon: laptop-code
collapse: true

```dataview
TASK FROM "zettelkasten" and #quarterly 
WHERE completed 
	AND meta(section).subpath = "Highlights"
	AND file.cday >= date(<%moment().startOf('year').format('YYYY-MM-DD')%>)
	AND file.cday <= date(<%moment().endOf('year').format('YYYY-MM-DD')%>)
```
---
Tags: #yearly
- Quarters: 
	- [[<%tp.date.now("YYYY-[Q1]")%>]] 
	- [[<%tp.date.now("YYYY-[Q2]")%>]] 
	- [[<%tp.date.now("YYYY-[Q3]")%>]] 
	- [[<%tp.date.now("YYYY-[Q4]")%>]] 
- Year:  self