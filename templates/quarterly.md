---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
# {{date:YYYY [Q]Q}}
<% tp.file.cursor(1) %>
## What happened last quarter?

## What's happening this quarter?

## Highlights

## Automated Highlights
```ad-note
title: Monthly rollup
icon: laptop-code
collapse: true

```dataview
TASK FROM "zettelkasten" and #monthly
WHERE completed 
	AND meta(section).subpath = "Highlights"
	AND file.cday >= date(<%moment().startOf('quarter').format("YYYY-MM")%>)
	AND file.cday <= date(<%moment().startOf('quarter').add(2, "M").format("YYYY-MM")%>)
```
---
Tags: #quarterly
- Months: 
	- [[<%moment().startOf('quarter').format("YYYY-MM")%>]] 
	- [[<%moment().startOf('quarter').add(1, "M").format("YYYY-MM")%>]] 
	- [[<%moment().startOf('quarter').add(2, "M").format("YYYY-MM")%>]] 
- Quarter: self
- Year:  [[<%tp.date.now("YYYY")%>]] 