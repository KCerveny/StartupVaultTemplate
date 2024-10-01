---
tags:
  - meeting
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
summary: ""
up:
  - "[[Meetings MOC]]"
meeting_date: 2024-05-15
---
# Meeting Notes
> [!calendar] Meeting Date
> Meeting Date: `INPUT[datePicker():meeting_date]`

> [!id] Attendees
- 

> [!map] Agenda
- 
## Notes





### Key Points and Decisions

> [!keaton]+ Meeting Summary
> `INPUT[text(	placeholder(One sentence summary), limit(50) ):summary]`

> [!award] Key Points
- 
#### Action Items
%% Things to develop by next meeting %%
- [ ] Complete summary property in this file