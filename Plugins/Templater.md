---
name: Templater
community: true
version: v1.12.0
source: "[link](https://github.com/SilentVoid13/Templater)"
docs:  "[link](https://silentvoid13.github.io/Templater/)"
category: templates
---

# Templater
Templater allows interactive templates to be created so that each folder can have their own template style. The template for the plugins folder in this example, uses this code to prompt for a title for the page and slip in links for 

```
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
docs:  "[link](<% tp.system.prompt("Docs:", "none") %>])"
category: <% tp.system.suggester(["Category: data", "Category: editor", "Category: templates"], ["data", "editor", "templates"]) %>
---

# <%* tR += `${title}` %>

```

The [[Good Plugins]] page then can construct a table based on this meta-information.