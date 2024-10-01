---
tags:
  - customer_discovery
  - dynamic
---
# All Hypotheses

%% 
Using the dataview plugin:
- [Dataview Github](https://github.com/blacksmithgu/obsidian-dataview?tab=readme-ov-file)
- [Dataview Docs](https://blacksmithgu.github.io/obsidian-dataview/)
%%

> [!warning]- The following tables are dynamically generated, and represent the current marked status of these files. Do not reference for retrospective purposes.
> Tables generated using the DataView Obsidian plugin

```meta-bind-button
label: New Hypothesis Note
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Atlas/Utilities/Templates/Customer Discovery Templates/Business Model Hypothesis Template.md
    folderPath: Atlas/Notes/Customer Development Process/1. Customer Discovery/Phase 1 - Hypothesis/Discovery Hypotheses
    fileName: HYPOTHESIS NAME
    openNote: true

```

## Active Hypotheses
---
```dataview
table status as Status, date_authored as "Date Authored" 
from #hypothesis 
where status = "active"
sort name desc
```



## Inactive Hypotheses
---
```dataview
table status as Status, date_authored as "Date Authored" 
from #hypothesis 
where status = "inactive"
sort name desc
```

## Rejected Hypotheses
---
```dataview
table status as Status, date_authored as "Date Authored" 
from #hypothesis 
where status = "rejected"
sort name desc
```
