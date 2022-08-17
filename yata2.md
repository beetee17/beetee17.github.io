# Yet Another Todo App, Yet Again…

## Overview

In V2, many todo-related features remain unchanged. You may still organise your tasks by creating subtasks, Projects and Areas, or assign them tags, due dates and recurrences. 

The app is split into 2 main sections - Tasks and Schedule. The main focus is on the Schedule, and keeping the Tasks Inbox clean. 

The Schedule shows all tasks that you have scheduled for a certain day, and if you grant the app access to your calendar, it will display your events as well. 

The Inbox shows tasks that have yet to be scheduled. Tasks are scheduled by giving them an Intent Date, or by assigning them special dates known as Anytime or Someday. 

Anytime or Someday tasks will not appear in your Schedule, but are moved to a special folder (of the same name) within your Tasks so you can easily find them and assign them an actual date when you want to. 


## Main Changes

### Removed Eisenhower Matrix
The Eisenhower Matrix is an interesting productivity idea, but it did not fit in the app well. 

Firstly, the matrix view made the UI feel cramped, especially on compact devices like the iPhone. Users did have the option to switch to a List view, but that seems to defeat the purpose of the Eisenhower system. 

Having a cluttered UI can be detrimental to productivity, as it can lead users to feeling unnecessarily overwhelmed by the tasks presented to them. I wanted a todo app that evokes feelings of calm and peace, allowing for more focus on GTD. 

Secondly, basing the app on the Eisenhower system is opinionated. Not everyone may want to use the system, and the previous version essentially forces users to do so. 

Finally, the way it was implemented in V1 was somewhat confusing. For example, if I had a personal project that was not as important as school, would I label all the tasks in the project with a lower priority? This would quickly clutter up the grid as most tasks would be concentrated in only one or two cells. 

Or should I label them relative to the project’s priority? But this would mean that when I viewed the overall matrix, some of my unimportant project’s tasks would be classified higher than actually important tasks (e.g school work)


### Revamped Calendar View

The idea of time-blocking is an excellent productivity idea. It is still a part of the app in V2, with the key difference being that tasks do not actually go into your Calendar as an event. 

Again, the previous way of doing it was opinionated. Not everyone wants their tasks to become calendar events. 

The Schedule view has replaced the previous Calendar view (which mimicked the native iOS Calendar App). This is mainly due to the fact that the previous view used a third-party library, which meant that I was unable to customise and add features to it easily. For example, could only display actual calendar events on the timeline, which is the reason why V1 forced users to create tasks as calendar events if they wanted to view them in their schedule.  





 