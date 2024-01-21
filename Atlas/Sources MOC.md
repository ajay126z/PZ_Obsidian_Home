---
up: "[[🏠 Home]]"
tags:
  - "#map "
created: 2023-12-13T11:55
updated: 2023-12-18T12:04
---

# Sources MOC
This is where I keep tabs on some of the sources I have encountered.

What "sources" should you track? Check out the tags pane. Find "source" and twirl it down. The sources I have decided to include tracking over the years include: *books, movies, songs, research papers, plays, paintings, quotes, videos, speeches, poems, tweets, articles, and newsletters*. 

Enjoy checking out the comprehensive [[Source Starmap 🔭]] and perusing my [[🗄️ Bookshelf]]  where my book notes are stored. Also, I have interests in [[📥 Books Inbox]] where I plan my book Reading Goals and [[📚 Books Pile]]. And to honor the old ones, I also keep a [[Commonplace Book]] based on tags. 
Also process other sources like [[Youtube]], [[Article]], And [[Tweets]] from  [[ReadItLater]] Inbox.



## A data view from the Sources folder
This is a simple data view pulling anything from the **Sources** folder.

> [!HINT]+ Book Sources

```dataview
table Tags, file.mday as "Last Updated"
from "Sources" and -#on/readme and #source/book 
sort file.mtime desc
```

---

> [!HINT]+ Course Sources
```dataview
table tags, file.mday as "Last Updated"
from "Sources" and -#on/readme and #source/course   
sort file.mtime desc
```

---


