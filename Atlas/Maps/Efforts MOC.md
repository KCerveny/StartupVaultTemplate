---
up:
  - "[[Home]]"
created: 2024-03-18
tags:
  - map
  - dashboard
---
# Efforts Dashboard
Keep your priorities in order. Quickly adjust your bandwidth as needed. 

## Efforts
> [!important]+ ###  On
> ``` dataview
> TABLE WITHOUT ID
> file.link as "",
>  rank as "Rank"
> FROM "Efforts/On"
> SORT rank asc
> ```


> [!recycle]+ ###  Ongoing
> ``` dataview
> TABLE WITHOUT ID
> file.link as "",
> rank as "Rank"
> FROM "Efforts/Ongoing"
> SORT rank ASC
> ```


> [!activity]+ ###  Simmering
> Efforts can easily move from `on` to `simmering` in the background.
>
> ``` dataview
> TABLE WITHOUT ID
> file.link as "",
> rank as "Rank"
> FROM "Efforts/Simmering"
> SORT rank asc
> ```


## Action Items
---

```tasks
not done
filter by function task.file.root === 'Efforts/'
group by function task.file.folder
group by function task.file.filename
```

---

> [!faq]+ Learn more about Efforts
> - [[A deeper dive into how ACE works]]
> - [[Why Efforts are Liberating]]
> - [[The Four Intensities of Efforts]]
> - [[How ideas and efforts play nicely together]]
> - [[The big differences between efforts and projects]]
>   
>   ![[robert-mccall-black-hole-concept-art copy.jpg]]

Back to [[Home]].
