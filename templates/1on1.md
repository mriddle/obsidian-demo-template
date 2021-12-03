---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
# <%* var name = await tp.system.prompt("Name"); await tp.file.rename(tp.date.now() + " 1on1 with " + name) %> <% tp.date.now("YYYY-MM-DD") %>
Follow-ups
- [ ] 

<% tp.file.cursor(1) %>

---
Tags:  #1on1 <% "#1on1" + name.toLowerCase() %> #event