---
up: "[[Sources MOC]]"
prev: "[[📥 Books Inbox]]"
tags:
  - "#note/develop🍃"
created: 2023-12-13T11:55
updated: 2024-01-10T12:03
---

#  🗄️ My Book Shelf 

---
![[434674B0-1A1A-4B17-808F-2B5353F53B6E.jpeg]]

---

 Welcome to My library! We are proud to provide a home for readers and learners of all ages.  This is a place for you to explore the world of knowledge. Come discover something new today!

### [[📚 Books Pile]]
These books list is not categorized, so first step would be categorize it.  
- Category
- Pick the Category based on interest and need.
- Track current books reading.
- Each book should have a separate note using the book template.

### [[📥 Books Inbox]] 
This is where I store books which I find Interesting but currently I don't have.
Tag any book with #[[📥 Books Inbox]] and it will be shown in that page.

## How to Read a Book and Apply it in Life
- We live in an era where knowledge is cheap and easily available. Accessing Knowledge is not the problem. The problem is determining what is truly important and then doing something with it.
- Let's face the facts, reading a book is a waste of time if you don't apply anything from the book to your life.
- Convert knowledge into action.
	- Identify Habits, Principle, Skills
- What to do after Reading a Book?
	- Read & Listen
	- Take Action
		- Follow simple action steps to keep moving towards your goals and dreams.
	- Transform
		- Action Plans and Evaluations will elevate your learning.
----

## Current Book Summary 

> [!cite]  List of all my Books

```dataview 
TABLE WITHOUT ID 
	"![|60](" + bookCover + ")" as Cover, 
	file.link as "Book Name",
	bookAuthor As "Author", 
	bookCategory As "Category", 
	tags as "Tags", 
	bookStatus as "Status", 
	file.mtime As "Last Modified"
FROM "Sources" and #source/book 
SORT file.mtime desc
```

## Books Grouped by Reading Status 

```dataview
TABLE WITHOUT ID 
	bookStatus as "Status",
	rows.file.link AS Book
FROM "Sources" AND #source/book 
GROUP BY bookStatus
SORT Status Desc
```


## Books Grouped by Category

```dataview
TABLE WITHOUT ID 
	bookCategory as "Category",
	rows.file.link as Book
FROM "Sources" AND #source/book 
GROUP BY bookCategory
SORT Category ASC
```

## List of all books

```dataview
TABLE WITHOUT ID
	link(file.link, Title) as Title,
	"![|60](" + bookCover + ")" as Cover,
	bookAuthor as Author,
	bookStatus as Status
FROM "Sources" and #source/book 
WHERE !contains(file.path, "Templates")
SORT Title ASC, file.ctime ASC
```


---
