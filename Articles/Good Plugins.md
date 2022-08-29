# Plugin List
This uses the [[Dataview]] plugin to generate a table of all the articles in the `Plugins` folder.  The `Version` value in this table is here to show what the latest version of the plugin was when I evaluated the plugin.

```dataview
TABLE WITHOUT ID
   file.link AS "Name",
   version AS "Version",
   source AS "Source",
   docs AS "Docs",
   category AS "Category"
FROM "Plugins" SORT file.link ASC
```