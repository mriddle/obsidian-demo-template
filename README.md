# Obsidian Template
Obsidian template for others interested in my setup and workflow.

The information below is my personal preferences, the plugins I use and the value I find therein. 

If any of this resonates with you please feel free to fork it and make it your own. 

## What is Obsidian?
> Obsidian is a powerful **knowledge base** on top of  a **local folder** of plain text Markdown files.

That last part is the key difference to other similar tools and why I decided to try Obsidian out. Should the product no longer be suitable your content is readily available. You could simply continue using VSCode or another text editor, although without some of the [[#Plugins Options|bells and whistles]] that make it such a joy to use. 

## Structure
- **files** for all of your attachments go here.
- **reference notes** for content that's not your original content. It's useful when you've got some source material which you'd like to directly embed or reference elsewhere. E.g. [[Zettelkasten]]
- **templates** is where the magic happens.
- **zettelkasten** the one and only folder all of your notes should go in. Don't try to structure the content as it works against the idea of [[Zettelkasten]] whereby you reference and link your thoughts and notes together. The structure of your notes should be fluid, not static IMO.

## Workflow
### Initial setup
Create a new note from the day, week, month, quarter and year you're in. Do it via the command pallet and [[#Periodic Notes https github com liamcain obsidian-periodic-notes|period notes plug]]. E.g. ⌘+P  -> "Open daily note "

### Daily workflow
- Plan out your day in the daily note
- Create a new event for meetings, thoughts and discussions. These will automatically be associated with your daily note using backlinks and dataview.
	- Create specific events for things you might do often like a [[1on1]] or [[retro]].
	- You can get creative with your templates using [[#Templater https silentvoid13 github io Templater|templater]] and create your note programatically. 
- Go about your day
- At the end of the day update your highlights, move stuff to done and add any other action items for the next day. 
- The highlights will be visible in the #weekly highlights, which allows you to curate the list available for the month and so forth until you're left with a highlight reel for the year.
- Any leftover tasks you didn't get to that day will be visible in [[TODO]]

As you continue with this pattern topics will begin to surface, which you may want to create a separate [[note]] for. I use the [[note]] template to formalize the content from the events that occur during the day, week, month, etc. 

These topics will continue to grow over time at which point you'll want to map out your thoughts with the #MOC. An example of a Map of Content could be [[Professional Development]] which would include your [[1 on 1]]s with your manger, career goals, [[books]], etc. From within that MOC the [[books]] [[note]] or [[moc]] could then list each book as a [[note]] which includes your summary or thoughts around that content. 

### My thoughts on this process

With this process I believe you can start to build out *Google for your brain*, revisiting your thoughts and the associated context at that point in time, and linking with the thoughts of today. In his way I believe you can reduce the amount of stress or cognitive load you need to carry around with you and free your mind up to think deeper.

### Troubleshooting

If you have any issues with configuring the plugins or playing with the templates, know that it's all JavaScript at the end of the day. Toggle the developer tools within Obsidian to debug and resolve your issue.

## Theme
### [Minimal Theme](https://github.com/kepano/obsidian-minimal)
The prettiest theme I've found to date, it's also popular which means there are less bugs. The UI on mobile is functional, unlike some other themes, and it's customisable using the [[#Minimal Theme Settings https github com kepano obsidian-minimal-settings|Minimal Theme Settings]] and [[#Style Settings https github com mgmeyers obsidian-style-settings|Style Settings]] plugins. 

## Plugins & Options
*I've made the following changes to the default configuration*

### Options
#### Files and links
- Deleted files are moved to .trash folder instead of system trash for easier recovery across devices.
- New notes created in "zettelkasten" folder
- New attachments stored in "files" folder

#### Hotkeys
- Removed Create Note shortcut
- Updated "Templater: Create new note from template" to use "Create Note" shortcut. This is used as part of my [[#Daily workflow]]

### Core Plugins
- On: Tag pane
	- Display tags and occurrences
- On: Templates
	- This should really be the default, it allows you to create templates.
- On: Outline
	- Display the outline of the document you're in
- On: FIle recovery
	- Stores snapshots of your documents so you can revert to prior versions easily.

### Community Plugins
#### [Admonition](https://github.com/valentine195/obsidian-admonition)
Customizable blocks, useful for bringing attention to a part of the document. Also provides a mechanism to have the content collapsed by default. Useful if you've got content on your screen that you don't want others to see if they happen to walk by.

Example:

```ad-note
title: Confidential
icon: user-lock
collapse: true

The cake is a lie.

```

#### [Calendar](https://github.com/liamcain/obsidian-calendar-plugin)
Widget on the right which integrates nicely with the [[#Periodic Notes https github com liamcain obsidian-periodic-notes]|period notes]] plugin

![[Pasted image 20211203123759.png]]

#### [Dataview](https://github.com/blacksmithgu/obsidian-dataview)
Query your notes and compile custom views or lists to surface the relevant information in other notes. 

Example: 

#### [Hider](https://github.com/kepano/obsidian-hider)
Hide some of the default UI elements to better focus on your content.

#### [Minimal Theme Settings](https://github.com/kepano/obsidian-minimal-settings)
Ability to further tweak your [[#Minimal Theme https github com kepano obsidian-minimal|miniam theme]]

#### [Natural Language Dates](https://github.com/argenos/nldates-obsidian)
Use `@today`, `@tomorrow`, `@yesterday` to retrieve the date.

#### [Obsidian Git](https://www.google.com/search?q=obsidian+git&rlz=1C5CHFA_enDK981DK981&oq=obsidian+git&aqs=chrome.0.69i59l2j0i512j0i20i263i512j0i512j69i60l3.1934j0j4&sourceid=chrome&ie=UTF-8)
Provide a GitHub repository and sync your notes, you can set it up to happen automatically or on demand. 

This is not compatible with iOS devices at the moment, use iCloud instead of your devices includes mobile devices.

#### [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes)

Create notes for the day, month, quarter and year. You could do this solely with templates but it integrates nicely with the [[#Calendar https github com liamcain obsidian-calendar-plugin|calendar]] plugin 

#### [Reminder](https://github.com/uphy/obsidian-reminder)
#### [Sliding Panges (Andy's Mode)](https://github.com/deathau/sliding-panes-obsidian)

Iinspired by the UI of [Andy Matuschak's notes](https://notes.andymatuschak.org/). A nicer workflow when working with multiple panes

#### [Style Settings](https://github.com/mgmeyers/obsidian-style-settings)

Allows you to easily customise themes, like the [[#Minimal Theme https github com kepano obsidian-minimal|Minimal Theme]]

#### [Tag Wrangler](https://github.com/pjeby/tag-wrangler)

Adds a context menu for tags allowing you to better manage them. 
-   [Rename the tag](https://github.com/pjeby/tag-wrangler#renaming-tags) (and all its subtags)
-   Start a new search for the tag (similar to a plain click)
-   Add the tag as a requirement (`tag:#whatever`) to the current search
-   Add an exclusion for the tag (`-tag:#whatever`) to the current search
-   Open a random note with that tag (if you have the [Smart Random Note](https://github.com/erichalldev/obsidian-smart-random-note/) plugin installed and enabled)
-   Collapse all tags at the same level in the tag pane
-   Expand all tags at the same level in the tag pane

#### [Templater](https://silentvoid13.github.io/Templater/)

A template language that lets you insert variables and functions results into your obsidian notes.

Example: [[event]] [[daily]]