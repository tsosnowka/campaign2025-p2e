```dataviewjs
let pages = dv.pages("").where(p => p.file && p.file.mtime);
let last = pages.sort(p => p.file.mtime, 'desc')[0];
//dv.paragraph("Ostatnio zmodyfikowany plik: " + last.file.link);
dv.paragraph("Data ostatniej modyfikacji: " + last.file.mtime.toFormat("yyyy-LL-dd HH:mm"));
```
---
[[Lista sesji]] 
```dataviewjs
let firstPage = dv.pages('"sessions"')
.where(p => p.file.name.startsWith("Sesja"))
.sort(p => p.file.name, 'desc')[0];
if(firstPage) {
	dv.span("Najnowsza sesja: " + firstPage.file.link);
}
```
---
[[Nasza drużyna]] 
