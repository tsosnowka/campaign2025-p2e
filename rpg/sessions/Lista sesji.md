
```dataviewjs
dv.list(
  dv.pages('"sessions"')
    .where(p => p.file.name.startsWith("Sesja"))
    .sort(p => p.file.name, 'desc')
    .map(p => p.file.link)
);
```

---
```
//alternative version without js //just pure dataview query
//```dataview
LIST
FROM "sessions"
WHERE startswith(file.name, "Sesja")
SORT file.name desc
```