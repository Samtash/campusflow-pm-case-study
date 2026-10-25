# User Stories

Format: As a [user], I want [action], so that [result].

Priority uses MoSCoW: **Must** (version 1 can't ship without it), **Should** (important, but can wait), **Could** (nice to have), **Won't** (not in version 1).

Each story links back to a finding in [Research.md](Research.md).

## Epic 1: Add things fast

| ID | Story | Priority | Finding |
|---|---|---|---|
| US01 | As Nusrat, I want to add a task in under 10 seconds, so that adding things never feels like work. | Must | #5 |
| US02 | As Arif, I want to paste text from a group chat and turn it into a task, so that I save it before it gets buried. | Must | #2, #8 |
| US03 | As Nusrat, I want to add a task without picking a date, so that I can capture it now and sort it later. | Should | #7 |

## Epic 2: See the whole week

| ID | Story | Priority | Finding |
|---|---|---|---|
| US04 | As Nusrat, I want to see classes, tuition, club work and personal tasks in one week view, so that nothing lives only in my head. | Must | #1, #3 |
| US05 | As Nusrat, I want to set up a repeating commitment like a tuition class once, so that I never have to enter it again. | Must | #3, #5 |
| US06 | As Arif, I want a short list of what's due today and tomorrow when I open the app, so that I don't have to scroll through chats. | Must | #2 |

## Epic 3: Handle changes

| ID | Story | Priority | Finding |
|---|---|---|---|
| US07 | As Nusrat, I want CampusFlow to show me what clashes when I add something new, so that a surprise quiz doesn't wreck my week. | Must | #4 |
| US08 | As Nusrat, I want to move a task to another day with one tap, so that fixing my plan takes seconds, not a planning session. | Should | #4, #5 |

## Epic 4: Protect the things that slip

| ID | Story | Priority | Finding |
|---|---|---|---|
| US09 | As Nusrat, I want a reminder before a tuition class or club meeting, so that I stop missing commitments to other people. | Must | #3 |
| US10 | As Nusrat, I want to set a soft target date for tasks with no deadline, so that long projects actually move. | Should | #7 |
| US11 | As Nusrat, I want a nudge when a task hasn't moved in a week, so that it doesn't sit forever. | Could | #7 |

## Epic 5: Decide what comes first

| ID | Story | Priority | Finding |
|---|---|---|---|
| US12 | As Nusrat, I want to mark a task as graded or high stakes, so that CampusFlow can show it first. | Should | #3 |
| US13 | As Arif, I want CampusFlow to suggest what to do first today, so that I don't waste time deciding. | Could | #8 |

## Not in version 1

| ID | Story | Priority | Why not |
|---|---|---|---|
| US14 | As a student, I want CampusFlow to pull deadlines from Canvas and Google Classroom on its own. | Won't | Hard to build, and research shows scattered info is not the main pain |
| US15 | As a student, I want to store and open course files across devices. | Won't | Came up in interviews, but it's a different problem |

## Acceptance criteria for Must stories

**US01: Add a task fast**
* Add button is visible on every screen
* Only the task name is required
* Saving takes one tap

**US02: Paste from a group chat**
* User can paste any text into the add box
* If the text has a date in it, CampusFlow fills in the date
* User can edit before saving

**US04: Week view**
* Shows 7 days on one screen
* Each type (class, tuition, club, personal) has its own color
* Works on a phone screen

**US05: Repeating commitments**
* User can pick which days and what time
* It shows up every week with no extra steps
* User can skip a single week without deleting the whole thing

**US06: Today and tomorrow list**
* It's the first screen when the app opens
* Shows no more than 7 items

**US07: Clash warning**
* When a new task lands on a busy day, CampusFlow says so
* It shows what else is on that day
* User can keep it or move it in one tap

**US09: Reminders for commitments to others**
* Reminder goes off 1 hour before by default
* User can change the time
