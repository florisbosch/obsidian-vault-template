---
created: <%tp.file.creation_date()%> 
modified: 
aliases: 
tags: [dailynote]
banner: "https://preview.redd.it/arqa352ph7x61.jpg?width=960&crop=smart&auto=webp&s=84f9245d607b029667d5bfc4abf36547fc6213de"
---

## ๐ Notes

<% tp.file.cursor() %>

#### ๐จ๐ปโ๐ป Today's Tasks 
```tasks 
not done 
due today 
sort by description 
```

#### โ๏ธOverdue Tasks 
```tasks 
not done 
due before today 
sort by due 
```

##### This Week's Tasks 
```tasks 
not done 
due after today 
due before in 1 week 
sort by due 
``` 

#### ๐๏ธ Unscheduled Tasks 
```tasks 
not done 
no due date 
sort by path
```

---
### Notes Created

```dataview
List FROM "" WHERE dateformat(date(split(created, " ")[0] + "T" + split(created, " ")[1]), "yyyy-MM-dd") = "<%tp.date.now("YYYY-MM-DD")%>"
```

### Notes Modified

```dataview
List FROM "" WHERE dateformat(date(split(modified, " ")[0] + "T" + split(modified, " ")[1]), "yyyy-MM-dd") = "<%tp.date.now("YYYY-MM-DD")%>" AND dateformat(date(split(created, " ")[0] + "T" + split(created, " ")[1]), "yyyy-MM-dd") != "<%tp.date.now("YYYY-MM-DD")%>"
```
