---
up:
  - "[[Home]]"
related:
  - "[[Meeting Template]]"
created: 2024-03-18
tags:
  - map
  - MOC
  - wide-table
---
# Meetings MOC
This MOC is based on Dann Berg's [Obsidian Meeting Note Template](https://dannb.org/blog/2023/obsidian-meeting-note-template/#fn:4)

```meta-bind-button
label: New Meeting Note
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Atlas/Utilities/Templates/Meeting Template.md
    folderPath: Calendar/Meetings
    fileName: Meeting Name
    openNote: true

```

Meetings are timestamped events with other people, where information is exchanged and collected. Meeting notes are intrinsically ephemeral. They're stored in a separate Space than other Umami notes (`Timestamps/Meetings`) and rarely reviewed. If there's information in a meeting that needs to be accessed later, it should be moved into a more evergreen note in the Umami folder. 


## Meeting Notes

```dataview
TABLE file.cday as Created, 
summary AS "Summary"
FROM "Calendar/Meetings" and -#MOC and -#readme
SORT file.cday DESC
```
