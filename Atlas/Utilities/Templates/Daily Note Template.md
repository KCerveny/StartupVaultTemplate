---
tags:
  - daily-note
date_authored: <% tp.file.creation_date() %>
date_modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
yesterday: '[[Calendar/Daily Notes/<% tp.date.now("YYYY/MM-MMMM/YYYY-MM-DD-dddd", -1, tp.file.title, "YYYY-MM-DD-dddd") %>|<% tp.date.now("YYYY-MM-DD-dddd", -1, tp.file.title, "YYYY-MM-DD-dddd") %>]]'
tomorrow: '[[Calendar/Daily Notes/<% tp.date.now("YYYY/MM-MMMM/YYYY-MM-DD-dddd", 1, tp.file.title, "YYYY-MM-DD-dddd") %>|<% tp.date.now("YYYY-MM-DD-dddd", 1, tp.file.title, "YYYY-MM-DD-dddd") %>]]'
file_date: <% moment(tp.file.title, "YYYY-MM-DD-dddd").format("YYYY-MM-DD") %>
week: '[[Calendar/Weekly Notes/<% tp.date.now("YYYY/YYYY-[W]WW") %>]]'
---
# <% tp.file.title %> Daily Note
<% tp.web.daily_quote() %>

## Today's Agenda
>[!milestone] What is one thing that would make today a success? 


### Day Planner




---
## Tasks
>[!map]- Visit your `Daily Dashboard` to see all tasks
>Add your miscellaneous extra tasks below throughout the day!
>These will automatically be added to your Dashboard and other locations where you query your upcoming tasks.

>[!summary]- Today's Important Tasks
>```tasks
>not done
>(due today) OR (due before today)
>
>sort by urgency
>sort by priority
>
>hide created date
>short mode
>```

- 




---
## Logs


### Today's Activity Log
>[!done]- Tasks Completed Today
> >A list of tasks taken from anywhere in the vault.
> >Query adopted from  [How to Add Tasks to your Daily Notes in Obsidian - Obsidian Rocks](https://obsidian.rocks/how-to-add-tasks-to-your-daily-notes/)
>---
>```tasks
>done on <% moment(tp.file.title, "YYYY-MM-DD-dddd").format("YYYY-MM-DD") %>
>short mode 
>```

>[!Leaf]- Notes Created Today
>```dataview
>List FROM "" WHERE 
>file.cday = date("<% moment(tp.file.title, "YYYY-MM-DD-dddd").format("YYYY-MM-DD") %>")
>SORT file.ctime asc
>```

>[!orbit]- Notes Last Updated Today
>```dataview
>List FROM "" 
>WHERE file.mday = date("<% moment(tp.file.title, "YYYY-MM-DD-dddd").format("YYYY-MM-DD") %>") 
>SORT file.mtime asc
>```

#### Dumped Links
%% Whenever you "share" a URL to Obsidian and place it in your Daily Note, it will end up here. %%