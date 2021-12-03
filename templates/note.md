---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
# <%* var title = await tp.system.prompt("Title"); await tp.file.rename(title) %> <% title %>
<% tp.file.cursor(1) %>

---
# References

```dataview
TABLE summary AS "Summary" FROM #event and "zettelkasten" WHERE contains(file.outlinks.file.name, "<% tp.file.title %>") SORT file.ctime DESC
```

---
Tags: 