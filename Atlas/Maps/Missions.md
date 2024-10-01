---
up:
  - "[[Tablet Menu]]"
related: 
created: 2024-05-13 13:51
tags:
  - map
  - MOC
cssclasses:
  - cards
  - myTable
  - cards-align-bottom
  - cards-cover
  - cards-16-9
mission_folders:
  - Efforts/On
  - Efforts/Ongoing
  - Efforts/Simmering
selected_folder: Efforts/On
selected_mission: Efforts/On/Apply for Jobs.md
---
# Missions
```meta-bind-js-view

---
const mb = engine.getPlugin('obsidian-meta-bind-plugin').api;


// 1) Set up mission folders dynamically
const folder_target = mb.createBindTarget('frontmatter', context.file.path, ['mission_folders']);

const folders_list = [
	"Efforts/On",
	"Efforts/Ongoing",
	"Efforts/Simmering"
]

mb.setMetadata(folder_target, folders_list)

```
```meta-bind-js-view

---
const mb = engine.getPlugin('obsidian-meta-bind-plugin').api;


// 1) Set up mission folders dynamically
const folder_target = mb.createBindTarget('frontmatter', context.file.path, ['mission_folders']);

const folders_list = [
	"Efforts/On",
	"Efforts/Ongoing",
	"Efforts/Simmering"
]

mb.setMetadata(folder_target, folders_list)

```
```meta-bind-js-view

---
const mb = engine.getPlugin('obsidian-meta-bind-plugin').api;


// 1) Set up mission folders dynamically
const folder_target = mb.createBindTarget('frontmatter', context.file.path, ['mission_folders']);

const folders_list = [
	"Efforts/On",
	"Efforts/Ongoing",
	"Efforts/Simmering"
]

mb.setMetadata(folder_target, folders_list)

```
```meta-bind-js-view
{mission_folders} as folders
---
let missionFolders = context.bound.folders; // Creating tabs selection

// Re-usable function, gets most immediate folder name, not path
const only_folder = (str) => String(str).split('/').pop() || str;

const foldersOptionList = missionFolders.map((name) => `option(${name}, ${only_folder(name)}),` );
let foldersOptions = foldersOptionList.join('\n');

const tabs_selection = `
	INPUT[
	select(
		${foldersOptions}
		class(tabsSelection)
	):selected_folder]
`

const folders_tabs = '```meta-bind\n' + tabs_selection  + '\n```\n';
const renderMeta = [folders_tabs].join("\n");
return engine.markdown.create(renderMeta)
```

> [!multi-column]
> 
> > [!blank]
> > ```meta-bind-js-view
> > {selected_folder} as folder
> > ---
> > let dataviewjs_display = `
> > 	const queryScript = "Atlas/Utilities/Scripts/missionsList";
> > 	const missionsArgs = {
> > 		missionFolder: "${context.bound.folder}"
> > 	};
> > 	await dv.view(queryScript, missionsArgs);
> > `;
> > 
> > if (context.bound.folder) {
> > 	return engine.markdown.create('```dataviewjs\n' + dataviewjs_display + '\n```\n');
> > } else return;
> > ```
>
> > [!blank]
> > ```meta-bind-js-view
> > {selected_mission} as target
> > ---
> > 
> > let dataview_query = `
> > TABLE WITHOUT ID
> > 	("" + up) as "Category",
> > 	"Rank: " + rank as "Rank",
> > 	embed(link(image)) as Image,
> > 	("## " + file.link) as "Title",
> > 	("Completed: " + progress + "/" + completion_target + " " + completion_target_units ) as "Completion",
> > 	("### Reward: " + default(reward, "???")) as Reward,
> > 	("" + description) as "Description"
> > 
> > WHERE contains(file.path, "${context.bound.target}") and rank
> > SORT rank asc
> > LIMIT 1
> > `
> > 
> > if (context.bound.target) {
> > 	return engine.markdown.create('```dataview\n' + dataview_query + '\n```');
> > } else return;
> > 
> > ```


