<%* 
     let title = tp.file.title 
     if (title.startsWith("Untitled")) {
       title = await tp.system.prompt("Title"); 
       await tp.file.rename(`${title}`); 
     }
     tR += ""%>---
name: <%* tR += `${title}` %>
community: <% tp.system.suggester(["Community Plugin: true", "Community Plugin: false"], ["true", "false"]) %>
version: <% tp.system.prompt("Version:", "v0.0.0") %>
source: "[link](<% tp.system.prompt("Source URL:", "") %>)"
docs:  "[link](<% tp.system.prompt("Docs:", "none") %>)"
category: <% tp.system.suggester(["Category: data", "Category: editor", "Category: templates", "Category: workflows"], ["data", "editor", "templates", "workflows"]) %>
---

# <%* tR += `${title}` %>
