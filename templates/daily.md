---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
<% await tp.file.rename(tp.date.now()) %>
# <% tp.file.creation_date("dddd Do MMMM YYYY") %>
## Today
- Review [[TODO]] items

## Tomorrow

## Done

## Events

```dataview
TABLE summary AS "Summary" FROM #event and "zettelkasten" WHERE file.cday = date(<% tp.file.creation_date("YYYY-MM-DD") %>) SORT file.ctime DESC
```

---
Tags: #daily 
- Week: [[<%tp.date.now("YYYY-[W]ww")%>]] 
- Month: [[<%tp.date.now("YYYY-MM")%>]] 
- Quarter: [[<%tp.date.now("YYYY-[Q]Q")%>]] 
- Year:  [[<%tp.date.now("YYYY")%>]] 