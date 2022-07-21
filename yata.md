# Yata: Yet Another To-Do App

[Testflight Link](https://testflight.apple.com/join/pGhH4eRP)

![Demo Gif](/beetee17.github.io/assets/yata/Onboarding.gif)

![Test](/docs/assets/overframe-window.png)

> What is important is seldom urgent and what is urgent is seldom important. 
> - Dwight Eisenhower

Yata is a to-do app that inspired by a variety of task management systems/philosophies, including the Eisenhower Matrix, Pomodoro method, and Time-boxing.

### Main Features
- **iCloud Integration**. All your tasks and data are automatically kept in sync between iOS devices that share an iCloud account. 
- **Daily Planner**. Yata deeply integrates with your device's calendar, allowing you to schedule pomodoro-style time blocks for your tasks in seconds.
- **Eisenhower Matrix**. Combat the mere-urgency effect and maximise the amount of time spent on tasks that are important to you.
- **Flexible Organisation System**. Categorise and group tasks in a way that makes most sense to you with as many (or as little) of the provided methods, such as tags, lists, projects, areas and sub-tasks. Find out more via the detailed tutorial screen!
- **Powerful Task Filtering**. Focus on the tasks that matter to you in the moment and avoid getting distracted by the clutter of irrelevant tasks. You can view tasks by their deadline, urgency, tag, list, project, area, or any combination of those attributes. 
- **Quick Add** allows you to create tasks with minimal friction. The appropriate attributes of the new task are automatically inferred based on your currently applied filter combination. There is also support for natural language dates, allowing you to set due dates inline. 

### Other Features
- Recurring tasks
- Upload and view attachments to a task
- Edit tasks in bulk
- Customise the sort order of tasks
- Search tasks by the contents of their title and notes
- List view as an alternative to the matrix layout for smaller devices. 

# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Coming Soon]
- Custom ordering of areas and tags
- Add Projects which are completable collections of tasks

## [Someday]
- Scratch pad upgrades (Make it behave similar to the iOS Notes app)
- Habit Tracker
- Pomodoro Timer

## [0.3.0 (3)] - 2022-07-20
### Added
- Ability to bulk move todos to a specific project or area
- Update onboarding views with better quality gifs 
- Add tutorial screen for creating and editing projects
- Add back pinch gesture to toggle full screen

### Changed
- Renamed Projects to Areas
- Projects, are now (completable) collections of todos and subtodos, similar to Things 3
- A todo can belong to either a project or area

### Fixed
- Crash when deleting a tag when it is currently selected as a filter

## [0.3.0 (2)] - 2022-07-19
### Changed
- Edit mode is set to inactive after user has finished creating/editing an area
- Change font size and placeholder text for notes input in quick add view

### Fixed
- Fix bug where area editor was dismissing automatically when keyboard is resigned

## [0.3.0 (1)] - 2022-07-19
### Added
- Ability to add notes to todo from quick add view

### Changed
- Changed the placeholder text for the quick add task description to one that lets users know they can use natural language to set due dates.
- Renamed Project to Area (may cause exisiting todos to lose information about their projects, apologies :/)

## [0.2.0 (10)] - 2022-07-18
### Added
- Dismiss tags menu when user is done with quick add
- Add subtle gradient to project icons
- Added the ability to customise sort ordering of todos 
- Ability to override parsing by selecting date manually (known limitation: after doing so user cannot re-activate parsing without re-invoking quick add)
- Remove extra whitespaces from parsed titles

### Changed
- Change archive filter to more useful completed filter
- Calendar view scrolls to current time when viewing the current day, but scrolls to the first event when viewing other days

### Fixed
- Fix project icon not updating on todo card
- Fix visual glitch in project filters: icon rounded edges had a slight grey border
- Fix: the word 'do' was being parsed as tomorrow's date
- Fix calendar view scrolling past its bounds

## [0.2.0 (9)] - 2022-07-15
### Added
- Add the ability to change pin status of quick add todo
- Add background to project icons with the ability to customise its colour
- Add max width to quick add for larger screens
- Add visual indicators for project and todo list in todo view

### Changed
- Move due date text to top right and recurring indicator to bottom right

### Fixed
- Visual glitches with todo title in quick add view when using natural language dates.
- Fix subtodo quick add bug where text field was not focusing properly.
- Forgot to respect todo list settings in quick add
- Fix some tags were appearing with white background 

## [0.2.0 (8)] - 2022-07-15
### Added
- Natural language dates parsing in quick add (Experimental)

### Changed
- Rearrange UI elements in quick add view
- Change quick add cancel button to a save button

### Fixed
- Visual glitches when todo title was too long in quick add view


## [0.2.0 (7)] - 2022-07-15
### Added
- Natural language dates parsing in quick add (Experimental)

## [0.2.0 (6)] - 2022-07-14
### Added
- Calendar view initalises to current date and time
- Improved create new todo experience - allows for quick-adds
- Add the option to infer recurring events when the todo is recurring. For example, if you drag a todo that is set to recur every 4 days, the app will ask if you want the created event to also recur every 4 days. This behaviour can be changed in the settings.
- Add counts to the filter rows. Displays the number of incomplete tasks that have the particular project or tag.

### Fixed
- Dragging a todo would not scroll to calendar after an event has been created
- Todo notes editor was not highlighting links that have # symbol correctly

## [0.2.0 (5)] - 2022-07-13
### Added
- Keyboard dismiss button for the notes text editor on iPhones

### Fixed
- Unable to add subtasks 

## [0.2.0 (4)] - 2022-07-13
### Added
- Back button to onboarding views for clarity in UI
- Settings button in the matrix view's menu button. Another way for users to get to the settings screen (it is also in the filters menu)

### Fixed
- Edit todo button in todo context menu was not working

## [0.2.0 (3)] - 2022-07-12
### Added
- Show onboarding screen for the user's first launch

## [0.2.0 (3)] - 2022-07-12
### Added
- Animations for bulk move actions

## [0.2.0 (2)] - 2022-07-12
### Fixed
- New todo page was not respecting current todo list filter
- New todo was not being added into the right eisenhower matrix cell

## [0.2.0 (1)] - 2022-07-12
### Added
- Ability to upload files or media as attachments to a task
- Various tutorial pages for tags, projects, lists and subtasks

### Changed
- Adjusted the padding and icon size of projects in the filter menu

### Fixed
- Add sub todo button was not responding to taps
- Todos would sometimes loop infinitely while in edit mode
- Tapping the add todo button caused a crash when a tag or project was filtered
- Matrix view was too low on iPad
- Todo detail view was not displaying properly on iPad

## [0.1.0 (9)] - 2022-07-11
### Added
- Ability to upload images and attachments to tasks

## [0.1.0 (8)] - 2022-07-11
### Added
- Ability to add subtasks to new todos
- Alert on dismissing sheet views when there are unsaved changes

### Fixed
- Some tasks would behave like they were recurring even if they had no due date set.
- Fix new todo and sub todos not respecting current filter preferences

## [0.1.0 (7)] - 2022-07-09
### Added
- Added the ability to set colors for both projects and tags
- Added support for recurring tasks
- Added the ability to open links detected in todo notes
- Added progress indicator to tasks with sub tasks
- Filter preferences are now saved and synced across devices

### Changed
- Changed the default behviour of completing subtasks as such: When all subtasks are completed, the parent task is NOT automatically completed

### Fixed
- Fixed: cannot open settings menu after editing/creating todo

## [0.1.0 (6)] - 2022-07-08
### Fixed
- Updated the logic for sorting todos. Previous version caused infinite looping when multiple todos were pinned

## [0.1.0 (5)] - 2022-07-08
### Added
- Added animations to filtering actions

## [0.1.0 (4)] - 2022-07-08
### Fixed
- Fix bug with filtering due to eisenhower status
- Fix visual bug with scroll overflow

## [0.1.0 (3)] - 2022-07-08
### Added
- Add inbox, today, anytime and someday categorisations inspired by GTD
- You can now organise a set of todos into Projects
- Add various utility functions to Select Mode (previously Edit Mode). For example, move a group of todos to a certain Project/Category or add tags to them
- Add more default filters such as Overdue and Due in 7 Days
- Add ability to search todos by title and their contained notes
- Add markdown support for Scratch Pad
- Scratch pad notes can now be saved and synced across devices
- Add list view as an alternative to the matrix view (useful for smaller devices like iPhone)

## [0.1.0 (2)] - 2022-07-04
### Added
- Added the ability to filter tasks that have no due date
- Added a button to clear selection of filters
- Added ability to group tasks into lists/folders (in addition to tags)
- Added the ability to pin tasks to the top via the context menu
- Replaced the glitchy swipe to delete with context menu.
	Note: If you would like to delete multiple todos quickly, long press on the todo and select "Enter Edit Mode".

### Changed
- Changed the iPad UI

### Removed
- Removed save button in the editing screen (changes are automatically saved when the screen is dismissed)

### Fixed
- Fixed a bug where some todos required 2 taps to bring up the edit screen
Thank you for downloading yet another to-do app.


