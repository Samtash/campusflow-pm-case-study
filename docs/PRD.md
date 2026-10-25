# Product Requirements Document: CampusFlow

| | |
|---|---|
| **Product** | CampusFlow |
| **Version** | 1.0 (MVP) |
| **Author** | [Your name] |
| **Status** | Draft |
| **Last updated** | October 2026 |

## 1. Overview
CampusFlow is a mobile planner for busy university students. It helps students who juggle classes with tuition, clubs, work and family keep a changing week in view. The goal is to make adding and updating tasks so fast that students actually keep using it.

## 2. Problem
Busy students keep most of their tasks in their heads. They protect graded work, but classes they teach, club commitments and personal tasks slip. When a new task shows up, their plan breaks. Planning tools take too long to set up and keep updated, so students give up on them and blame their own discipline.

**Evidence** (full details in [Research.md](Research.md))
* 17 of 22 students rely mostly on memory
* 13 of 22 forgot or almost forgot something 2 or more times in 3 months
* "Too many things at once" was the top reason for forgetting (11 of 22)
* Only 3 of 22 said they missed the announcement, so finding info is not the main problem
* One interviewee quit Google Calendar because setup took too long and her week kept changing

## 3. Goals

**User goals**
* See the whole week, including non graded commitments, in one place
* Add or change a task in seconds
* Stop missing commitments to other people, like tuition classes and club meetings

**Business goals** (for a real launch)
* Get students to come back on their own, without a weekly planning session
* Prove that low setup effort keeps students using a planner past the first 2 weeks

## 4. Non goals for version 1
* **Syncing with Canvas or Google Classroom.** Hard to build, and scattered info is not the main pain.
* **File storage or sharing.** Came up in interviews, but it's a separate problem.
* **Group or class features.** Class reps already share info. CampusFlow is for the individual student.
* **Grade tracking or study timers.** Different job, different product.
* **Students with a light load.** See the Tanvir persona. They don't need this.

## 5. Target users
* **Primary:** Nusrat, the Juggler. Final year, heavy load outside class, quit Google Calendar.
* **Secondary:** Arif, the Group Chat Student. 2nd year, gets everything through WhatsApp and Messenger, forgets things he has already seen.

Full details in [Personas.md](Personas.md).

## 6. MVP features

| ID | Feature | What it does | Stories | Finding |
|---|---|---|---|---|
| F1 | Quick add | Add a task with just a name in one tap, from any screen | US01, US03 | #5 |
| F2 | Paste from chat | Paste text from a group chat. If it has a date, CampusFlow fills it in. | US02 | #2, #8 |
| F3 | Repeating commitments | Set up tuition classes, club meetings or work shifts once. They show up every week. | US05 | #3, #5 |
| F4 | Week view | All 7 days on one phone screen, color coded by type | US04 | #1, #3 |
| F5 | Today screen | The first screen. Shows what's due today and tomorrow, 7 items max. | US06 | #2 |
| F6 | Clash warning | When something new lands on a busy day, shows what else is there and lets the user move it | US07 | #4 |
| F7 | Commitment reminders | Reminder 1 hour before tuition, club or other commitments to people | US09 | #3 |

**Should have (version 1.1)**
* One tap reschedule (US08)
* Soft target dates for tasks with no deadline (US10)
* Mark tasks as graded or high stakes (US12)

## 7. Main user flow

**First time**
1. Student opens CampusFlow
2. App asks: "What do you do every week besides classes?" Student adds tuition, club meetings or work as repeating commitments (F3)
3. Student adds 2 or 3 upcoming tasks with quick add (F1)
4. Week view shows everything in one place (F4)

Target: done in under 3 minutes.

**Every day**
1. Student opens the app and sees the Today screen (F5)
2. A quiz is announced in a group chat. Student copies the message and pastes it into CampusFlow (F2)
3. CampusFlow sees Thursday is already full and shows a clash warning (F6)
4. Student keeps it on Thursday or moves something else in one tap

Target: under 30 seconds.

## 8. Success metrics

**North star metric**
Weekly active students who have tasks on at least 3 different days of the coming week. This shows they are actually using CampusFlow to see their week, not just opening it.

**Supporting metrics**

| Metric | Target |
|---|---|
| Finish first time setup | 70% of new users |
| Time to add a task | Under 10 seconds |
| Still active in week 2 | 40% of new users |
| Still active in week 4 | 25% of new users |
| Repeating commitments added in the first week | At least 1 per user |

**Outcome metrics** (checked with a short survey after 4 weeks)
* Fewer students say they forgot something 2 or more times in a month (baseline: 13 of 22 in 3 months)
* Average satisfaction goes from 3.3 to 4 out of 5

**Guardrail metrics**
* Time spent planning each week stays under 5 minutes. If it goes up, CampusFlow is becoming the thing students quit.
* Fewer than 20% of users turn off reminders. If more do, reminders are too noisy.

Full metrics plan in [Metrics.md](Metrics.md).

## 9. Risks

| Risk | Why it matters | How to reduce it |
|---|---|---|
| Students blame themselves, not their tools | They may not try a new app at all | Market it as "less effort," not "get organized." Keep setup under 3 minutes. |
| Students drop it after 2 weeks like Google Calendar | That's the exact pattern research found | No weekly planning session. Repeating commitments do most of the work. |
| Paste from chat reads dates wrong | Wrong dates break trust fast | Always show the date before saving. Let the user fix it. |
| Too many reminders | Students turn them off or delete the app | Only remind for commitments, not every task. Let users change timing. |
| Small research sample | Findings may not hold for all busy students | Test with 5 to 10 students before building more features |

## 10. Assumptions
* Busy students will spend 3 minutes on first time setup if it saves them time after
* Students check their phone daily, so a phone first app fits
* A clash warning is useful, not annoying

## 11. Open questions
* Should CampusFlow work offline? Many students have spotty data.
* Should the app support Bangla?
* Can paste from chat handle mixed Bangla and English messages?
* How should the app handle a commitment that gets cancelled for one week only?

## 12. Release plan
* **Version 1.0:** F1 to F7
* **Version 1.1:** Should have stories (US08, US10, US12)
* **Later:** Suggested order for today (US13), nudges for stuck tasks (US11)

Full plan in [Roadmap.md](Roadmap.md).
