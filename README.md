# obsidian-workflow
Description and files of my Obsidian workflow

## WIP
I'm working on creating a starter version of my workflow that's easy to modify and get going with yourself. Until I can get that done and publish the templates, there is enough detail here to put this all together yourself if you like.

## Motivation
I am a college student with a busy schedule, a small laptop battery, and very little patience for the modern web. I don't want to use a different app or site for note taking, task management, and calendaring. I want one lightweight app to handle all my needs. For a while I was using Notion, but the lack of an offline mode, poor performance, and resource bloat set me searching for a new workflow.

As of now, I am using Obsidian as my daily driver application. It's far from perfect, but it's much better than any other workflow or system I've used in the past. My workflow is also still evolving, and the adaptability and modularity of Obsidian is one of its largest draws. The learning curve can be steep, but like most steep learning curves, it pays off.

This isn't a perfect system- notably, I'm still using Google Calendar for scheduling some events, because Obsidian doesn't support notifications. Still, it works for me for now, and all or some of it might work for you.

## Overview / Is this for me?
The workflow uses *Daily Notes* a dashboard and a bridge to everything relevant to each day. These notes link to *Class Notes*, which are intended as not only a note-taking system but a fluid interface to all other features, especially tasks. The idea is to sit down in class, open the Class Note, and not have to leave it or Obsidian until you get up. I want to vomit information into the system and have it organize everything for me.

This type of system isn't for everyone, but if you like how it sounds, read on.

## Features
The workflow implements the following components entirely within Obsidian and with a high level of integration:
- Note-taking with heavily automated organization
- Task management
- Hourly salary tracking (niche but I find it helpful)
- Basic calendaring

It's easy to do all the other things you'd normally do in Obsidian, too, including:
- Knowledge base
- Formatting assignments
- Whatever else you can think of

Of course, because of the modular Obsidian architecture, everything is customizable to your liking.

## Detailed Architecture
As a college student, my schedule is highly periodic; I know which events (classes) will take place on each day. This lends itself to an workflow based around repetition.

### Daily Notes
The core of the workflow.

A *Daily Note* holds everything I need to know that's relevant for each day, and it's organized as follows:

- A Quick Notes section for whatever miscellaneous information I need to write down each day. It doesn't see too much use since the workflow is designed to place information.

- A Class Notes section which links to pages for only the classes I have on that day, to keep things clean.

- A Tasks section which has several queries for the Tasks plugin. It shows overdue tasks, tasks due today, this week, and afterwards, and finally tasks done today.

- A Planner section which, much like Class Notes, is set up to autofill relevant events for each day. In my case I use it to plan tasks and events around my classes each day. 
	- If you want, you can add the following tag to an entry: `[hours::<numHrs>]` with a number value and it'll be added to a salary hour tracker. I used this to track inconsistent hours for my tutoring job.

All date-based queries are hardcoded based on the date of the note itself, not the day it was generated or the current day. For example, if you create a task with a Friday due date, your Tuesday note will show it as due in several days, even if accessing that note in the future. The Friday note will always show is as being due that day.

### Class Notes
Class notes are linked from daily notes, and they have their own templates with useful tags. As stated above, it's intended that these be used as the centerpiece of not only note-taking but task management. I have "New Task" bound to Ctrl+T, and if I need to add a task, I just add it and continue typing. It'll be linked to in new Daily Notes.

For a time, I also added important concepts to a knowledge base where I could store and review them independent of dates. I have since stopped doing this for reason other than laziness. I suggest you do it, it can help recall and reviewing for exams.

### Folder Structure
Folders are organized like so:
- Vault
	- Daily Notes
		- 2022-02-15
		- etc.
	- Class Notes
		- Class Code (i.e. CS231)
			- 2022-02-15
			- etc.
	- kn (the knowledge base I should be using)
	- misc (catch-all folder)
	- work (for assignment formatting)
		- Class code or project name
			- Assignment

## Miscellaneous
- All dates are in ISO8601 format with dashes (YYYY-MM-DD).
- The full list of plugins I use is:
	- Necessary for the workflow:
		- Calendar
		- Dataview
		- Day Planner
		- Periodic Notes
		- Tasks
		- Templater
	- Helpful in some way:
		- Advanced Tables
		- File Tree Alternative Plugin
		- Natural Language Dates
		- Pandoc
		- Quick Switcher++
		- Quick Latex
		- Sliding Panes
		- Text Expander
