  # Agenda


```dataview
TABLE duedate, duedate - date(today) AS "Remaining months",(duedate - date(today)).day AS "Remaining days"
WHERE file.name = "100 DAYS DSA"
```

----
# All Notes
```dataview
table
WHERE file.mtime != null and file.name != "HOMEPAGE"
SORT file.mtime desc
```