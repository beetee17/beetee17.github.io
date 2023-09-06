# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1 (16-20)] - 2023-09-06

- Revert to iOS 16 code in preparation of update, as App Store does not accept beta submissions
- The only notable change is that interactive widgets have been disabled for iOS 17 beta. If you would like to have interactive widgets, do remain on version 2.1 (15).
- Expect this change to be reverted when iOS 17 GM build is released

## [2.1 (13-15)] - 2023-09-05

### Changed

- Subtask section is now easier to access in detail view
- Updated Tutorial gifs

## [2.1 (11-12)] - 2023-09-04

### Changed

- Reduce font weight and sizes in widgets

### Fixed

- Reduced app size significantly
- Occasional frame drops when switching back to app
- Deep linking to schedule not updating the calendar

## [2.1 (10)] - 2023-08-29

### Changed

- Default to Inbox view when in Sidebar layout instead of showing blank detail

### Fixed

- Fixed an issue with the sidebar not updating when the task counts changed

## [2.1 (9)] - 2023-08-29

### Added

- Added a numbers row above the keyboard when rescheduling tasks for easier date entry

### Changed

- Improved the arrangement of task row detailed layout in certain cases
- The detailed layout is now the default setting for new users
- Reduced load times when switching to Schedule tab by fetching data on app launch
- Changed Future icon color to blue instead of app theme's accent color
- Standardised (and made smaller) the font size of titles in the Schedule

### Fixed

- Fix navigation bug when switching tabs on iPad
- Preserve state in the Tasks Tab instead of overriding it completely if user reselects the same destination
- Fixed a bug causing some Task Lists to not animate when it was ungrouped

## [2.1 (8)] - 2023-08-25

### Fixed

- Fixed an issue with the lock screen widgets' text being grayed out on iOS 16 devices

## [2.1 (7)] - 2023-08-25

### Added

- Added the ability to edit project's area in detail view
- Added better deep links to the app for the Schedule widgets
- Added interactivity to the lock-screen Task widget
- Improved accessibility on various screens when using larger font sizes
- Added icons to the screen shown when configuring a Task widget

### Changed

- Reduced the undo banner's lifetime
- Removed an additional tap to confirm when moving tasks and projects
- Changed the icon appearance of calendar events
- Redirect the Submit Feedback button to Yata's canny.io feedback board

### Fixed

- Fixed a visual glitch when selecting a tag
- Fixed issues with the UI not refreshing after syncing with iCloud
- Fixed an issue where tasks created from the Share extension would not show in the UI till the next launch
- Fixed a missing add action when todo has no subtasks

## [2.1 (6)] - 2023-08-23

### Added

- Add ability to group or ungroup tasks by area in Inbox, Someday and Anytime lists.

### Changed

- Improved the UI of the Area/Project creation/edit screens

### Fixed

- Fix textfield not presenting on iOS16 when creating a todo
- Incorrect sort ordering of todos without due dates

## [2.1 (5)] - 2023-08-22

### Fixed

- Improve the performance of the text field when creating a todo
- Fix textfield being dismissed when dismissing the Task Mover when creating a todo
- Fix bug preventing users from saving a todo to a specified Area from the ShareExtension

## [2.1 (4)] - 2023-08-19

### Added

- A brand new theme gallery and editor!
- Area widgets have been revamped and renamed to Task widgets, as they can now show tasks from any list, i.e. Upcoming, Anytime, Someday, or even specific areas or projects.
- Schedule widgets now also show calendar events in addition to tasks

### Changed

- What's New page in preparation for upcoming release
- Delete outdated/unnecessary tutorial pages
- Expanded the hit-box of the quick add popup to prevent accidental dismissal

## [2.1 (3)] - 2023-08-04

### Fixed

- Some text fields were inserting unwanted text due to new iOS 17 autocorrect feature
- Performance improvements to task creation

## [2.1 (1-2)] - 2023-08-03

### Added

- Support for iOS 17 Interactive Widgets and StandBy mode. Try it out!
- View attachments directly from the MiniDetailView
- Undo/Redo critical actions
- Significant rewrites of the UI/Database layer to improve performance across many parts of the app

## [2.0.2 (3)] - 2023-04-01

### Fixed

- Timeblocking a scheduled task without inputting a date was not copying over the task's end date

## [2.0.2 (2)] - 2023-03-31

### Changed

- Use 'Tmr' keyword for tomorrow instead of the weekday
- Hide todos from the Inbox if they have incomplete timeblocks

### Fixed

- Filtering by tags was not working in some tasks lists

## [2.0.2 (1)] - 2023-03-30

### Added

- Added some keyboard shortcuts for todo detail view and quick add buttons. CTRL-n to create a task, CTRL-s to save edits to a task, and ESC to cancel edits

### Changed

- Use a more realistic mock database for previewing changes to the widget appearance

### Removed

- Remove unimplemented duplicate tasks button when bulk editing

