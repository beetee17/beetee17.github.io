# Yata: Yet Another To-Do App

[Testflight Link](https://testflight.apple.com/join/pGhH4eRP)  

Yata is a to-do app that combines both task management and daily planning into a powerful productivity tool for you to get things done.

[Documentation]({{ site.base-url }}/yata/docs)

<img src="https://beetee17.github.io/docs/assets/Yata/images/Yata2Screenshot.png">


### Main Features
- **iCloud Integration**. All your tasks and data are automatically kept in sync between iOS devices that share an iCloud account. 

- **Daily Planner**. Yata deeply integrates with your device's calendar, allowing you to schedule pomodoro-style time blocks for your tasks in seconds.

- **Flexible Organisation System**. Categorise and group tasks in a way that makes most sense to you with as many (or as little) of the provided methods, such as **subtasking**, **tags**, **projects**, **areas**. 

- **Quick Add** allows you to create tasks with minimal friction. The appropriate attributes of the new task are automatically inferred based on your current location within the app. There is also support for **natural language dates**, allowing you to schedule tasks inline. 

### Other Features
- Recurring tasks
- Upload and view attachments to a task
- Edit tasks in bulk
- Customise the sort order of tasks
- Search tasks by the contents of their title and notes
- Light and Dark Themes

# Changelog

## [Known Issues]

## [Coming Soon]
- Widgets

## [Someday / Maybe]
- Habit Tracker
- Pomodoro Timer


## [0.6.0 (10)] - 2022-10-02
### Added
- Users will now experience haptic feedback when creating a todo or event

### Fixed
- Fix intermittent crashing on tapping the quick add button

## [0.6.0 (9)] - 2022-10-02
### Added
- Lock screen widgets for iOS 16 users!
  - You can now view your next upcoming task in your lock screen
  - More widgets such as those for the home screen are coming soon
- Improved the UX relating to expanding and collapsing task rows
  - The app will now automatically scroll to newly created tasks
  - The app will now automatically scroll to show the task row when the keyboard is activated such that the text field is not hidden
  - The app will now collapse a task row when user has finished editing
  - If a row is currently expanded, tapping on any other row will collapse it. Otherwise, the row is expanded as usual
- Add slight delay to edit task action and dismiss mini detail upon doing so

### Changed
- Reverted the previous change to the task title text fields

## [0.6.0 (8)] - 2022-09-30
### Added
- There is now a slight delay when adding tasks to allow for more UI feedback
- Added more functionality to the Canvas integration
  - When selecting an Area to add tasks from a Canvas course, your preferences are now saved between imports
  - Canvas tasks that have been added will now be hidden initially so they are not re-added by default

### Changed
- Do not allow rescheduling of read-only events
- Experimental: Editing the title of a task that is lower down on the list now does not result in the keyboard hiding the text field
  - However, this means that on non-iOS 16 devices, the text field is limited to a single line. 
  - On iOS 16 devices, the text field is still expandable but the animations are slightly choppy
  - Will revert if there is a net cost to UX

### Fixed
- The background of the Tasks view was partially blacked out in iOS 16


## [0.6.0 (7)] - 2022-09-27
### Added
- Task Priority System
  - You can now specify a priority level for a task
  - Tasks with a higher priority will be moved higher up in the task list! No more pinning tasks to get them to the top of the list
  - Hide reschedule button for events that are not editable
- https://stackoverflow.com/questions/4475120/iphone-how-to-detect-if-an-ekevent-instance-can-be-modified


### Fixed
- Users were unable to reschedule tasks or events in the Upcoming view
- Intent indicators were not updating visually, even though the task was rescheduled correctly
- Changes made to tasks in the Upcoming view were not being animated
- The "Add Subtask" button was not fully tappable

## [0.6.0 (6)] - 2022-09-26
### Added
- You can now specify a custom ordering for your subtasks
- The subtask section's UI is improved with the following changes
  - The checkmark has been replaced with a checkbox view that is more consistent with the app's UI
  - Tapping outside of checkbox now does not mark the subtask as complete
  - The keyboard is automatically activated when creating new subtasks
- You are now able to share attachments
- You can now swipe down to dismiss the mini detail view
- The task's checkbox is now colored depending on the task's project or area color

### Changed
- Your task's notes are now not copied over when completing them (if they are recurring tasks)
- You can now see the full title of your tasks in the mini detail view (previously, the title was truncated if it exceeded 2 lines)
- You can now see more of a task's notes in the mini detail view 
- You can now reschedule a task via the mini detail view (this replaces the previous action which was to duplicate a task)

### Fixed
- Fixed the Canvas import functionality not returning all results
- Fixed some dates not being parsed correctly (e.g. 8am instead of 830am) when creating or rescheduling tasks/events in the Upcoming tab, or in the Scheduled Tasks list


## [0.6.0 (4)] - 2022-09-25
### Fixed
- Hopefully reverted iCloud duplication issues with the last update


## [0.6.0 (3)] - 2022-09-24
### Added
- Add basic functionality to manage storage taken up by attachments
- Tapping on the Tasks tab now navigates to the root view.
- Tapping on the Upcoming tab now resets the selected date to the current date
- Added the ability to select/copy task title and notes in mini detail view
- Added colors to buttons depending on task's area color
- Added haptic feedback when todo detail view is activated

### Changed
- Parse dates from the back of text
  - If there are two dates, the one that occurs latest in the text is parsed
  - Example: "Do this today or on sunday" will parse as this Sunday instead of Today
- Increase intensity of haptic feedback when changing dates in calendar
- Gray out today's events that have past their times and completed tasks
- Creating new events will now default to the currently selected date
- Removed the restriction on duplicate project names
- Show area in project tasks list, and none where appropriate

## [0.6.0 (2)] - 2022-09-23
### Added
- Add task count to select all button when bulk editing
- Add indication of number of selected todos when bulk editing

### Changed
- Limit subtasks list's height, and make the list scrollable if it exceeds the constrained space
- Disallow setting of opacity for custom tag and project colors
- Rename title of canvas tutorial page

### Fixed
- Fix space taken up by todo notes not being constrained in Upcoming view


## [0.6.0 (1)] - 2022-09-23
### Added
- Import tasks from Canvas! Mainly applicable to NUS students. 
  - Allows users to fetch quizzes and assignments from Canvas to be added as tasks into the app. Check it out in the Settings tab.
- Further improvements to parsing logic
  - Rescheduling items in daily planner was not respecting selected date
  - Specifying meridiem was causing the parser to ignore the default date.
  	- For example, when rescheduling a task that was scheduled for tomorrow, "5am" was parsing as today's 5am, rather than tomorrow's 5am

### Changed
- Changed the UI of Settings page to fit the app theme
- Show tasks that were completed on the day in the daily planner.
Previously, if a task was not scheduled for the day but was marked complete on the day, it would not show up in the daily planner


## [0.5.0 (15)] - 2022-09-18
### DISCALAIMER 
Apologies for the duplication of data after the recent updates! Unfortunately, upon investigation it seems to be a bug on Apple's side... It occurs due to certain changes in the database that cannot be handled correctly by iCloud (so it duplicates all data as a safeguard). However, as the current state of the app's architecture is relatively mature already, hopefully such changes will not be required in the future!

### Added
- Show area or project under task title where appropriate

### Changed
- Deleting areas or projects now also deletes tasks within them.
- Users are not allowed to create tasks with an empty title
- Improve parsing logic by prioritising forward dates.
  - For example, parsing "at 2" when it is 10am should result in 2pm, rather than 2am
- Reset todos' collapse state when exiting task list

### Fixed
- Fix todo detail view title text field not aligned with placeholder


## [0.5.0 (14)] - 2022-09-14
### Added
- Newly created events will default to the currently selected date.

### Fixed
- Add back ability to create Calendar events directly.
  
## [0.5.0 (13)] - 2022-09-14
### Changed
- Hide intent indicators for Scheduled tasks list
- Replaced tutorial screen with simple introduction with link to online documentation (will be enhanced closer to production)

### Fixed
- Fixed bug where user was unable to edit or delete recurring events (changes were not being saved)
- Fix quick add not ignoring certain patterns such as "11a", "11:"
- Numerous under-the-hood improvements

## [0.5.0 (12)] - 2022-09-02
### Changed
- Add icons beside task list titles. Therefore, now intent indicators are hidden in anytime and someday views

### Fixed
- Fix bulk select bottom bar starting in the wrong position.
- Improve stability of area/project notes view (still requires further improvements).


## [0.5.0 (11)] - 2022-08-27
### Added
- Add placeholder to area tasks list if it is empty

### Changed
- Flag tasks that are due tomorrow as well. (Might make this a customisable setting)
- Exclude parsing {some digit}: as a date. For example, Watch Lecture 9: Title would be parsed as 9am due to the 9:

### Fixed
- Fix fatal bug when navigating around the app which was only recoverable by force quitting the app
- Fix tasks lists were not animating
- Fix task notes text cursor jumping to the end (was not actually fixed in the previous version)
- Fix quick add tag selector not dismissing when quick add dismisses
- Reset tapped tags when selector is dismissed


## [0.5.0 (10)] - 2022-08-26
### Added
- You can now add notes to areas and projects

### Fixed
- Bug where text cursor was jumping to the end of text when editing a task's notes


## [0.5.0 (9)] - 2022-08-25
### Added
- Added the ability to manually order areas and tags
- Add haptic feedback throughout app when marking tasks as complete/incomplete


## [0.5.0 (8)] - 2022-08-24
### Added
- Add Light mode theme! 
  - Users can switch between dark and light themes in the Settings, or opt for an "Automatic" setting which follows the current device's color scheme

### Changed
- Change quick add notes keyboard's return key from "Done" to default, as it inserts a new line rather than creating the task
- Make area icon selection buttons' hit box larger
- Change area icon selection color to gray
- Show create button for projects and areas by default

### Fixed
- Fix quick add not being consistent with inferring current context.
  - For example, if viewing a project's tasks, quick add should detect this and default the new task to the project. This should work no matter what screen the user navigates to. If the user does not change the default settings, the newly created task should always appear in the current list.
- Fix unable to edit task title when expanded


## [0.5.0 (7)] - 2022-08-22
### Added
- Mini detail sheet when selecting tasks in the Upcoming view.

### Changed
- Simplify subtask to narrow its purpose to creating simple checklists. Now, subtasks do not have the full functionality of a normal task, and instead simply comprise of a title and completion status. Users can utilise projects for more advanced needs. Previously the functionality of projects and subtasks were too similar, which can lead to user confusion.

### Fixed
- Also fixed a bug introduced in the previous version where creating a task would pop the current view off the navigation stack.


## [0.5.0 (6)] - 2022-08-20
### Fixed
- Fix bug where area icon was not selecting.
- Fix visual glitch when navigating between screens after expanding a task.


## [0.5.0 (5)] - 2022-08-20
### Fixed
- Fix bug with navigation view not responding after navigation
- Partially fix bug where edit button was not clickable after sheet has been presented

## [0.5.0 (4)] - 2022-08-19
### Added
- Add settings button to iPad on landscape to allow for access to settings screen
- Add clear button to textfield in Area detail view.

### Changed
-  Make textfield and preview icon larger in Area detail view.

### Removed
-  Removed blank icons from Area detail view.
-  Revert pinning sections in Completed and Scheduled list as it was causing infinite loop when bulk selecting

### Fixed
- Attempt to fix various visual glitches (tasks were getting stuck to the top of the screen, forcing user to force quit the app.)
- Fix settings view appearing to be blank on iPads in Portrait mode



## [0.5.0 (3)] - 2022-08-18
### Fixed
- Fix keyboard sometimes remaining on screen after creating todo


## [0.5.0 (2)] - 2022-08-18
### Added
- Setting to customise the default landing page of Tasks view
- Drag handle in calendar view to indicate to users that it is draggable (to toggle between Week and Month views)

### Fixed
- Attempt to fix issues with adding Calendar events (events were sometimes not saving or saving with incorrect date)


## [0.5.0 (1)] - 2022-08-17
### Added
- [Yata v2]({{ site.base-url }}/yata2)


## [0.3.0 (11)] - 2022-07-29
### Added
- UI improvements to attachments view
- UI improvements to the quick add date picker
- Restrict users from creating tasks with empty title

### Changed
- Updated gifs to higher quality and changed logic of gif playback to debug crashes (likely due to memory leaks)
- Slightly increased the size of each todo

### Fixed
- Fix crash when uploading attachments to a task
- Parser was detecting the correct time but removing the wrong portion of the text

## [0.3.0 (10)] - 2022-07-29
### Added
- Major UI changes to the todo detail view
- Smoother animations overall, especially when deleting todos or performing actions from the context menu
- Significanlty improved Natural language parser. It now infers duration, intent dates, due dates and due times. 
  - For example, try "Do assignment tomorrow at 4pm for two hours" or "Do assignment for two hours due in two days at 4pm"
- Ability to set an estimated duration for a task. This duration is used when scheduling tasks as Calendar events.
- "Do Today" and "Do Tomorrow" quick actions. 
  - "Do Today" sets the task's intent date to today, and moves it to the *Today* list.
  - "Do Tomorrow" sets the task's intent date to tomorrow, and moves it to the *Anytime* list.
- "Create Event" quick action. Creates a calendar event for the task without drag and drop.

### Changed
- Allow tasks to be recurring as long as intent date or due date is set 

### Removed
- Remove setting to toggle intent dates
- Removed tutorial gifs temporarily for debugging purposes


## [0.3.0 (9)] - 2022-07-27
### Added
- Intent durations. Setting an intended duration for a task means that when dragging it onto the calendar, the created event will automatically be set to that duration.
- Add a button that moves a todo to the selected list via the context menu

### Changed
- Updated the App Icon (draft)
- Updated the animation when completing a todo
- Reduce padding around show details button as due date text occasionally overflows
- Standardise UI and UX for todo recurrence picker
- Make notes editor dynamically size to fit text
- Change black background of detail view to dark gray
- Only show recurrence option if todo has due date
- Change time picker to show 5 minute intervals

### Fixed
- Fix: todo details sometimes not saving
- Fix: time picker icon was gray when no time was selected. It should always be blue
- Fix: context menu actions were not animating


## [0.3.0 (8)] - 2022-07-26
### Added
- Push notifications! Notifications are sent at a task's due date/time if it is set. If only a due date is specified, the notification will trigger at 9am (will be customisable in the future).
- Intent dates! Intent dates allow users to schedule a task to automatically move to the Today list at a specified date, whilst keeping this separate from the task's due date. This feature is OFF by default and can be enabled via the settings screen.
- Ability to specify due date AND time for task
- Options to automatically move tasks to Today list depending on due date (this behaviour is turned ON by default, and can be disabled in the settings screen)
- Persist the collapsed states for tags and projects filters section
- Add content to GTD lists onboarding

### Changed
- Changed the colour of the settings screen's top bar
- The filters menu now stretches when drag gesture over-shoots
- The filters menu now takes up slightly more space
- Modifying parent Eisenhower status now also modifies its subtasks' statuses
- Selecting the current todo list as a filter should not deselect it
- If no filter is selected, quick add applies the last used setting
- Prettified the due date sections in the task detail view
- Prettified the onboarding screens
- The collapse arrows in the filters menu is now hidden when there is nothing to show.


### Removed
- Removed the new project rows from the areas section. Users can use drag and drop to move a project into an area.
- Removed redundant word 'todo' from the context menu action labels


### Fixed
- Fix todo sometimes marking as completed even when in edit mode
- Fix crash when discarding changes from quick todo detail


## [0.3.0 (7)] - 2022-07-24

### Changed
- Disable edit mode when filters menu is dismissed
- Change the default behaviour to sort by completion date when filtering by completed tasks
- Calendar events do not split into two columns if they are immediately consecutive
- Remove more words that were being parsed as dates e.g. "vie", "fr", "mo"
- Add slight shadow to main view that overlays the filters menu
- Setting of overdue dates is now allowed
- Bias the parsed date to be a future date. For example, typing "mar" would be inferred as March 1st, 2023 rather than March 1st, 2022
- Projects and Tags filter sections are now collapsible
- Add buttons for projects, areas and tags are hidden unless editing (need to update tutorial gifs)

### Fixed
- Fix parsed date was highlighting the wrong range of text

## [0.3.0 (6)] - 2022-07-23

### Changed
- Change due date button to calendar icon, and today list icon to a star
- Hide quick add selector buttons if there are no options to select
- Move tags section to the bottom of filters view
- Only show all filters in edit mode when user expresses intent.
- Only show clear selection button when not editing
- Chang onboarding flow to show all views

### Removed
- Remove menu button from note view, users should not be able to enter edit mode from scratch pad

## [0.3.0 (5)] - 2022-07-22
### Added
- Allow tapping on page indicator to change page
- Add setting to increase size of page indicator
- Add more default filters (hidden by default):
  - Filter tasks by whether they have file attachments 
  - Filter tasks by whether they have url links in their notes content

### Changed
- Improved link detection, previously was not detecting links such as google.com, www.google.com


## [0.3.0 (4)] - 2022-07-21
### Changed
- Clear filters selection button is shown when at least one filter is selected
- Rearrange filters section
- Change default project color

### Fixed
- Project filter was not clearing when tapping the clear selection button
- Infinite looping glitch when todos had the same attributes

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


