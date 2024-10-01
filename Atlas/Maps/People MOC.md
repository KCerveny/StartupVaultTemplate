---
up:
  - "[[Home]]"
related:
  - "[[People Template]]"
created: 2024-03-18
tags:
  - map
  - MOC
cssclasses:
  - list-cards
---
# People MOC
A personal CRM. People Notes are about jotting down notable information about people and linking people back to [[Meetings MOC]].

```meta-bind-button
label: New Person Note
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Atlas/Utilities/Templates/People Template.md
    folderPath: Atlas/Notes/People
    fileName: CHANGEME
    openNote: true

```


#### **Table of Contents**
1) [[#People Cards]]
2) [[#People Table]]


## People Cards
```dataview
LIST

FROM "Atlas/Notes/People" and -#readme
SORT file.name asc
```



## People Table
```dataview
TABLE WITHOUT ID
file.link AS "Person", 
role AS "Role"
from "Atlas/Notes/People" and -#readme
sort file.name asc
```
