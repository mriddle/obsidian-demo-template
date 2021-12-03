---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
<% await tp.file.rename(tp.date.now() + " - Retro") %>
# <% tp.date.now("YYYY-MM-DD") %> [[Retrospective|Retro]]

## What went well?

<% tp.file.cursor(1) %>

## What could go better?

## What should we do differently?

---
Tags:  #retro #event