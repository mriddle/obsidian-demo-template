---
creation date: <% tp.file.creation_date() %> 
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
summary: <%* var title = await tp.system.prompt("Title"); await tp.file.rename(tp.date.now("YYYY-MM-DD HHmmss") + " - " + title) %> <% title %>
aliases: []
---
<% tp.file.cursor(1) %>

---
Tags: #event, [[<% tp.file.creation_date("YYYY-MM-DD") %> ]]