### Fixed

- Fixed occasional crashes when typing a natural language date in Quick Add

## [2.0.1 (1-2)] - 2023-03-29

### Added

- There is now an option in the Settings Tab to export application logs if needed (e.g. send to me for debugging purposes). However, you are in full control of the log files, and you may inspect the contents before sending them (they are plain text files).
- These logs are anonymous, non-personal event data collected as the app runs, so if something odd happens (like a crash, or something doesn't load) there's some info that can help piece together why it happened. If you're having a particular issue the developer might ask you to send your specific logs to better figure out what's going on, and this is the way to do that! The logging is strictly done locally on the device, and NO user data is sent anywhere. Again they're anonymous with no way to tie them to a specific person or device, and their purpose is purely diagnostic.

## [2.0 (19)] - 2023-03-28

### Changed

- Completed tasks in the ScheduleView are now faded out

### Fixed

- Multiple UI inconsistencies and general ugliness on iOS 15 devices

## [2.0 (15-18)] - 2023-03-27

### Added

- Added a new dark default theme: Ocean

### Changed

- Tweak ScheduleView UI for sidebar layout (i.e. on iPads)
- Default to use numbers keyboard type on iPhones for faster input when rescheduling items

### Fixed

- Fixed a bug where the Save All button when importing tasks from Canvas was not working
- Fixed visual duplication of tasks when grouped by area
- Fixed a bug where tasks belonging to an area via a project was not appearing under that area in Tasks Lists that were grouped by area (complicated, I know).

## [2.0 (14)] - 2023-03-26

### Fixed

- Fixed glitchy animation for Select button when navigating to a Tasks List

## [2.0 (13)] - 2023-03-26

### Added

- Added cancel button for submit feedback alert.

### Changed

- Update GitHub feedback link to reflect new GitHub repo name
- Standardise SettingsView Icons to use flat colors rather than gradients

## [2.0 (12)] - 2023-03-26

### Added

- Added a communication channel for users to submit bug reports or feature requests via GitHub or Google Forms

### Fixed

- Fix ScheduleWidget not showing tasks in the same order as the ScheduleView
- Fixed deep linking from notifications not working on cold starts

## [2.0 (11)] - 2023-03-25

### Added

- Drastically improved performance of the app, especially for users with >1000 todos.
- Improved stability of deep linking feature
- Added badge counts to the Main Tasks screen
- Added the full context menu of TaskRows to ScheduleView items. Press and hold on a task in the ScheduleView to view a list of helper actions!
- Added priority indicator to MiniDetailView
- Added animations when confirming a TaskMover action

### Changed

- Removed some unnecessary padding in the Priority section of the TodoDetailView

### Fixed

- The rescheduler not parsing certain inputs intelligently, when only the end date's meridiem is specified. For example, "8 to 10am" should be equivalent to "8am to 10am". However, the parser was seeing the two dates independently. Since we prioritise forward dates, the "8" was being parsed as "8pm", hence the output was "8pm to 10am". This actually causes a crash as the end date is earlier than the start date!
- The bottom bar when bulk editing was not ignoring the keyboard

## [2.0 (7-10)] - 2023-03-24

### Added

- What's New page detailing the changes made in version 2.0. Find it in Settings → What's New.
- Added the ability to switch between the new and original icons. You can find this setting in Settings → App Icon
- Added the ability to export core data database (this is essentially only for debugging purpose)
- Added Haptic feedback to various user actions to improve U

### Fixed

- Completed projects were not hidden in AreaTasksListView by default.
- Bug where notifications were still being sent for tasks that had their intent dates removed. This occurs when time blocking a task (which creates a copy of it and removes the intent date from the original task).

## [2.0 (6)] - 2023-03-21

### Added

- Added the option to use a more detailed layout for task rows for those that prefer to see more at a glance! You can change from the default "Compact" style in Settings → Task Row Layout → "Detailed".
- Add the ability to mark Projects as completed. Completed Projects will be hidden by default.

### Changed

- A radically new app icon! Please do submit feedback on this change. An option to switch back to the previous icon will likely be implemented soon.
- Changed the default sort order to break ties by due date first before creation date

## [2.0 (5)] - 2023-03-12

### Added

- Add Developer Mode setting and DebuggingView
- Add option to sort by creation date

### Changed

- Change default sort order to break ties by creation date first before

### Fixed

- Fix Delete confirmation dialog disappearing immediately when trying todelete Projects or Areas
  lexicographical order

## [2.0 (4)] - 2023-02-27

### Fixed

- Fixed broken iCloud sync

## [2.0 (3)] - 2023-02-26

### Added

- You can now press and hold on a task to bring up its context menu for shortcuts to common actions
- Added an alert dialog when changing themes that informs the user that their changes may not be fully reflected in the app until the app is next restarted

### Fixed

- Fixed a visual issue where tasks with tags were not showing its tag indicator
