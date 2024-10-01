---
up: 
related: 
date_created: 2024-10-01 09:45
date_last_modified: Monday 20th May 2024 11:44
mission_name: Configure This Mission
description: ""
reward: ""
completion_target: "0"
completion_target_unit: 
image: 
rank: 2
progress: 0
is_pinned: false
is_completed: false
tags:
  - mission
---

```meta-bind
VIEW[{image}][image()]
```

```meta-bind-button
label: Complete Mission
icon: ""
hidden: true
class: ""
tooltip: ""
id: mission-complete
style: destructive
actions:
  - type: updateMetadata
    bindTarget: is_completed
    evaluate: false
    value: true
    
  - type: updateMetadata
    bindTarget: is_pinned
    evaluate: false
    value: false
    
  - type: command
    command: file-explorer:move-file
    
  - type: input
    str: "Missions/Archived"

```


# `VIEW[{mission_name}][text]`

### Overview

> [!blocks]- Mission Configurations
> Set up your mission once, then minimize this window.
> 
>```meta-bind
>INPUT[ text( title(Mission Name), defaultValue(Configure Mission), placeholder(Enter Mission Name) ):mission_name]
>```
>
> ```meta-bind
> INPUT[textArea(title(Mission Description), placeholder(Write mission summary) ):description]
> ```
> 
> ```meta-bind
> INPUT[textArea( title(Reward), placeholder(Reward for completion) ):reward]
> ```
>
>```meta-bind
>INPUT[text( title(Completion Target), placeholder(Target value to complete), defaultValue(10) ):completion_target]
>```
>
>
>```meta-bind
>INPUT[text( title(Completion Target Unit), placeholder(Unit of completion target) ):completion_target_unit]
>```
>
> ```meta-bind
>INPUT[inlineSelect(
>	title(Priority Level), defaultValue(2),
>	option(0, 0: Highest), option(1, 1: High), option(2, 2: Medium), option(3, 3: Low), option(4, 4: Lowest)
>):rank]
>```
>
>```meta-bind
>INPUT[imageSuggester( title(Mission Image), optionQuery("") ):image ]
>```
>

> [!activity]- Mission Updates
> 
>
> ```meta-bind
> INPUT[number( title(Completion Progress), defaultValue(0)):progress]
>```
>
>```meta-bind
>INPUT[toggle( title(Pin Mission) ):is_pinned]
>```
>
> > [!warning]- End Mission
> >Warning: This is a destructive action. This will end and archive this mission.
> >
> >`BUTTON[mission-complete]`
> 

## Notes




## Objectives
```meta-bind
INPUT[list(
	title(Main Goals),
	placeholder(Enter main goals of effort)
):main_goals]
```
### Tasks
- [ ] Wrap-up  and complete mission





