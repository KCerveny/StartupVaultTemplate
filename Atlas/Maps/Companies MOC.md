---
up:
  - "[[Home]]"
related:
  - "[[Company Template]]"
created: 2024-04-29 12:49
tags:
  - map
  - MOC
---

# Companies MOC
A place where I can keep track of and connect companies and people. Really a less-important version of the [[People MOC]], but useful when I have multiple contacts at a single organization.


```meta-bind-button
label: New Company Note
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Atlas/Utilities/Templates/Company Template.md
    folderPath: Atlas/Notes/Companies
    fileName: Enter Company Name
    openNote: true

```

# Companies
```dataview
TABLE WITHOUT ID
file.link AS "Company"
from "Atlas/Notes/Companies" and -#readme
sort file.name asc
```

