---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
# {{date:gggg MMMM [Week] ww}}
<% tp.file.cursor(1) %>
## What happened last week?

## What's happening this week?

## Highlights
```dataview
TASK FROM "zettelkasten" and #daily
WHERE completed 
	AND meta(section).subpath = "Highlights"
	AND file.cday >= date({{monday:YYYY-MM-DD}})
	AND file.cday <= date({{friday:YYYY-MM-DD}})
```
---
Tags: #weekly
- Days
	- Monday [[{{monday:YYYY-MM-DD}}]]
	- Tuesday [[{{tuesday:YYYY-MM-DD}}]]
	- Wednesday [[{{wednesday:YYYY-MM-DD}}]]
	- Thursday [[{{thursday:YYYY-MM-DD}}]]
	- Friday [[{{friday:YYYY-MM-DD}}]]
- Week: self
- Month: [[<%tp.date.now("YYYY-MM")%>]] 
- Quarter: [[<%tp.date.now("YYYY-[Q]Q")%>]] 
- Year:  [[<%tp.date.now("YYYY")%>]] 