---
up: "[[🏠 Home]]"
tags:
  - "#map/view "
created: 2023-12-13T11:55
updated: 2023-12-18T12:04
---

# The Inbox
This isn't a normal inbox. It's a cooling pad 🧊.

Thoughts come in hot 🌶. But after a few days, they cool down ❄️.

When cooler thoughts prevail, you can better prioritize. Cool? 

This view looks at the 20 newest notes in your **+ Encounters** folder. As you process each note, make connections, add details, move them to the best folder,  and delete everything that no longer sparks ✨. 

> [!HINT]+ This data view 🔬 of 20 latest Notes.

``` dataview
TABLE WITHOUT ID
 file.link as "Encounters and new notes",
 (date(today) - file.cday).day as "Days alive",
 tags as "Tags"

FROM "+ Encounters" and -#on/readme 

SORT file.cday asc

LIMIT 50
```



> [!idea] Total files in + Encounter Folder



If you want to encounter some new things, check out: [🐦](https://www.twitter.com) or 📚.
